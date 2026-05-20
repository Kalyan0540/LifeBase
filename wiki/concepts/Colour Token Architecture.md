---
type: concept
sources: 1
created: 2026-05-07
updated: 2026-05-07
---

# Colour Token Architecture

A two-tier system for organising colour in a design system: **primitives** and **usage tokens**. Described in [[Figma Design System 2025 - Colour Tokens Ep 1]].

## Tier 1 — Colour Primitives

The raw colour palette. A rainbow of base hues plus a branded greyscale, each with ~10 shades.

- Named as `hue/shade` e.g. `blue/10`, `blue/50`, `blue/100`
- The `50` shade is the base/brand colour for that hue; lighter shades go below, darker above
- Saturation and brightness must stay consistent across all hues so the palette is cohesive
- **Scoped out** — never directly accessible in design tools. Backend reference only.

## Tier 2 — Usage Tokens (Colour Usage)

Semantic variables that map to primitives. Organised by property type:

### Background
Groups: `neutral`, `neutral/inverse`, `brand`, `semantic/{success,warning,error,info}`
Each group has `primary`, `secondary`, `tertiary` (and `disabled` for neutral).
Semantic groups have `subtle` and `bold` variants.
Scoped to: fill (frame + shape).

### Text
Mirrors background grouping. Scoped to: text only.

### Icon
Same as text grouping. Scoped to: fill and stroke.

### Border
Simplified grouping: `neutral`, `neutral/inverse`, `brand`, semantics — each with `primary` and `inverse`.
Scoped to: stroke only.

## Dark mode

Achieved at the primitive level by inverting shade scales — dark mode `100` = light mode `10`, dark mode `90` = light mode `20`, etc. Because usage tokens reference primitives, switching modes on a frame cascades automatically. See [[Dark Mode Design]].

## Static colours

Always include `white` and `black` variables that do not change between modes — needed for cases where a colour must remain fixed regardless of theme.

## Related pages

- [[Figma Design System 2025 - Colour Tokens Ep 1]]
- [[Figma Variables]]
- [[Dark Mode Design]]
