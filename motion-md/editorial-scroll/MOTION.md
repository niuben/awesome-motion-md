# MOTION.md: Editorial Scroll

## Overview

Editorial Scroll defines narrative motion for articles, reports, launches, explainers, and scrollytelling pages. Use it when motion should guide reading pace and reveal information progressively. The style favors grouped text reveals, subtle image parallax, caption timing, sticky visual moments, and vertical continuity while preserving readability and scroll control.

## Motion Philosophy

Motion should support narrative pacing. Use scroll-based reveals, image parallax, text sequencing, and section transitions to guide attention like an interactive article or magazine feature.

## Core Tokens

| Token | Value | Use |
| --- | --- | --- |
| `--motion-ease-editorial` | `cubic-bezier(0.22, 1, 0.36, 1)` | Reveals |
| `--motion-ease-soft` | `cubic-bezier(0.33, 1, 0.68, 1)` | Image and caption effects |
| `--motion-fast` | `180ms` | Captions and links |
| `--motion-default` | `500ms` | Text blocks |
| `--motion-slow` | `900ms` | Section and image reveals |

## Entrance

- Article header: opacity `0 -> 1`, y `40px -> 0`, `900ms`.
- Paragraph groups: opacity `0 -> 1`, y `24px -> 0`, `500ms`.
- Pull quotes: opacity `0 -> 1`, scale `0.96 -> 1`, `700ms`.
- Images: clip-path reveal or slow scale `1.06 -> 1`, `900ms`.

## Scroll

- Trigger when `25%` of an element enters the viewport.
- Text should reveal in readable groups, not individual letters unless used for a headline.
- Image parallax max offset: `12%` of element height.
- Captions may fade in after image reveal with `120ms` delay.
- Long pages should vary pacing: quiet text sections, then richer visual moments.

## Interaction

- Links: underline draw or color change, `180ms`.
- Image hover: subtle zoom `1.025` and caption emphasis.
- Navigation anchors: smooth scroll allowed unless reduced motion is enabled.

## Transitions

- Section transitions should use vertical continuity.
- Avoid lateral motion unless the story explicitly compares parallel items.
- Sticky visual panels are allowed for scrollytelling.

## Reduced Motion

- Disable parallax, sticky scrub animation, and smooth scroll.
- Use simple opacity reveals or static content.

## Don't

- Do not animate every paragraph independently with long delays.
- Do not make scrolling feel hijacked.
- Do not sacrifice reading speed for visual choreography.

## Agent Instructions

Generate narrative scroll motion with measured pacing, grouped text reveals, subtle image parallax, and strong reading comfort.
