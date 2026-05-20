---
type: concept
---

# Custom Variable - Variable Output

Sub-concept of [[Custom Variable Creation]]. Shared rules (originals preserved, first-match-wins, no-match behaviour) are documented on the parent page.

Variable output custom variables are useful when values from multiple variables need to be combined into one single analysis variable.

The system works like:

```text
IF condition matches
→ copy a value from a selected source variable
```

## Example

**Existing variables**

| Respondent | Purchased Product | Mobile Brand | Laptop Brand |
|---|---|---|---|
| R1 | Mobile | Apple   | — |
| R2 | Laptop | —       | Dell |
| R3 | Mobile | Samsung | — |
| R4 | Laptop | —       | HP |

## The Problem

`Mobile Brand` and `Laptop Brand` are stored as separate variables. Analysis becomes split across the two — neither crosstab shows the full picture.

`Columns = Mobile Brand`

| Apple | Samsung |
|---|---|
| 1 | 1 |

Only mobile users are included.

`Columns = Laptop Brand`

| Dell | HP |
|---|---|
| 1 | 1 |

Only laptop users are included.

## Creating the New Variable

**Variable Name:** Purchased Brand

| Condition | Output (variable) |
|---|---|
| Purchased Product = Mobile | Mobile Brand |
| Purchased Product = Laptop | Laptop Brand |

## What Happens Internally

The system creates a new column by copying values from different source variables:

| Respondent | Purchased Product | Purchased Brand |
|---|---|---|
| R1 | Mobile | Apple |
| R2 | Laptop | Dell |
| R3 | Mobile | Samsung |
| R4 | Laptop | HP |

Original variables (`Mobile Brand`, `Laptop Brand`) still exist separately.

## Crosstab AFTER Custom Variable

`Columns = Purchased Brand`

| Apple | Samsung | Dell | HP |
|---|---|---|---|
| 1 | 1 | 1 | 1 |

Now:

- all brands are combined into one variable
- analysis becomes simpler
- a single crosstab can be used

## Output Mode Comparison

| Mode | What it assigns | Example |
|---|---|---|
| Text Output | Fixed labels | `Young Adult` |
| Number Output | Fixed numeric values | `100` |
| Variable Output | Values copied dynamically from another variable | `Apple` / `Dell` / `Samsung` / `HP` |

---

*Sources: [[Custom Variable Creation - Variable Output]]*
*Updated: 2026-05-20*
