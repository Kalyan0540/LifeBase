---
type: concept
---

# Tabs vs Custom Tabs

Two visually similar components in AI Summarisation that serve different purposes. Understanding the distinction prevents misuse.

## Tabs

Used for switching between **distinct modes or workflows**.

- Mutually exclusive — one tab active at a time
- Each tab represents a different workflow or editor
- Content structure changes significantly between tabs
- Users stay within one mode to complete a task before switching

**Example:** `Bucketing` | `Custom Logic` — two separate tools for building logic. The interface is different in each mode.

## Custom Tabs

Used for **selecting different contexts or breakdowns** of the same data.

- Represent applied filters or breakdown dimensions
- Content remains structurally the same; only the data changes
- Users toggle quickly to compare different slices
- State is preserved when switching between tabs
- Tabs can be added or removed (closeable with ×)

**Example:** `Aggregate` | `Income Range` | `Income and Age` — the same layout showing different breakdowns of the same data.

## Design Rule

> Use **Custom Tabs** when users are selecting different contexts or breakdowns to view the same data differently.
> Use **Tabs** when users are switching between different ways to build or edit something.

### When to use Custom Tabs (Filters / Breakdowns)

- Users frequently compare multiple breakdowns together
- The underlying layout and components stay the same
- Tabs with close (×) communicate "applied content"
- Enables quick exploration and comparison across slices

### When to use Tabs (Modes / Workflows)

- Each mode has its own distinct interface and capabilities
- Only one mode is used at a time to complete a task
- Users switch between modes, not stack them
- State is preserved when the user returns to a tab

## In AI Summarisation

Bucketing and Custom Logic use **Tabs** (not Segmented Controls, not Custom Tabs). They are two distinct workflows with different tools and intentions. See [[Decisions/Tabs over Segmented Controls|Tabs over Segmented Controls]] for the decision and full comparison.

![[Pasted image 20260522001227.png]]

---

*Sources: [[raw/work/inbox/Tabs vs Segemented controls vs Custom tabs.md]]*
*Updated: 2026-05-22*
