# MOTION.md: Stripe Polished

## Overview

Stripe Polished defines refined, commercial motion for high-trust landing pages and product marketing surfaces. Use it when the interface needs to feel premium, technical, layered, and conversion-focused. Motion should combine smooth reveals, subtle depth, gradient movement, staggered content, and refined hover states without becoming playful or chaotic.

## Motion Philosophy

Motion should feel refined, commercial, layered, and technically polished. Use subtle depth, gradient movement, staggered reveals, and smooth component state changes.

## Core Tokens

| Token | Value | Use |
| --- | --- | --- |
| `--motion-ease-polished` | `cubic-bezier(0.22, 1, 0.36, 1)` | Default movement |
| `--motion-ease-soft` | `cubic-bezier(0.33, 1, 0.68, 1)` | Effects and gradients |
| `--motion-fast` | `180ms` | Hover and focus |
| `--motion-default` | `420ms` | Section reveals |
| `--motion-slow` | `700ms` | Hero and ambient motion |

## Entrance

- Hero copy: opacity `0 -> 1`, `translateY(30px) -> 0`, `700ms`.
- CTA buttons: opacity `0 -> 1`, scale `0.96 -> 1`, `420ms`, delayed after headline.
- Product cards: opacity `0 -> 1`, `translateY(36px) -> 0`, stagger `60ms`, max `360ms`.
- Code blocks or dashboards: clip reveal or mask wipe, `420ms`.

## Interaction

- Button hover: gradient position shift, `translateY(-2px)`, shadow increase, `180ms`.
- Card hover: `translateY(-8px)`, shadow and border glow increase, `420ms`.
- Link hover: underline sweep or arrow nudge `4px`.
- Product mockups: subtle perspective tilt is allowed, max `4deg`.

## Scroll

- Use section-based reveal with restrained stagger.
- Background gradients may drift slowly, `8s` to `16s`, only for decorative layers.
- Parallax must be subtle and never block readability.

## Transitions

- Prefer masked reveals, sliding panels, and layered depth.
- Keep top-level navigation transitions quick and clean.
- Use skeletons for dashboards and payment UI.

## Component Motion

| Component | Motion |
| --- | --- |
| Button | Hover shifts gradient position, lifts `-2px`, and increases shadow over `180ms`; press scales to `0.97`. |
| Card | Hover lifts `-8px`, increases border glow, and may zoom media to `1.035` over `420ms`. |
| Dialog | Enter with opacity `0 -> 1`, scale `0.96 -> 1`, y `24px -> 0`, `420ms`; dim overlay fades over `180ms`. |
| Popover/Menu | Use polished layered reveal: opacity, y `10px -> 0`, and subtle blur `8px -> 0` over `180ms` to `240ms`. |
| Pricing/Feature table | Reveal columns with `60ms` stagger; hover highlights cells through background and border, not row movement. |
| Tabs | Slide underline or pill indicator over `420ms`; content crossfades over `180ms` with a tiny y shift. |
| Toast/Banner | Slide from top or bottom with opacity over `420ms`; add a restrained shine sweep only for success or upgrade moments. |
| Form field | Focus animates border glow and label color over `180ms`; validation message fades and moves `6px` over `180ms`. |
| Carousel/Testimonial | Move as a grouped layer over `420ms`; avoid independent text and image directions. |
| Loading | Use skeleton shimmer or masked reveal at `1000ms` to `1400ms`; keep shimmer low contrast. |

## Reduced Motion

- Disable parallax, perspective tilt, animated gradients, and long staggers.
- Keep opacity reveals under `150ms`.

## Don't

- Do not use chaotic bounce or glitch.
- Do not animate gradients so fast they distract from content.
- Do not make business UI feel like a game.

## Agent Instructions

Generate premium landing-page motion with smooth reveals, subtle depth, refined hover states, and high perceived polish.
