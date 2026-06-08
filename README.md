# awesome-motion.md

![awesome-motion.md animated logo](asset/logo-motion.svg)

A curated collection of `MOTION.md` files that help AI agents generate stunning, non-boring UI animations.


## Preview Gallery

Each preview uses the same UI elements, while the visual style and motion behavior are generated from its own `MOTION.md`.

| Material Expressive | Apple Fluid |
| --- | --- |
| ![Material Expressive preview](asset/previews/material-expressive.gif) | ![Apple Fluid preview](asset/previews/apple-fluid.gif) |

| Fluent Productive | Carbon Enterprise |
| --- | --- |
| ![Fluent Productive preview](asset/previews/fluent-productive.gif) | ![Carbon Enterprise preview](asset/previews/carbon-enterprise.gif) |

| Linear Snappy | Stripe Polished |
| --- | --- |
| ![Linear Snappy preview](asset/previews/linear-snappy.gif) | ![Stripe Polished preview](asset/previews/stripe-polished.gif) |

| Vercel Minimal | Framer Spring |
| --- | --- |
| ![Vercel Minimal preview](asset/previews/vercel-minimal.gif) | ![Framer Spring preview](asset/previews/framer-spring.gif) |

| GSAP Cinematic | Game Impact |
| --- | --- |
| ![GSAP Cinematic preview](asset/previews/gsap-cinematic.gif) | ![Game Impact preview](asset/previews/game-impact.gif) |

| Glitch Cyberpunk | Editorial Scroll |
| --- | --- |
| ![Glitch Cyberpunk preview](asset/previews/glitch-cyberpunk.gif) | ![Editorial Scroll preview](asset/previews/editorial-scroll.gif) |

## What Is This?

`MOTION.md` is a motion design rulebook for AI coding agents like Cursor, Claude Code, and OpenCode.

Instead of asking an AI to "make it animated" and getting generic fades, you give it a concrete motion specification: easing curves, duration tokens, entrance animations, hover states, scroll-triggered behavior, exit transitions, accessibility rules, and anti-patterns.

## Project Structure

```txt
awesome-motion-md/
├── asset/                # Demo GIFs and visual assets
├── motion-md/            # Motion style rulebooks
├── docs/                 # Guides and examples
├── README.md             # English README
└── README.zh-CN.md       # Chinese README
```

## Motion Styles

Motion styles will live in `motion-md/`, with each style as a complete standalone `MOTION.md` rulebook.

Available styles:

```txt
motion-md/
├── material-expressive/MOTION.md
├── apple-fluid/MOTION.md
├── fluent-productive/MOTION.md
├── carbon-enterprise/MOTION.md
├── linear-snappy/MOTION.md
├── stripe-polished/MOTION.md
├── vercel-minimal/MOTION.md
├── framer-spring/MOTION.md
├── gsap-cinematic/MOTION.md
├── game-impact/MOTION.md
├── glitch-cyberpunk/MOTION.md
└── editorial-scroll/MOTION.md
```

| Style | Description |
| --- | --- |
| `material-expressive` | Physics-inspired motion based on Material Design's expressive spring system. |
| `apple-fluid` | Calm, continuous, premium motion inspired by Apple's spatial and direct-manipulation feel. |
| `fluent-productive` | Fast, functional, layered motion for productivity interfaces. |
| `carbon-enterprise` | Precise and accessible motion for complex enterprise products. |
| `linear-snappy` | Ultra-fast SaaS motion with tiny distances and crisp state changes. |
| `stripe-polished` | Refined landing-page motion with depth, stagger, and commercial polish. |
| `vercel-minimal` | Restrained developer-tool motion with subtle dark-mode-friendly effects. |
| `framer-spring` | Spring-first, gesture-aware, layout-native motion patterns. |
| `gsap-cinematic` | Timeline-based cinematic motion for high-impact marketing pages. |
| `game-impact` | Punchy game-like feedback with anticipation, impact, and reward effects. |
| `glitch-cyberpunk` | Neon, scanline, and glitch motion with accessibility safeguards. |
| `editorial-scroll` | Narrative scroll motion for articles, launches, and scrollytelling pages. |

## References

- [`docs/material-motion-reference.md`](docs/material-motion-reference.md): summarized Material Motion guidance used to shape the `material-expressive` style.

## Goal

Make AI-generated interfaces feel intentional, expressive, and alive.
