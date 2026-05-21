---
type: work-product
parent: Enlyta
---

# Cross Tabs

Sub-product of [[Enlyta - Index|Enlyta]]. A crosstab analysis tool. Current focus is custom variable creation — letting users derive new variables from existing survey variables using condition-to-output rules.

## Folders

- `Concepts/` — Product/UX understanding (features, workflows, behaviours, rules)
- `Decisions/` — Explicit product/design decisions with reasoning and tradeoffs
- `Cross Tabs - Tasks` — Open, blocked, and completed tasks
- [[Patterns Index]] — Cross-product pattern registry

## Concepts

- [[Run and Save Flow]] — Run is mandatory before Save; two distinct confirmation dialogues
- [[Custom Variable Creation]] — Parent overview: rule-based derived variables, shared behaviour, output type comparison
  - [[Custom Variable - Text Output]] — Fixed text labels for segmentation and readable groups
  - [[Custom Variable - Number Output]] — Fixed numeric values; current buckets vs. expected metric behaviour
  - [[Custom Variable - Variable Output]] — Values copied dynamically from other variables (deferred to post-release)

## Decisions

- [[Run Before Save]] — Do not auto-run on save; run is mandatory before save
- [[Variable Creation Scope]] — Output type at variable level; variable output deferred to post-release

## Patterns

This sub-product follows two work-level patterns — see [[Patterns Index]] for detail:

- [[patterns/Session-Based Destructive Confirmation|Session-Based Destructive Confirmation]]
- [[patterns/Trigger Warnings on Intent, Not Possibility|Trigger Warnings on Intent, Not Possibility]]

## Source Notes

- [[Custom Variable Creation - Text Output]]
- [[Custom Variable Creation - Number Output]]
- [[Custom Variable Creation - Variable Output]]

---

*Updated: 2026-05-22*
