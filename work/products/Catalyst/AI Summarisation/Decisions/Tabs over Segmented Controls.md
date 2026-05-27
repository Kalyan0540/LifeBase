---
type: decision
status: accepted
---

# Tabs over Segmented Controls for Bucketing and Custom Logic

For AI Summarisation, Bucketing and Custom Logic are presented as Tabs, not as Segmented Controls.

## What Was Decided

Two approaches were considered for the Bucketing / Custom Logic toggle:

1. **Segmented Controls (initial idea)** — Bucketing and Custom Logic as a segmented control within the same view.
2. **Tabs (current approach)** — Bucketing and Custom Logic as separate tabs.

**Tabs were chosen.**

## Reasoning

A full criteria comparison was evaluated:

| Criteria | Segmented Controls | Tabs | Winner |
|---|---|---|---|
| Mental Model | Feels like a toggle/switch within the same view | Clearly communicates different workflows/modes | Tabs |
| Content Change | Entire interface structure changes significantly | Sets right expectation for distinct interfaces | Tabs |
| Scalability | Doesn't scale well if more modes are added | Scales to 3+ workflows in future | Tabs |
| Discoverability | Less obvious that these are separate capabilities | Makes different capabilities explicit | Tabs |
| Industry Convention | Used for small, in-place toggles | Used for switching between distinct tools/views | Tabs |
| User Confidence | May feel like switching a filter, not a mode | Clear expectation of switching workflows | Tabs |

Bucketing and Custom Logic are two distinct workflows with different tools and intentions. Segmented Controls imply a lightweight toggle within a single context; Tabs set the correct expectation that the user is moving between separate editors. Tabs also scale better if additional workflow modes are introduced later.

![[raw/work/assets/Pasted image 20260522001218.png]]

## Final Behaviour

- Bucketing and Custom Logic rendered as Tabs, not Segmented Controls.
- Each tab has its own distinct interface and capabilities.
- State is preserved when switching between tabs.

See [[Tabs vs Custom Tabs]] (concept) for the broader Tabs vs Custom Tabs distinction and when to apply each.

---

*Sources: [[raw/work/processed/Tabs vs Segemented controls vs Custom tabs.md]]*
*Updated: 2026-05-22*
