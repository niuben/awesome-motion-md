# MOTION.md: Material Expressive

## Overview

Material Expressive is a physics-inspired motion system for polished product interfaces. Use it when UI should feel alive, fluid, and coherent without becoming chaotic. This style separates spatial motion from visual effects: use spring-like spatial tokens for movement, scale, size, shape, and rotation; use non-overshooting effects tokens for opacity, color, blur, and shadow. It works best for component demos, dashboards, landing pages, and hero interactions that need premium expressiveness with strong accessibility safeguards.

## Motion Philosophy

Create expressive, physics-inspired UI motion that feels alive, fluid, and predictable.

Use spring-like motion as the default mental model. Elements should feel like physical objects moving through a coherent spatial system, not arbitrary layers fading in and out.

This style is best for polished product interfaces, hero interactions, modern app landing pages, dashboards, and component demos that need to feel premium without becoming chaotic.

## Global Motion Scheme

Use the `expressive` scheme by default.

| Scheme | Use |
| --- | --- |
| `expressive` | Default for most components, hero moments, meaningful interactions |
| `standard` | Utility-heavy interactions, dense controls, repeated low-attention transitions |

Most motion on a page must use one scheme. Only swap to `standard` for dense utility components or very frequent interactions.

## Motion Tokens

### Spatial Tokens

Use spatial tokens for movement, rotation, scale, size, shape, and corner radius.

Spatial tokens may overshoot the final value.

| Token | CSS Fallback | Duration | Use |
| --- | --- | --- | --- |
| `motion.spring.fast.spatial` | `cubic-bezier(0.42, 1.67, 0.21, 0.90)` | `350ms` | Buttons, chips, switches, small cards |
| `motion.spring.default.spatial` | `cubic-bezier(0.38, 1.21, 0.22, 1.00)` | `500ms` | Default component movement, panels, medium cards |
| `motion.spring.slow.spatial` | `cubic-bezier(0.39, 1.29, 0.35, 0.98)` | `650ms` | Full-width sections, large sheets, page-level movement |

### Effects Tokens

Use effects tokens for opacity, color, shadow intensity, blur, and filter changes.

Effects tokens must not overshoot.

| Token | CSS Fallback | Duration | Use |
| --- | --- | --- | --- |
| `motion.spring.fast.effects` | `cubic-bezier(0.31, 0.94, 0.34, 1.00)` | `150ms` | Hover color, quick opacity, icon state |
| `motion.spring.default.effects` | `cubic-bezier(0.34, 0.80, 0.34, 1.00)` | `200ms` | Default fade, shadow, surface color |
| `motion.spring.slow.effects` | `cubic-bezier(0.34, 0.88, 0.34, 1.00)` | `300ms` | Large surface opacity, loading reveal |

## CSS Custom Properties

When generating CSS, define these variables at the root:

```css
:root {
  --motion-spatial-fast: cubic-bezier(0.42, 1.67, 0.21, 0.90);
  --motion-spatial-default: cubic-bezier(0.38, 1.21, 0.22, 1.00);
  --motion-spatial-slow: cubic-bezier(0.39, 1.29, 0.35, 0.98);
  --motion-effects-fast: cubic-bezier(0.31, 0.94, 0.34, 1.00);
  --motion-effects-default: cubic-bezier(0.34, 0.80, 0.34, 1.00);
  --motion-effects-slow: cubic-bezier(0.34, 0.88, 0.34, 1.00);
  --motion-duration-spatial-fast: 350ms;
  --motion-duration-spatial-default: 500ms;
  --motion-duration-spatial-slow: 650ms;
  --motion-duration-effects-fast: 150ms;
  --motion-duration-effects-default: 200ms;
  --motion-duration-effects-slow: 300ms;
}
```

## Duration Rules

| Duration | Use |
| --- | --- |
| `50ms` | Press feedback only |
| `100ms` | Tiny utility response |
| `150ms` | Fast effects, small opacity or color changes |
| `200ms` | Default effects, quick exits |
| `300ms` | Slow effects and loading reveals |
| `350ms` | Fast spatial motion for small elements |
| `500ms` | Default spatial motion and expressive transitions |
| `650ms` | Large spatial motion |
| `800ms+` | Ambient decorative motion only |

