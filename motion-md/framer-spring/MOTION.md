# MOTION.md: Framer Spring

## Overview

Framer Spring defines physical, interruptible, gesture-aware motion for interfaces that benefit from real spring behavior and layout animation. Use it for prototypes, interactive product UI, draggable surfaces, shared element transitions, reorderable lists, and playful but controlled component motion. Prefer real springs and layout transitions over fixed CSS timelines whenever the platform supports them.

## Motion Philosophy

Motion should feel physical, interruptible, gesture-aware, and layout-native. Prefer spring behavior, shared layout transitions, and direct manipulation.

## Spring Tokens

| Token | Stiffness | Damping | Use |
| --- | --- | --- | --- |
| `spring.snappy` | `520` | `34` | Buttons, small controls |
| `spring.default` | `360` | `30` | Cards, modals, layout changes |
| `spring.gentle` | `220` | `26` | Large surfaces |
| `spring.bouncy` | `420` | `18` | Playful hero moments only |

CSS fallback: use `cubic-bezier(0.34, 1.56, 0.64, 1)` for bouncy spatial motion and `cubic-bezier(0.16, 1, 0.3, 1)` for non-bouncy motion.

## Entrance

- Components: opacity `0 -> 1`, scale `0.96 -> 1`, y `20px -> 0`.
- Layout groups: animate from previous layout whenever possible instead of independent keyframes.
- Lists: stagger `35ms`, max `280ms`.

## Interaction

- Hover: scale `1.03` for buttons, `1.015` for cards.
- Tap: scale `0.95` for buttons, `0.985` for cards.
- Drag: element follows pointer directly; spring only on release.
- Reorder: siblings animate to new layout with `spring.default`.

## Transitions

- Use shared layout IDs for cards expanding into detail views.
- Use `AnimatePresence`-style exit motion when removing elements.
- Exit: opacity `1 -> 0`, scale `1 -> 0.96`, y `0 -> -8px`.

## Gestures

- Swipe dismiss threshold: `35%` of width or sufficient velocity.
- On failed swipe, spring back with `spring.default`.
- Avoid gesture motion that conflicts with native scroll.

## Component Motion

| Component | Motion |
| --- | --- |
| Button | Use `whileHover` scale `1.03` and `whileTap` scale `0.95` with `spring.snappy`; keep color transitions separate. |
| Card | Use layout animation for resize/reorder; hover scale `1.015`, tap `0.985`, and shared layout for expansion. |
| Dialog | Enter with opacity, scale `0.96 -> 1`, y `20px -> 0` using `spring.default`; exit through `AnimatePresence`. |
| Popover/Menu | Anchor to trigger with transform origin; opacity plus scale `0.96 -> 1` using `spring.snappy`. |
| Bottom sheet | Drag follows pointer directly; release snaps to detents with `spring.default` or dismisses after threshold. |
| Tabs | Use shared `layoutId` for the indicator; content can crossfade or slide with `spring.default`. |
| Toast | Enter from edge with `spring.default`; swipe dismiss with velocity and spring-back on failed gesture. |
| Form field | Animate label position, helper text, and validation presence with layout transitions; avoid bouncy opacity. |
| Reorderable list | Use layout animation for siblings and direct drag for active item; settle with `spring.default`. |
| Loading | Crossfade skeleton to loaded content and let layout animate to final size instead of jumping. |

## Reduced Motion

- Disable layout morphing and gesture rebound.
- Keep direct opacity changes and instant layout updates.

## Don't

- Do not approximate every spring with long CSS transitions if real springs are available.
- Do not let bouncy springs affect opacity or color.
- Do not use gesture physics on static content without clear affordance.

## Agent Instructions

If using Framer Motion or similar libraries, use real springs, layout animation, shared elements, and interruptible gesture motion.
