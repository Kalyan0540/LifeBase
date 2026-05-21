---
type: pattern
tags: [Catalyst, Enlyta]
---

# Session-Based Destructive Confirmation

> Inform once, then trust the user within the current context.

The confirmation acts as an awareness mechanism rather than repeated permission validation.

## Behaviour

**First destructive action in a session:**
- Show a confirmation dialog.
- Communicate downstream impact.
- Allow the user to cancel or proceed.

**After the user confirms:**
- Suppress additional confirmations for similar actions within the same session.
- Allow uninterrupted continuation of the workflow.

**If the user cancels:**
- Continue showing confirmation on future destructive attempts.
- Suppression begins only after a successful acknowledgement.

## Why This Pattern Works

Repeated confirmations for the same action create unnecessary interruption and reduce workflow efficiency. The first confirmation establishes awareness of the impact; after that, the user is assumed to understand the consequence within the current session context. Users performing multiple edits can continue without repeatedly encountering the same modal.

## When to Use Carefully

Avoid or use cautiously when actions:
- Affect multiple users or systems simultaneously.
- Have irreversible consequences.
- Create significant data loss.
- Impact multiple dependent workflows.

In those cases, showing confirmation every time is safer.

This pattern works better when:
- The action is still recoverable or repeatable.
- Users can recreate the same setup again with minimal-to-moderate effort (not moderate-to-high effort).
- The primary impact is additional effort, time, or processing cost rather than permanent loss.

---

*Applies to: Catalyst — AI Summarisation · Enlyta — Cross Tabs*
*Sources: [[raw/work/inbox/Session-Based Destructive Confirmation Pattern.md]]*
*Updated: 2026-05-22*