Scale duration with the size of the transition area. Small components move faster. Large surfaces move slower.

Exit transitions should usually be faster than enter transitions.

## Entrance Animations

### Page And Main Content

Use a clean staged reveal.

- Page container: opacity `0 -> 1`, duration `200ms`, token `motion.spring.default.effects`.
- Main content group: `translateY(24px) -> translateY(0)`, opacity `0 -> 1`, duration `500ms`, token `motion.spring.default.spatial`.
- Avoid animating every element independently on initial load.

### Hero Title

Use expressive spatial motion.

- Transform: `translateY(32px) scale(0.96) -> translateY(0) scale(1)`.
- Opacity: `0 -> 1`.
- Duration: `500ms`.
- Spatial easing: `motion.spring.default.spatial`.
- Effects easing: `motion.spring.default.effects`.

### Cards

Cards should feel like surfaces settling into place.

- Transform: `translateY(28px) scale(0.98) -> translateY(0) scale(1)`.
- Opacity: `0 -> 1`.
- Duration: `500ms`.
- Easing: `motion.spring.default.spatial` for transform, `motion.spring.default.effects` for opacity.
- Stagger: `40ms` per item, maximum total delay `240ms`.

### Buttons And Chips

Use fast spatial motion.

- Transform: `scale(0.92) -> scale(1)`.
- Opacity: `0 -> 1`.
- Duration: `350ms`.
- Easing: `motion.spring.fast.spatial`.

### Images

Images should reveal without heavy bounce.

- Transform: `scale(1.04) -> scale(1)`.
- Opacity: `0 -> 1`.
- Optional filter: `blur(10px) -> blur(0)`.
- Duration: `500ms`.
- Use effects token for opacity and blur.

## Interaction Animations

### Hover

Hover states should be noticeable but not theatrical.

| Element | Motion |
| --- | --- |
| Button | `translateY(-2px) scale(1.02)`, effects duration `150ms`, spatial duration `350ms` |
| Card | `translateY(-6px) scale(1.01)`, shadow or border intensity increases over `200ms` |
| Image card | Image scales to `1.03`, overlay opacity increases over `200ms` |
| Link | Underline or highlight expands over `150ms` |

Do not rotate standard product UI on hover unless the page is explicitly playful or editorial.

### Press

Press feedback must be fast.

- Button press: `scale(0.96)` for `50ms` to `100ms`.
- Card press: `scale(0.985)` for `100ms`.
- Toggle press: move handle with `motion.spring.fast.spatial`.

### Focus

Keyboard focus must be visible.

- Animate outline color or focus ring opacity using `motion.spring.fast.effects`.
- Do not rely on transform-only focus states.

## Scroll-Triggered Motion

Use scroll motion to clarify reading flow, not to decorate every object.

Trigger elements when at least `20%` of the element is visible or when the element is within `80px` of the viewport bottom.

Default reveal:

- Transform: `translateY(32px) -> translateY(0)`.
- Opacity: `0 -> 1`.
- Duration: `500ms`.
- Easing: `motion.spring.default.spatial`.
- Trigger once.

For grids and lists:

- Stagger by DOM order.
- Delay interval: `40ms`.
- Maximum total delay: `240ms`.
- Move items in one unified direction.

Do not apply scroll-triggered entrance motion to sticky headers, fixed navigation, persistent toolbars, or footer legal text.

## Transition Patterns

### Container Transform

Use for hero transitions where an element expands into a detailed state.

Best for cards, images, search boxes, FAB menus, chips, and sheets.

Rules:

- Preserve at least one persistent element between states, such as a container, image, or title.
- Use `motion.spring.default.spatial` or `motion.spring.slow.spatial`.
- Duration: `500ms` for medium transforms, `650ms` for large transforms.
- Avoid using this pattern repeatedly in deep navigation.

### Forward And Backward

Use for navigation between consecutive hierarchy levels.

Rules:

- Prefer platform defaults in native apps.
- On web, use subtle horizontal movement plus clean fade.
- Forward: entering content moves from `24px` right to `0`; exiting content moves `0` to `-12px` with opacity reduction.
- Backward: reverse the direction.
- Duration: `300ms` to `500ms` depending on area.

