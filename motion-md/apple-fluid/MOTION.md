# MOTION.md: Apple Fluid

## Overview

Apple Fluid defines calm, continuous, spatial motion for interfaces that should feel premium and directly manipulated. Use it for product pages, mobile-inspired UI, media surfaces, and app experiences where transitions need to preserve context. Motion should be soft, natural, and restrained: prefer continuity, depth, shared elements, subtle scale, and gentle deceleration over bounce or spectacle.

## Motion Philosophy

Motion should feel continuous, spatial, and quietly premium. Favor natural acceleration, soft deceleration, depth, and direct manipulation. Avoid theatrical bounce, jitter, or decorative effects.

## Core Tokens

| Token | Value | Use |
| --- | --- | --- |
| `--motion-ease-fluid` | `cubic-bezier(0.22, 1, 0.36, 1)` | Default movement |
| `--motion-ease-enter` | `cubic-bezier(0.16, 1, 0.3, 1)` | Entering surfaces |
| `--motion-ease-exit` | `cubic-bezier(0.7, 0, 0.84, 0)` | Dismissals |
| `--motion-fast` | `160ms` | Hover, focus, color |
| `--motion-default` | `320ms` | Component transitions |
| `--motion-slow` | `560ms` | Large spatial transitions |

## Entrance

- Main content: opacity `0 -> 1`, `translateY(18px) -> 0`, `320ms`.
- Hero title: opacity `0 -> 1`, `translateY(28px) -> 0`, `560ms`.
- Cards: opacity `0 -> 1`, `translateY(20px) -> 0`, stagger `45ms`, max `270ms`.
- Images: scale `1.035 -> 1`, opacity `0 -> 1`, `560ms`.

## Interaction

- Button hover: `translateY(-1px)`, subtle shadow increase, `160ms`.
- Card hover: `translateY(-4px)`, scale `1.005`, shadow softens outward, `320ms`.
- Press: scale to `0.985` for surfaces, `0.96` for buttons.
- Focus: animate focus ring opacity and offset, never remove keyboard focus.

## Transitions

- Prefer continuity between states: preserve containers, images, titles, or selected controls.
- Use shared-element style transforms for card-to-detail and image expansion.
- Top-level unrelated views should fade cleanly, not slide dramatically.
- Avoid moving many independent elements in different directions.

## Component Motion

| Component | Motion |
| --- | --- |
| Button | Hover lifts `-1px` with soft shadow over `160ms`; press scales to `0.96` and releases with `--motion-ease-fluid`. |
| Card | Hover lifts `-4px`, scale `1.005`, and deepens shadow over `320ms`; selected cards may expand with shared-element continuity. |
| Dialog | Enter with opacity `0 -> 1`, scale `0.96 -> 1`, and y `18px -> 0` over `320ms`; close with opacity and slight scale down over `200ms`. |
| Popover/Menu | Grow from trigger origin with opacity `0 -> 1`, scale `0.98 -> 1`, and y `8px -> 0` over `200ms`. |
| Sheet/Drawer | Slide from owning edge over `320ms` to `560ms`, keeping inner content slightly delayed by `60ms`. |
| Tabs/Segmented control | Move the selected indicator with a continuous transform over `320ms`; fade content over `160ms` only when needed. |
| Toast | Rise from bottom with opacity `0 -> 1`, y `14px -> 0`, `320ms`; dismiss toward the edge over `200ms`. |
| Form field | Focus ring, label, and helper text animate through color, opacity, and tiny y shifts over `160ms`; do not move the input box. |
| List item | Insert with opacity `0 -> 1`, y `10px -> 0`, stagger `35ms`; removal fades first, then collapses space. |
| Loading | Use stable skeletons with a soft pulse around `1400ms`; loaded content fades in under `160ms`. |

## Scroll

- Use gentle reveal only for editorial or marketing content.
- Avoid scroll motion in dense product UI.
- Parallax must be subtle: background moves no more than `8%` slower than foreground.

## Reduced Motion

- Replace scale, parallax, and long spatial movement with opacity transitions under `120ms`.
- Preserve essential state changes.

## Don't

- Do not use elastic bounce.
- Do not use glitch, shake, or aggressive rotation.
- Do not animate layout in ways that feel detached from user intent.

## Agent Instructions

Generate calm, continuous motion using transform and opacity. Prioritize spatial relationship, direct manipulation, and premium restraint.
