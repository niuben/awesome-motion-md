# MOTION.md: Glitch Cyberpunk

## Motion Philosophy

Motion should feel electric, unstable, neon, and digital. Use quick cuts, scanlines, chromatic offsets, flickers, and abrupt displacement. Keep glitches intentional and brief.

## Core Tokens

| Token | Value | Use |
| --- | --- | --- |
| `--motion-ease-cut` | `steps(2, end)` | Glitch cuts |
| `--motion-ease-neon` | `cubic-bezier(0.16, 1, 0.3, 1)` | Settling after glitch |
| `--motion-glitch-hit` | `80ms` | Single glitch burst |
| `--motion-fast` | `160ms` | Hover effects |
| `--motion-default` | `360ms` | Reveals |
| `--motion-loop` | `2200ms` | Ambient neon flicker |

## Entrance

- Hero title: opacity flicker `0/1`, x offsets `-8px/6px/0`, `360ms`.
- Cards: clip-path wipe plus neon border flash, stagger `45ms`.
- Images: RGB split for `80ms`, then settle to normal.
- Buttons: scanline sweep, opacity `0 -> 1`, `160ms`.

## Interaction

- Button hover: neon glow intensifies, text shifts `1px` horizontally in one glitch burst.
- Card hover: border flicker and background noise opacity increase.
- Link hover: underline becomes segmented or scanline-based.

## Effects

- Glitch bursts should last `40ms` to `120ms`.
- Ambient flicker must be subtle and infrequent.
- Avoid full-screen flashing above safe thresholds.

## Scroll

- Use scanline reveals and clipped section wipes.
- Do not glitch every element; reserve glitches for headings, CTAs, and key visuals.

## Reduced Motion

- Disable flicker, rapid displacement, RGB split, and scanline movement.
- Use static neon styles and short opacity transitions.

## Don't

- Do not use high-frequency flashing.
- Do not apply glitch to body paragraphs or long reading content.
- Do not combine large shake with flicker.

## Agent Instructions

Generate cyberpunk motion with brief glitch bursts, neon state changes, clipped reveals, and strict accessibility safeguards.
