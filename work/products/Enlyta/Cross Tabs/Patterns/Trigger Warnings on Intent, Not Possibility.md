---
type: pattern
---

# Trigger Warnings on Intent, Not Possibility

Cross Tabs follows this pattern. The decision was made in Catalyst AI Summarisation — see [[Trigger Warnings on Intent, Not Possibility (AI Summarisation Decision)]].

> Warnings should appear only when users perform actions with meaningful destructive consequences, not merely when they enter an editable state.

## The Pattern

Show warnings and confirmations only when the user performs a specific destructive action — not when they enter a context where a destructive action is merely possible.

Entering edit mode is not a signal of intent. Users may add, rename, or restructure — all non-destructive. Displaying a warning at entry interrupts users who had no harmful intent.

Warnings are meaningful when tied to the moment of actual destructive intent: the user actively tries to delete or alter something with downstream impact.

---

*Sources: [[raw/work/inbox/Trigger warnings on intent, not possibility.md]] · [[raw/work/inbox/Tabs vs Segemented controls vs Custom tabs.md]]*
*Updated: 2026-05-22*
