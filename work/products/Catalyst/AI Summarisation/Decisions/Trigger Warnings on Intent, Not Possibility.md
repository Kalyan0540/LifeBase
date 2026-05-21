---
type: decision
status: accepted
---

# Trigger Warnings on Intent, Not Possibility

For AI Summarisation, show destructive-action warnings only when the user performs a destructive action — not when they enter edit mode.

## What Was Decided

Two approaches were considered:

1. **Passive warning banner** — show a banner inside the bucketing screen when a variable has been used in a generated summary, alerting the user to modify with caution.
2. **Intent-triggered confirmation** — show a confirmation dialog only when the user performs a specific destructive action (e.g. deleting a bucket already used in summarisation).

**Approach 2 was chosen.**

## Reasoning

Entering edit mode in the bucketing screen is not inherently harmful. Users can perform both destructive and non-destructive actions from the same screen:

- Non-destructive: adding a new bucket, renaming a bucket, adding values to an existing bucket.
- Destructive: deleting a bucket that is already used in AI summarisation.

Showing a warning banner on entry creates unnecessary cognitive noise because the user may not intend to do anything destructive. It also exposes warning information before any user action — the opposite of progressive disclosure.

A passive banner would have made sense if simply entering edit mode itself affected all users or system state. In this flow it does not — impact happens only during specific destructive actions.

**The guiding principle:**
> Warnings should appear only when users perform actions with meaningful destructive consequences, not merely when they enter an editable state.
>
> In short: trigger warnings on intent, not possibility.

## Final Behaviour

- No passive warning banner in the bucketing screen.
- Show confirmation only for destructive actions that affect existing AI summaries (e.g. deleting a bucket used in summarisation).

See [[patterns/Trigger Warnings on Intent, Not Possibility|Trigger Warnings on Intent, Not Possibility]] (pattern) for the generalised form of this behaviour.

---

*Sources: [[raw/work/inbox/Trigger warnings on intent, not possibility.md]] · [[raw/work/inbox/Tabs vs Segemented controls vs Custom tabs.md]]*
*Updated: 2026-05-22*
