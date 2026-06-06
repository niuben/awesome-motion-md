# MOTION.md: Linear Snappy

## Overview

Linear Snappy defines ultra-fast motion for modern SaaS and keyboard-driven product interfaces. Use it for issue trackers, command palettes, developer tools, collaboration apps, and high-frequency workflows. Motion should feel nearly instant: tiny distances, very short durations, crisp hover states, and responsive transitions that reinforce speed instead of calling attention to themselves.

## Motion Philosophy

Motion should feel instant, sharp, and keyboard-fast. The interface should respond before the user has time to notice the animation.

## Core Tokens

| Token | Value | Use |
| --- | --- | --- |
| `--motion-ease-snap` | `cubic-bezier(0.16, 1, 0.3, 1)` | Default snappy movement |
| `--motion-ease-out` | `cubic-bezier(0, 0, 0.2, 1)` | Reveals |
| `--motion-instant` | `60ms` | Press feedback |
| `--motion-fast` | `120ms` | Hover, focus, command UI |
| `--motion-default` | `180ms` | Panels, popovers |
| `--motion-slow` | `260ms` | Rare larger transitions |

## Entrance

- App shell: no theatrical entrance.
- Command palette: opacity `0 -> 1`, scale `0.985 -> 1`, `180ms`.
- Popovers: opacity `0 -> 1`, `translateY(6px) -> 0`, `120ms`.
- Cards/issues: opacity `0 -> 1`, `translateY(8px) -> 0`, stagger `18ms`, max `108ms`.

## Interaction

- Hover: background tint and border color, `120ms`.
- Press: scale `0.985`, `60ms`.
- Keyboard navigation: selected row highlight moves immediately, color transition `60ms`.
- Drag/reorder: use direct transform, no laggy easing during drag; settle in `180ms`.

## Transitions

- Route changes: quick fade with `translateX(8px)` max.
- Modal open: scale `0.98 -> 1`, opacity `0 -> 1`, `180ms`.
- Modal close: opacity `1 -> 0`, scale `1 -> 0.99`, `120ms`.

## Scroll

- Avoid scroll-triggered decoration in app UI.
- Marketing pages may use tight staggered reveals with max delay `160ms`.

## Don't

- Do not use long hero choreography inside product UI.
- Do not use bounce, wobble, or large parallax.
- Do not make hover transforms bigger than `2px` or `1.01` scale.

## Agent Instructions

Generate fast SaaS/product motion with short durations, small distances, sharp response, and minimal visual noise.