### Lateral

Use for peer content: tabs, carousels, image galleries.

Rules:

- Move content as a group along the x-axis.
- Do not fade heavily during the slide.
- Duration: `350ms` to `500ms`.
- Do not use for hierarchical navigation.

### Top Level

Use for switching top-level destinations.

Rules:

- Use quick fade out, then fade in.
- Do not imply a spatial relationship between unrelated destinations.
- Exit opacity: `1 -> 0` over `100ms` to `150ms`.
- Enter opacity: `0 -> 1` over `150ms` to `200ms`.
- Avoid lateral slide for navigation bars, rails, and drawers.

### Enter And Exit

Use for dialogs, menus, snackbars, sheets, drawers, tooltips, and banners.

Rules:

- Components should enter from the side of the screen where they logically live.
- Top menu expands downward.
- Snackbar or bottom sheet expands upward from the bottom.
- Navigation drawer enters from the left in left-to-right layouts.
- Avoid using this pattern for full screen hierarchy navigation.

## Exit Animations

Exit motion should require less attention than entrance motion.

| Element | Exit Motion |
| --- | --- |
| Dialog | Opacity `1 -> 0`, scale `1 -> 0.98`, duration `200ms` |
| Menu | Opacity `1 -> 0`, slight collapse on y-axis, duration `150ms` |
| Snackbar | Translate toward screen edge, duration `200ms` |
| Card removal | Fade and collapse space after fade, duration `200ms` |
| Full panel | Slide toward owning edge, duration `300ms` to `500ms` |

Use effects tokens for opacity. Use spatial tokens for movement and size.

## Loading And Skeletons

Use skeleton loaders to keep layout stable while content loads.

Rules:

- Skeletons should match the final layout dimensions.
- Use subtle pulsing, not aggressive shimmer.
- Pulse should move from top-left toward bottom-right when directional motion is used.
- Pulse duration: `1000ms` to `1400ms`.
- Loaded content should fade in quickly over `150ms` to `200ms`.
- Do not let final content pop in and shift layout.

## Reduced Motion

Always support `prefers-reduced-motion: reduce`.

When reduced motion is enabled:

- Replace sliding, scaling, parallax, morphing, and decorative movement with subtle fades.
- Disable shape morphing.
- Disable decorative parallax.
- Disable staggered movement.
- Keep necessary state feedback, but use opacity, color, or outline changes.
- Keep durations at `0ms` to `100ms`.

Use this CSS baseline:

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 1ms !important;
    animation-iteration-count: 1 !important;
    scroll-behavior: auto !important;
    transition-duration: 1ms !important;
  }
}
```

## Performance Rules

Prefer animating:

- `transform`
- `opacity`
- `filter` only when subtle and limited

Avoid animating:

- `top`, `right`, `bottom`, `left`
- `width` and `height` during high-frequency interactions
- expensive blur on large surfaces
- layout-affecting properties during scroll

Use `will-change` sparingly and only shortly before animation starts.

## Do

- Use spatial tokens for motion and effects tokens for opacity or color.
- Scale duration with component size.
- Keep grouped elements moving in one unified direction.
- Use container transforms for meaningful hero moments.
- Use quick, clean fades for top-level destination changes.
- Keep skeleton loading layouts stable.
- Make keyboard focus states visible.

## Don't

- Do not use bouncy spatial motion for every common transition.
- Do not animate many persistent elements independently.
- Do not use lateral transitions for hierarchy navigation.
- Do not use sheet-style enter/exit motion for screen navigation.
- Do not slowly cross-fade two complex screens.
- Do not fade bottom sheets slowly while they slide.
- Do not add scroll-triggered motion to fixed navigation.
- Do not ignore reduced motion settings.

## Agent Instructions

When using this file to generate UI code:

1. Define motion tokens as CSS custom properties.
2. Use spatial tokens for transform-based animations.
3. Use effects tokens for opacity, color, shadow, and filter changes.
4. Implement scroll-triggered reveals with `IntersectionObserver`.
5. Keep motion consistent across similar components.
6. Add reduced-motion fallbacks.
7. Avoid generic `fadeIn` unless the pattern specifically calls for a top-level or reduced-motion fade.
