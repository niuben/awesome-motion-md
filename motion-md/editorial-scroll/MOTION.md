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

## Component Motion

| Component | Motion |
| --- | --- |
| Button | Hover uses underline, color, or gentle y `-1px` over `180ms`; avoid oversized CTA bounce. |
| Card | Reveal as part of reading flow with opacity and y `24px -> 0`, `500ms`; hover may zoom image to `1.025`. |
| Dialog | Use calm overlay fade plus y `20px -> 0`, `500ms`; keep reading position recoverable on close. |
| Popover/Footnote | Fade and rise `8px` from anchor over `180ms`; dismiss without moving surrounding prose. |
| Image lightbox | Expand from image position when possible; fade caption after `120ms`; disable parallax inside modal. |
| Tabs/Comparisons | Use vertical fade or restrained lateral slide only when comparing parallel content. |
| Pull quote | Reveal with opacity and scale `0.96 -> 1`, `700ms`; do not animate every word unless it is a headline moment. |
| Newsletter/Form | Focus states animate color and underline over `180ms`; success message fades in under `500ms`. |
| Table/List | Reveal rows in readable groups, not individually; cap stagger at `180ms` total. |
| Loading | Prefer static placeholders or gentle fade-in; avoid looping motion near body text. |

## Reduced Motion

- Disable parallax, sticky scrub animation, and smooth scroll.
- Use simple opacity reveals or static content.

## Don't

- Do not animate every paragraph independently with long delays.
- Do not make scrolling feel hijacked.
- Do not sacrifice reading speed for visual choreography.

## Agent Instructions

Generate narrative scroll motion with measured pacing, grouped text reveals, subtle image parallax, and strong reading comfort.
