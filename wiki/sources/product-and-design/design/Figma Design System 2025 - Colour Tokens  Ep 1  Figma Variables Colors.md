---
type: source
source_title: "Figma Design System 2025 - Colour Tokens Ep 1"
source_url: "https://www.youtube.com/watch?v=m7kUGmNkPoc"
channel_name: "TD Sunshine"
channel_url: ""
published: ""
duration_seconds: ""
raw_path: "raw/knowledge/product-and-design/design/Figma Design System 2025 - Colour Tokens  Ep 1  Figma Variables Colors.md"
created: 2026-05-07
updated: 2026-05-27
---

# Figma Design System 2025 - Colour Tokens Ep 1

Episode 1 of a series on building a basic design system in Figma using variables and styles. Covers the full colour token setup from primitives to usage tokens, including dark mode.

## Key takeaways

- Start with **colour primitives** — a rainbow palette of base colours with ~10 shades each. Keep saturation and brightness levels consistent across hues so the palette is cohesive.
- Use **HSB** (Hue, Saturation, Brightness) to reason about colour consistency. If any one colour deviates significantly in saturation or brightness, it breaks the palette.
- The **middle shade (50/500)** is your base brand colour; generate lighter and darker shades from there using a plugin like Color Scale Generator.
- **Branded greyscale**: inject a small amount of your brand hue into your grey palette (e.g. 1–5% saturation at your brand hue) to keep it feeling intentional rather than sterile.
- **Dark mode by inversion**: swap shade scales — dark mode 100 = light mode 10, dark mode 90 = light mode 20, etc. Works ~95% of the time for a basic system.
- **Static colours**: always create a `white` and `black` variable that never change between modes. Essential for cases where a colour must remain fixed.

## Token architecture

Three layers of [[Colour Token Architecture]]:

1. **Colour Primitives** — the full rainbow + greyscale palette. Scoped out so they are never directly accessible in design — backend only.
2. **Colour Usage (Background)** — semantic groupings: `background/neutral/primary`, `background/neutral/secondary`, `background/neutral/inverse`, `background/brand`, `background/semantic/{success,warning,error,info}/{subtle,bold}`. Scoped to fill (frame + shape only).
3. **Colour Usage (Text, Icon, Border)** — same grouping pattern, scoped to their respective property types (text, fill/stroke, stroke only).

## Figma-specific workflow

- Use a plugin (e.g. **Color Variables Creator**) to bulk-create primitive variables from named swatches. Name swatches as `blue/10`, `blue/20` etc. to auto-generate grouped collections.
- Manually set up light/dark modes inside the variable collection — no plugin handles this cleanly yet.
- Use **Apply Variable Mode** on a frame to switch between light and dark to preview in real time.
- **Scope variables** to restrict where they appear in the UI: primitives show nowhere; background tokens show in fill; text tokens show in text; border tokens show in stroke.
- Check colour accessibility with Figma's built-in contrast checker. AA is minimum acceptable; AAA preferred but not always achievable while maintaining brand colour.

## Episode roadmap

Next episodes cover: sizing tokens (radius, spacing, padding), typography variables, components (buttons, dropdowns).

## Related pages

- [[Colour Token Architecture]]
- [[Figma Variables]]
- [[Dark Mode Design]]
