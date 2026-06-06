# MOTION.md: Game Impact

## Motion Philosophy

Motion should feel punchy, energetic, and rewarding. Use anticipation, overshoot, impact frames, particles, shake, and strong feedback. This style is for demos, game UI, launches, and playful experiences.

## Core Tokens

| Token | Value | Use |
| --- | --- | --- |
| `--motion-ease-impact` | `cubic-bezier(0.34, 1.56, 0.64, 1)` | Impact bounce |
| `--motion-ease-slam` | `cubic-bezier(0.7, -0.4, 0.2, 1.4)` | Aggressive entrance |
| `--motion-hit` | `120ms` | Impact frame |
| `--motion-fast` | `220ms` | Buttons and pickups |
| `--motion-default` | `420ms` | Cards and panels |
| `--motion-combo` | `700ms` | Reward sequence |

## Entrance

- Hero title: scale `1.3 -> 0.92 -> 1`, opacity `0 -> 1`, `420ms`.
- Cards: rotate `-4deg -> 0`, y `40px -> 0`, stagger `50ms`.
- Buttons: anticipation scale `0.85 -> 1.08 -> 1`.
- Badges: pop with overshoot and optional particle burst.

## Interaction

- Button hover: scale `1.08`, glow, `220ms`.
- Button press: scale `0.9`, then rebound to `1.06`.
- Card hover: lift `-10px`, rotate `1deg` to `3deg`, shadow intensifies.
- Success state: pulse, burst, count-up, or shine sweep.

## Effects

- Screen shake allowed only for explicit impact moments, max `6px`, max `180ms`.
- Particles must be short-lived, under `700ms`.
- Looping attention effects must be rare and pause on hover/focus when needed.

## Scroll

- Use explosive stagger for showcase pages.
- Maximum total stagger delay `500ms`.

## Reduced Motion

- Disable shake, particles, bounce, and large scale changes.
- Replace with color, opacity, and short scale under `1.02`.

## Don't

- Do not use this style for serious dashboards or forms.
- Do not shake text while users are reading.
- Do not run infinite pulsing on many elements.

## Agent Instructions

Generate energetic motion with anticipation, impact, rebound, rewards, and strong interaction feedback while respecting reduced motion.
