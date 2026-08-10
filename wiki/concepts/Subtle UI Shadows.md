---
type: concept
sources:
  - "[[Your Figma Drop Shadows Look Cheap (Fix This in 2 Minutes)]]"
created: 2026-07-17
updated: 2026-07-17
---

# Subtle UI Shadows

Subtle UI shadows create separation without making elevation the dominant visual element. In repeated card layouts and dashboards, heavy shadows compound quickly and make the interface look bulky.

## Figma Technique

Use negative spread values to make drop shadows softer and less square.

The source's practical rule is:

- do not rely only on blur radius
- lower opacity when the shadow still dominates
- use negative spread to pull the shadow inward
- review the shadow on multiple adjacent cards

## Design-System Implication

Shadow tokens should be tested in repeated layouts, not only as isolated examples. A shadow that looks acceptable on one object can become noisy across a dashboard grid.

## Links

- [[Your Figma Drop Shadows Look Cheap (Fix This in 2 Minutes)]]
