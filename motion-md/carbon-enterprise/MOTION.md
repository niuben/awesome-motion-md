# MOTION.md: Carbon Enterprise

## Motion Philosophy

Motion should be precise, restrained, accessible, and appropriate for complex enterprise software. It should reduce cognitive load and clarify cause and effect.

## Core Tokens

| Token | Value | Use |
| --- | --- | --- |
| `--motion-ease-productive` | `cubic-bezier(0.2, 0, 0.38, 0.9)` | Productive micro-interactions |
| `--motion-ease-expressive` | `cubic-bezier(0.4, 0.14, 0.3, 1)` | Important UI changes |
| `--motion-fast-01` | `70ms` | Immediate response |
| `--motion-fast-02` | `110ms` | Hover and focus |
| `--motion-moderate-01` | `150ms` | Small component transitions |
| `--motion-moderate-02` | `240ms` | Panels and disclosure |
| `--motion-slow-01` | `400ms` | Large surface changes |

## Entrance

- Data panels: opacity `0 -> 1`, `translateY(8px) -> 0`, `240ms`.
- Cards and tiles: opacity `0 -> 1`, `translateY(12px) -> 0`, stagger `30ms`, max `180ms`.
- Tables: do not animate individual rows on initial load; use skeleton or quick fade.
- Charts: reveal axes first, then data marks over `400ms` only if it improves comprehension.

## Interaction

- Buttons: background, border, and text color transition `110ms`.
- Press: immediate tonal change, optional scale `0.99` only for large buttons.
- Accordion: expand/collapse over `240ms`; avoid bouncing height.
- Side panel: slide from owning edge over `240ms` to `400ms` depending on width.

## Transitions

- Use motion to show hierarchy: disclosure, drill-down, panel opening, filtering.
- Prefer direct, orthogonal movement along x or y axes.
- Dense workflows should prioritize speed over expressiveness.

## Accessibility

- Always support reduced motion.
- Avoid flashing, looping attention effects, and large parallax.
- Focus indicators must be visible and animated only through color or opacity.

## Don't

- Do not animate dense tables, logs, or code blocks item-by-item.
- Do not use decorative spring bounce.
- Do not hide loading with layout shifts.

## Agent Instructions

Generate enterprise-safe motion: precise, short, accessible, and optimized for data-heavy interfaces.
