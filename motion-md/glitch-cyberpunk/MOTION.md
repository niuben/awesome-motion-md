# MOTION.md: Glitch Cyberpunk

## Overview

Glitch Cyberpunk defines electric, neon, digitally unstable motion for cyberpunk, hacker, music, gaming, and experimental visual interfaces. Use it when the brand can support scanlines, flicker, chromatic offsets, clipped reveals, and brief displacement. Glitches must be short, intentional, and accessibility-safe: never apply rapid flashing or unstable motion to long-form reading content.

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

## Component Motion

| Component | Motion |
| --- | --- |
| Button | Hover intensifies neon glow and triggers one `40ms` to `80ms` x-offset glitch; press uses hard cut scale `0.96 -> 1`. |
| Card | Hover flickers border once, raises noise opacity, and may add RGB split for `80ms`; settle with `--motion-ease-neon`. |
| Dialog | Enter with clipped wipe, opacity flicker, and final settle over `360ms`; overlay should not flash full-screen. |
| Popover/Menu | Reveal with scanline wipe and item flicker stagger `30ms`; keep text readable after the burst. |
| Tabs | Indicator snaps with segmented underline; content changes through clipped reveal, not continuous distortion. |
| Toast/Alert | Use neon border flash for one hit, then stable state; critical alerts must remain legible and non-flashing. |
| Form field | Focus can show scanline underline and glow over `160ms`; validation errors may glitch once, never while typing continuously. |
| Data panel | Use clipped panel reveals and subtle grid scan; avoid glitching dense numbers or code blocks. |
| Progress/Loader | Linear scan or terminal-style cursor blink; keep blink rate accessible and pause on completion. |
| Media | RGB split is allowed only for key visuals and should resolve within `120ms`. |

## Reduced Motion

- Disable flicker, rapid displacement, RGB split, and scanline movement.
- Use static neon styles and short opacity transitions.

## Don't

- Do not use high-frequency flashing.
- Do not apply glitch to body paragraphs or long reading content.
- Do not combine large shake with flicker.

## Agent Instructions

Generate cyberpunk motion with brief glitch bursts, neon state changes, clipped reveals, and strict accessibility safeguards.
