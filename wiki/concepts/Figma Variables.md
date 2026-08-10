---
type: concept
sources:
  - "[[Figma Design System 2025 - Colour Tokens  Ep 1  Figma Variables Colors|Figma Design System 2025 - Colour Tokens Ep 1]]"
  - "[[Going Unitless in Figma - Text Line-heights & letter-spacing]]"
created: 2026-05-07
updated: 2026-07-13
---

# Figma Variables

Figma's native system for storing and reusing values — colours, numbers, strings — across a design file, with support for multiple modes (e.g. light/dark). The mechanism behind [[Colour Token Architecture]].

## Collections and modes

Variables are organised into **collections**. Each collection can have multiple **modes** (e.g. `light` / `dark`). Switching a frame's mode cascades all variables inside it.

In [[Figma Design System 2025 - Colour Tokens  Ep 1  Figma Variables Colors|Figma Design System 2025 - Colour Tokens Ep 1]], two collections are used:
- `color primitives` — base palette (light mode only; dark is handled via inversion)
- `color usage` — semantic usage tokens with light and dark modes

## Scoping

Each variable can be scoped to specific property types — fill, stroke, text, effect. This controls where the variable appears in the design UI. Key practice: scope primitives to nothing (hidden from designers), scope usage tokens to their relevant properties only.

## Creating variables in bulk

Name colour swatches as `hue/shade` (e.g. `purple/50`) before running a bulk-creation plugin. The `/` separator creates nested groups in the variable panel automatically.

## Code Syntax for typography handoff

[[Going Unitless in Figma - Text Line-heights & letter-spacing]] extends variables into typography handoff. Because Figma cannot store unitless line-height values directly in text-style variables, teams can store calculated pixel values and use the variable's Code Syntax field to show the implementation token developers should use.

See [[Unitless Typography Tokens in Figma]].

## Modes and dark mode

No current plugin handles multi-mode setup cleanly. The recommended workflow is: create light mode via plugin, then manually copy values into the dark mode column using the shade-inversion method. See [[Dark Mode Design]].

## Related pages

- [[Colour Token Architecture]]
- [[Figma Design System 2025 - Colour Tokens  Ep 1  Figma Variables Colors|Figma Design System 2025 - Colour Tokens Ep 1]]
- [[Dark Mode Design]]
- [[Unitless Typography Tokens in Figma]]
