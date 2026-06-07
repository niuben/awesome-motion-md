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

## Component Motion

| Component | Motion |
| --- | --- |
| Button | Hover changes border/background over `120ms`, optional y `-1px`; press scales `0.99` for `80ms`. |
| Card | Hover increases border brightness and background gradient opacity over `240ms`; avoid visible lift. |
| Dialog | Enter with opacity, scale `0.98 -> 1`, y `8px -> 0`, `180ms`; overlay fades over `120ms`. |
| Popover/Menu | Use opacity plus scale `0.98 -> 1` over `120ms`; active item highlight fades in `120ms`. |
| Command palette | Fade and scale over `180ms`; result highlight moves instantly with a `120ms` background transition. |
| Tabs | Indicator slides `240ms`; content fades `120ms`; avoid heavy page-level choreography. |
| Toast | Fade and y `8px -> 0` over `180ms`; exit with opacity over `120ms`. |
| Form field | Animate focus ring, border glow, and validation text opacity over `120ms`; keep layout fixed. |
| Code block | Copy button fades in on hover over `120ms`; line highlight uses background transition only. |
| Loading | Use static skeletons or subtle linear shimmer; disable decorative scans in reduced motion. |

## Reduced Motion

- Disable decorative beams, grid scans, and spotlight movement.
- Keep opacity transitions only.

## Don't

- Do not use large movement distances.
- Do not use elastic easing.
- Do not over-animate empty states or docs pages.

## Agent Instructions

Generate restrained developer-tool motion: minimal movement, crisp state transitions, subtle glow, and excellent dark-mode fit.
