# MOTION.md: Stripe Polished

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

## Reduced Motion

- Disable parallax, perspective tilt, animated gradients, and long staggers.
- Keep opacity reveals under `150ms`.

## Don't

- Do not use chaotic bounce or glitch.
- Do not animate gradients so fast they distract from content.
- Do not make business UI feel like a game.

## Agent Instructions

Generate premium landing-page motion with smooth reveals, subtle depth, refined hover states, and high perceived polish.
