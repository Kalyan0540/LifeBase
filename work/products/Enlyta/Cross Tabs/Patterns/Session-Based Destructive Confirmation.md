---
type: pattern
---

# Session-Based Destructive Confirmation

Cross Tabs follows this pattern. The decision was made in Catalyst AI Summarisation — see [[Session-Based Destructive Confirmation (AI Summarisation Decision)]].

> Inform once, then trust the user within the current context.

## Behaviour

**First destructive action in a session:**
- Show a confirmation dialog communicating downstream impact.
- Allow the user to cancel or proceed.

**After the user confirms:**
- Suppress additional confirmations for similar actions in the same session.

**If the user cancels:**
- Continue showing confirmation on future destructive attempts until the user successfully acknowledges.

## When to Use Carefully

Avoid when actions are irreversible, affect multiple users simultaneously, or cause significant data loss. Works best when the user can recover or repeat the action at moderate cost.

---

*Sources: [[raw/work/inbox/Session-Based Destructive Confirmation Pattern.md]]*
*Updated: 2026-05-22*
