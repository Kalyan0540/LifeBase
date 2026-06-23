---
type: concept
sources:
  - "[[Figma Design System 2025 - Colour Tokens  Ep 1  Figma Variables Colors|Figma Design System 2025 - Colour Tokens Ep 1]]"
created: 2026-05-07
updated: 2026-05-07
---

# Dark Mode Design

Approach for implementing dark mode colour tokens in a design system. Source: [[Figma Design System 2025 - Colour Tokens  Ep 1  Figma Variables Colors|Figma Design System 2025 - Colour Tokens Ep 1]].

## Shade inversion method

For a basic design system, dark mode colours are derived by inverting the shade scale of light mode primitives:

| Light mode | Dark mode |
|---|---|
| 10 | 100 |
| 20 | 90 |
| 30 | 80 |
| ... | ... |
| 50 | 60 (brand colour loses a bit of brightness, doesn't disappear) |

Works ~95% of the time. The centre of the scale (50) maps to 60 rather than 50 to preserve the brand colour while reducing brightness slightly.

## Why this works

Because usage tokens reference primitives, and the primitive collection has light and dark modes, switching a frame's mode cascades all colours automatically. No per-component dark mode handling needed.

## Static colours

`white` and `black` variables must always be created separately as mode-invariant — they never change regardless of active mode. See [[Colour Token Architecture]].

## Accessibility

Check contrast ratios after applying dark mode. Figma's built-in contrast checker can verify AA / AAA compliance. If a brand colour cannot achieve AAA, AA is an acceptable minimum to maintain brand identity.

## Related pages

- [[Colour Token Architecture]]
- [[Figma Variables]]
- [[Figma Design System 2025 - Colour Tokens  Ep 1  Figma Variables Colors|Figma Design System 2025 - Colour Tokens Ep 1]]
