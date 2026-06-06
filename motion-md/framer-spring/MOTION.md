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

## Reduced Motion

- Disable layout morphing and gesture rebound.
- Keep direct opacity changes and instant layout updates.

## Don't

- Do not approximate every spring with long CSS transitions if real springs are available.
- Do not let bouncy springs affect opacity or color.
- Do not use gesture physics on static content without clear affordance.

## Agent Instructions

If using Framer Motion or similar libraries, use real springs, layout animation, shared elements, and interruptible gesture motion.
