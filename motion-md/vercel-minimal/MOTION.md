# MOTION.md: Vercel Minimal

## Overview

Vercel Minimal defines crisp, restrained motion for developer tools, documentation, dashboards, and dark-mode-first product surfaces. Use it when the interface should feel fast, quiet, and technically sharp. Motion should be almost invisible until interaction: subtle opacity, tiny transforms, border or glow transitions, and minimal page choreography.

## Motion Philosophy

Motion should be minimal, crisp, dark-mode friendly, and almost invisible until interacted with. Prioritize clarity, speed, and restraint.

## Core Tokens

| Token | Value | Use |
| --- | --- | --- |
| `--motion-ease-minimal` | `cubic-bezier(0.16, 1, 0.3, 1)` | Default movement |
| `--motion-ease-linear` | `linear` | Progress and scanning effects |
| `--motion-fast` | `120ms` | Hover/focus |
| `--motion-default` | `240ms` | Reveals and panels |
| `--motion-slow` | `480ms` | Hero-only transitions |

## Entrance

- Page: opacity `0 -> 1`, `240ms`.
- Hero: opacity `0 -> 1`, `translateY(16px) -> 0`, `480ms`.
- Cards: opacity `0 -> 1`, `translateY(12px) -> 0`, stagger `35ms`, max `210ms`.
- Code blocks: opacity reveal, optional border glow `0 -> 1`, `240ms`.

## Interaction

- Button hover: border and background transition, optional `translateY(-1px)`.
- Card hover: border brightness and subtle background gradient shift.
- Link hover: text color transition or underline opacity, no bounce.
- Press: scale `0.99`, `80ms`.

## Scroll

- Use minimal reveals only once.
- Avoid heavy parallax.
- Decorative grid, beams, or spotlight effects may animate slowly and linearly.

## Transitions

- Route changes: fade and tiny y-shift only.
- Dialogs/popovers: opacity plus scale `0.98 -> 1`, `180ms`.
- Tabs: indicator slides `240ms`; content fades `120ms`.

## Reduced Motion

- Disable decorative beams, grid scans, and spotlight movement.
- Keep opacity transitions only.

## Don't

- Do not use large movement distances.
- Do not use elastic easing.
- Do not over-animate empty states or docs pages.

## Agent Instructions

Generate restrained developer-tool motion: minimal movement, crisp state transitions, subtle glow, and excellent dark-mode fit.
