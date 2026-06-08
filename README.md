# awesome-motion.md

![awesome-motion.md animated logo](asset/logo-motion.svg)

A curated collection of `MOTION.md` files that help AI agents generate stunning, non-boring UI animations.

[中文版](README.zh-CN.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | [العربية](README.ar.md)

## Preview Gallery

Each preview uses the same UI elements, while the visual style and motion behavior are generated from its own `MOTION.md`.

<table width="100%">
  <tr><td width="100%"><strong>Material Expressive</strong><br /><img src="asset/previews/material-expressive.gif" alt="Material Expressive preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Apple Fluid</strong><br /><img src="asset/previews/apple-fluid.gif" alt="Apple Fluid preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Fluent Productive</strong><br /><img src="asset/previews/fluent-productive.gif" alt="Fluent Productive preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Carbon Enterprise</strong><br /><img src="asset/previews/carbon-enterprise.gif" alt="Carbon Enterprise preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Linear Snappy</strong><br /><img src="asset/previews/linear-snappy.gif" alt="Linear Snappy preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Stripe Polished</strong><br /><img src="asset/previews/stripe-polished.gif" alt="Stripe Polished preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Vercel Minimal</strong><br /><img src="asset/previews/vercel-minimal.gif" alt="Vercel Minimal preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Framer Spring</strong><br /><img src="asset/previews/framer-spring.gif" alt="Framer Spring preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>GSAP Cinematic</strong><br /><img src="asset/previews/gsap-cinematic.gif" alt="GSAP Cinematic preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Game Impact</strong><br /><img src="asset/previews/game-impact.gif" alt="Game Impact preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Glitch Cyberpunk</strong><br /><img src="asset/previews/glitch-cyberpunk.gif" alt="Glitch Cyberpunk preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Editorial Scroll</strong><br /><img src="asset/previews/editorial-scroll.gif" alt="Editorial Scroll preview" width="100%" /></td></tr>
</table>

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
├── README.zh-CN.md       # Chinese README
├── README.ja.md          # Japanese README
├── README.ko.md          # Korean README
└── README.ar.md          # Arabic README
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

## Goal

Make AI-generated interfaces feel intentional, expressive, and alive.
