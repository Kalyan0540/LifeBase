# Patterns Index

Cross-product pattern registry. One row per distinct pattern. Product columns show which sub-product the pattern has been applied to.

Patterns live in `work/patterns/`. Decisions that originated a pattern live at the sub-product level in `Decisions/`.

---

| Pattern                                         | Description                                                                                                                                  | Catalyst         | Enlyta     | AI  |
| ----------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ---------------- | ---------- | --- |
| [[patterns/Session-Based Destructive Confirmation\|Session-Based Destructive Confirmation]]      | Show a confirmation dialog on the first destructive action in a session, then suppress for subsequent similar actions.                       | AI Summarisation | Cross Tabs | —   |
| [[patterns/Trigger Warnings on Intent, Not Possibility\|Trigger Warnings on Intent, Not Possibility]] | Show warnings only when the user performs a destructive action — not when they enter an editable state where destruction is merely possible. | AI Summarisation | Cross Tabs | —   |

---

*To add a new pattern: create a file in `work/patterns/`, tag it with the relevant products in frontmatter, and add a row here.*
