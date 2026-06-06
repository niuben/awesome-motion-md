# MOTION.md: Apple Fluid

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
