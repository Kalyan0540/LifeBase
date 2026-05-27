---
type: pattern
tags: [Catalyst, Enlyta]
---

# Trigger Warnings on Intent, Not Possibility

> Warnings should appear only when users perform actions with meaningful destructive consequences, not merely when they enter an editable state.

## The Pattern

Show warnings and confirmations only when the user performs a specific destructive action — not when they enter a context where a destructive action is *possible*.

Entering edit mode is not a signal of destructive intent. Users in edit mode may add, rename, or restructure — all non-destructive. Displaying a warning at this point interrupts users who had no harmful intent and creates noise before any action has been taken.

Warnings become meaningful and contextual when they are tied to the moment of destructive intent:
- The user actively tries to delete something with downstream impact.
- The user attempts an action that will remove or alter data used elsewhere.

## When a Passive Banner Makes Sense

A passive banner at entry is appropriate when *entering* the edit state itself has system-wide consequences — for example, if clicking "Edit" immediately locks the record for all other users. In that case, entry is the intent-signal.

If the entry state is neutral and consequences arise only from specific sub-actions, hold the warning until those actions occur.

## Example

In AI Summarisation bucketing:
- Entering the bucketing edit view: no warning shown.
- Adding a new bucket: no warning shown.
- Renaming a bucket: no warning shown.
- Deleting a bucket that is already used in a generated summary: confirmation dialog shown.

---

*Applies to: Catalyst — AI Summarisation · Enlyta — Cross Tabs*
*Sources: [[raw/work/processed/Trigger warnings on intent, not possibility.md]] · [[raw/work/processed/Tabs vs Segemented controls vs Custom tabs.md]]*
*Updated: 2026-05-22*
