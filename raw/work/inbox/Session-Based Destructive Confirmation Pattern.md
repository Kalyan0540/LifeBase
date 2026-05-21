
# UX Principle

> Inform once, then trust the user within the current context.

The confirmation acts as an awareness mechanism rather than repeated permission validation.

---

# Behaviour

## First Destructive Action

When the user performs a destructive action for the first time in the current session:

- show confirmation dialog
- communicate downstream impact
- allow user to cancel or proceed

---

## After Successful Confirmation

Once the user confirms the action:

- suppress additional confirmations for similar actions in the same session
- allow uninterrupted continuation of the workflow

---

## If User Cancels

If the user cancels the action:

- continue showing confirmation on future destructive attempts
- suppression begins only after successful acknowledgement

---

# Why This Pattern Was Chosen

## Reduces Confirmation Fatigue

Repeated confirmations for the same action create unnecessary interruption and reduce workflow efficiency.

---

## Preserves Workflow Momentum

Users performing multiple edits can continue without repeatedly encountering the same modal.

---

## Maintains Awareness Without Over-Interrupting

The first confirmation establishes awareness of the impact, after which the user is assumed to understand the consequence within the current session context.

---

# Use This Pattern Carefully

This pattern should be avoided or used cautiously when actions:

- affect multiple users or systems simultaneously
- have irreversible consequences
- create significant data loss
- impact multiple dependent workflows

In such cases, showing confirmation every time is safer and more appropriate.

This pattern works better for actions where:

- the action is still recoverable or repeatable
- users can recreate the same setup again with minimal-moderate efforts not for moderate-high efforts
- the primary impact is additional effort, time, or processing cost rather than permanent loss

Used in catalyst AI Summarisation