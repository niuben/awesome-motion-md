# MOTION.md: Fluent Productive

## Motion Philosophy

Motion should support productivity: fast, legible, layered, and functional. Use motion to clarify hierarchy and state, not to entertain.

## Core Tokens

| Token | Value | Use |
| --- | --- | --- |
| `--motion-ease-standard` | `cubic-bezier(0.1, 0.9, 0.2, 1)` | Default productive movement |
| `--motion-ease-decelerate` | `cubic-bezier(0, 0, 0, 1)` | Enter |
| `--motion-ease-accelerate` | `cubic-bezier(1, 0, 1, 1)` | Exit |
| `--motion-fast` | `120ms` | Control feedback |
| `--motion-default` | `200ms` | Menus and panels |
| `--motion-slow` | `320ms` | Larger surfaces |

## Entrance

- Panels: opacity `0 -> 1`, `translateY(8px) -> 0`, `200ms`.
- Menus: opacity `0 -> 1`, scale `0.98 -> 1`, origin from trigger, `120ms`.
- Cards: opacity `0 -> 1`, `translateY(10px) -> 0`, stagger `25ms`, max `150ms`.
- Toolbars and navigation should appear stable; avoid decorative entrance motion.

## Interaction

- Button hover: color and background transition only, `120ms`.
- Button press: scale `0.98`, `80ms`.
- List row hover: background tint transition, no vertical movement.
- Panel resize: animate transform or clip when possible, `200ms`.

## Transitions

- Use small movement distances: `8px` to `16px`.
- Use layering: menus and flyouts emerge from their trigger.
- Navigation between work areas should be quick fade or short slide.
- Dismissals should be faster than entrances.

## Loading

- Prefer progress bars, skeleton rows, and stable placeholders.
- Skeleton pulse should be subtle and slow, `1200ms`.

## Reduced Motion

- Remove slides and scaling. Keep background, opacity, and outline changes.

## Don't

- Do not use bounce or overshoot in productivity UI.
- Do not animate tables row-by-row unless explicitly requested.
- Do not delay user workflows with long choreography.

## Agent Instructions

Generate efficient enterprise/productivity motion with small distances, short durations, stable layouts, and clear state feedback.
