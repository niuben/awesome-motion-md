# Material Motion Reference

This document summarizes the Material Design motion guidance that should influence `MOTION.md` styles in this repository.

## Core Direction

Material Design's current motion direction favors a physics-based system over fixed easing and duration pairs.

The goal is to make UI motion feel expressive, predictable, fluid, and easy to use.

## Motion Schemes

Material defines two primary motion schemes:

| Scheme | Character | Best For |
| --- | --- | --- |
| Expressive | More opinionated, lively, overshoots final values, adds bounce | Hero moments, key interactions, expressive products |
| Standard | More functional, minimal bounce, eases into final values | Utility-focused products, frequent interactions |

Most motion in one product should use the same scheme. A product may swap schemes for specific hero moments or components.

## Spring Model

Material's physics system is based on springs.

A spring is controlled by:

| Attribute | Meaning |
| --- | --- |
| Stiffness | How quickly the spring moves toward the target |
| Damping | How much bounce or oscillation remains |
| Initial velocity | How fast the element is already moving when animation starts |

Springs are reusable across transitions, gestures, component effects, and interruptions.

## Spring Token Types

Material separates spring tokens by movement type.

| Token Type | Use For | Overshoot? |
| --- | --- | --- |
| Spatial | Position, x/y movement, rotation, scale, size, shape, rounded corners | Yes, especially in expressive schemes |
| Effects | Opacity, color, visual effects | No |

Use spatial tokens when something physically moves or changes geometry. Use effects tokens for properties that should not overshoot.

## Speed Tokens

Each motion scheme has three speeds.

| Speed | Use For |
| --- | --- |
| Fast | Small components, buttons, switches, compact interactions |
| Default | Most component transitions and medium-size changes |
| Slow | Full-screen transitions, large layout changes, content refreshes |

## Web Spring-To-Curve Fallbacks

When actual springs are not available on the web, use cubic-bezier curves that approximate the spring behavior.

| Token | CSS Curve | Duration |
| --- | --- | --- |
| Expressive fast spatial | `cubic-bezier(0.42, 1.67, 0.21, 0.90)` | `350ms` |
| Expressive default spatial | `cubic-bezier(0.38, 1.21, 0.22, 1.00)` | `500ms` |
| Expressive slow spatial | `cubic-bezier(0.39, 1.29, 0.35, 0.98)` | `650ms` |
| Expressive fast effects | `cubic-bezier(0.31, 0.94, 0.34, 1.00)` | `150ms` |
| Expressive default effects | `cubic-bezier(0.34, 0.80, 0.34, 1.00)` | `200ms` |
| Expressive slow effects | `cubic-bezier(0.34, 0.88, 0.34, 1.00)` | `300ms` |
| Standard fast spatial | `cubic-bezier(0.27, 1.06, 0.18, 1.00)` | `350ms` |
| Standard default spatial | `cubic-bezier(0.27, 1.06, 0.18, 1.00)` | `500ms` |
| Standard slow spatial | `cubic-bezier(0.27, 1.06, 0.18, 1.00)` | `750ms` |
| Standard fast effects | `cubic-bezier(0.31, 0.94, 0.34, 1.00)` | `150ms` |
| Standard default effects | `cubic-bezier(0.34, 0.80, 0.34, 1.00)` | `200ms` |
| Standard slow effects | `cubic-bezier(0.34, 0.88, 0.34, 1.00)` | `300ms` |

## Legacy Easing And Duration

Material still documents legacy easing and duration tokens as fallbacks.

| Transition Type | Easing | Duration |
| --- | --- | --- |
| Begin and end on screen | Emphasized | `500ms` |
| Enter the screen | Emphasized decelerate | `400ms` |
| Exit the screen | Emphasized accelerate | `200ms` |
| Standard begin and end | Standard | `300ms` |
| Standard enter | Standard decelerate | `250ms` |
| Standard exit | Standard accelerate | `200ms` |

Useful CSS fallback curves:

| Name | CSS Curve |
| --- | --- |
| Emphasized decelerate | `cubic-bezier(0.05, 0.7, 0.1, 1.0)` |
| Emphasized accelerate | `cubic-bezier(0.3, 0.0, 0.8, 0.15)` |
| Standard | `cubic-bezier(0.2, 0.0, 0.0, 1.0)` |
| Standard decelerate | `cubic-bezier(0.0, 0.0, 0.0, 1.0)` |
| Standard accelerate | `cubic-bezier(0.3, 0.0, 1.0, 1.0)` |

## Duration Scale

| Token | Value | Use |
| --- | --- | --- |
| `short1` | `50ms` | Instant feedback |
| `short2` | `100ms` | Tiny utility transitions |
| `short3` | `150ms` | Small effects |
| `short4` | `200ms` | Selection controls, quick exits |
| `medium1` | `250ms` | Small-to-medium enters |
| `medium2` | `300ms` | Standard utility transitions |
| `medium3` | `350ms` | Fast spatial movement |
| `medium4` | `400ms` | Emphasized enter transitions |
| `long1` | `450ms` | Large component movement |
| `long2` | `500ms` | Container transforms, major transitions |
| `long3` | `550ms` | Large expressive transitions |
| `long4` | `600ms` | Large slow transitions |
| `extra-long1` | `700ms` | Rare ambient transitions |
| `extra-long2` | `800ms` | Rare ambient transitions |
| `extra-long3` | `900ms` | Rare ambient transitions |
| `extra-long4` | `1000ms` | Ambient carousel auto-advance |

## Transition Patterns

| Pattern | Use For | Guidance |
| --- | --- | --- |
| Container transform | Card to detail, search expansion, image gallery, FAB to sheet | Strongest relationship between states; reserve for hero moments |
| Forward and backward | Consecutive hierarchy navigation | Use platform defaults when possible |
| Lateral | Peer content such as tabs, carousels, galleries | Slide content as a group; do not use for hierarchy navigation |
| Top level | Navigation bar, rail, drawer destinations | Use quick fade; do not imply spatial relationship |
| Enter and exit | Dialogs, menus, snackbars, sheets, drawers | Direction should match screen location and spatial model |
| Skeleton loaders | Loading to loaded UI | Stabilize layout with subtle pulsing, then quickly reveal content |

## Good Transition Rules

Good transitions should:

- Follow reduced motion settings.
- Use subtle fades instead of intense motion when reduced motion is enabled.
- Stay consistent across similar interactions.
- Keep layouts stable during loading.
- Avoid jarring jump cuts for normal navigation.
- Maintain a coherent spatial model.
- Move grouped elements along one unified direction.
- Fade old content out before fading new content in.
- Keep frequent transitions simple rather than highly stylized.

## Anti-Patterns

Avoid:

- Applying bouncy expressive motion to every common transition.
- Animating many persistent elements independently.
- Using lateral transitions for hierarchical navigation.
- Using enter/exit sheet-style movement for screen navigation.
- Slow cross-fades that show two transparent layers at once.
- Content popping into place and shifting layout after loading.
- Decorative parallax or shape morphing when reduced motion is enabled.
