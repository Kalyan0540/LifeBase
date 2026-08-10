---
type: work-product
parent: Catalyst
---

# AI Summarisation

Sub-product of [[Catalyst - Index|Catalyst]]. AI-powered summarisation feature, including backend flag controls for enabling/disabling summarisation on the member side.

## Folders

- `Concepts/` — Product/UX understanding (summarisation behaviour, flag model, member-side flow)
- `Decisions/` — Explicit product/design decisions
- `AI Summarisation - Tasks` — Open, blocked, and completed tasks
- [[Patterns Index]] — Cross-product pattern registry

## Concepts

- [[Tabs vs Custom Tabs]] — When to use Tabs (mode/workflow switching) vs Custom Tabs (context/breakdown selection)

## Decisions

- [[Decisions/Session-Based Destructive Confirmation|Session-Based Destructive Confirmation]] — Show confirmation once per session for destructive actions, then suppress
- [[Decisions/Trigger Warnings on Intent, Not Possibility|Trigger Warnings on Intent, Not Possibility]] — Show warnings on destructive action, not on entering edit mode
- [[Decisions/Tabs over Segmented Controls|Tabs over Segmented Controls]] — Use Tabs (not Segmented Controls) for Bucketing and Custom Logic
- [[Decisions/Zero-Contributor Values in Bucketing and Custom Logic|Zero-Contributor Values in Bucketing and Custom Logic]] — Keep 0-respondent values available during Bucketing and Custom Logic, with warning/indicator

## Patterns

This sub-product applies two work-level patterns — see [[Patterns Index]] for detail:

- [[patterns/Session-Based Destructive Confirmation|Session-Based Destructive Confirmation]]
- [[patterns/Trigger Warnings on Intent, Not Possibility|Trigger Warnings on Intent, Not Possibility]]

---

*Updated: 2026-08-06*
