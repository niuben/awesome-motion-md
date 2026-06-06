# MOTION.md: GSAP Cinematic

## Overview

GSAP Cinematic defines timeline-driven, high-impact motion for marketing pages, launches, portfolios, and visual storytelling. Use it when the page needs directed sequences, scroll choreography, masks, staged text reveals, and strong contrast between stillness and motion. This style is intentionally expressive and should be reserved for moments where visual drama supports the content.

## Motion Philosophy

Motion should feel directed, sequenced, and visually dramatic. Use timelines, layered reveals, masks, scroll choreography, and strong contrast between stillness and movement.

## Core Tokens

| Token | Value | Use |
| --- | --- | --- |
| `--motion-ease-cinematic` | `cubic-bezier(0.77, 0, 0.175, 1)` | Dramatic transitions |
| `--motion-ease-out` | `cubic-bezier(0.16, 1, 0.3, 1)` | Reveals |
| `--motion-hit` | `180ms` | Impact beats |
| `--motion-scene` | `800ms` | Scene transitions |
| `--motion-ambient` | `1600ms` | Slow atmospheric motion |

## Entrance

- Use timeline sequencing, not simultaneous fades.
- Hero title: split lines or words, y `110% -> 0`, opacity `0 -> 1`, stagger `60ms`.
- Visual asset: mask reveal or clip-path wipe, `800ms`.
- CTA: delayed scale `0.92 -> 1`, opacity `0 -> 1`, `400ms`.

## Interaction

- Button hover: magnetic pull up to `8px`, glow or invert effect.
- Card hover: 3D tilt max `8deg`, image zoom `1.08`, overlay reveal.
- Cursor-follow effects allowed only on marketing/creative pages.

## Scroll

- Use scroll-triggered scenes and pinned sections for storytelling.
- Parallax depth: foreground `1x`, midground `0.65x`, background `0.35x`.
- Scrubbed animation must preserve readability.
- Avoid triggering more than one major scene at the same scroll position.

## Transitions

- Use wipes, masks, reveals, and camera-like movement.
- Between sections: one dominant direction only.
- Scene changes may last `800ms` to `1200ms`.

## Reduced Motion

- Disable pinned scroll, parallax, cursor-follow, and 3D tilt.
- Use quick opacity and mask-free reveals.

## Don't

- Do not use cinematic motion in dense productivity screens.
- Do not animate text so much that reading becomes difficult.
- Do not create scroll hijacking without clear value.

## Agent Instructions

Generate high-impact marketing motion using timelines, staggered text, masks, scroll scenes, and strong visual rhythm.
