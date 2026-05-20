---
type: concept
---

# Custom Variable - Number Output

Sub-concept of [[Custom Variable Creation]]. Shared rules (originals preserved, first-match-wins, no-match behaviour) are documented on the parent page.

Number output custom variables are used to:

- assign numeric codes / scores
- create numeric categories
- support scoring-based analysis

The system works like:

```text
IF condition matches
→ assign a numeric value
```

## Example — NPS Scoring

**Existing variable: Recommendation Score**

| Respondent | Recommendation Score |
|---|---|
| R1 | 10 |
| R2 | 9  |
| R3 | 7  |
| R4 | 3  |

### Crosstab BEFORE Custom Variable

`Rows = Brand`, `Columns = Recommendation Score`

| Brand / R-Score | 3 | 7 | 9 | 10 |
|---|---|---|---|---|
| Nike   | 0 | 1 | 1 | 1 |
| Adidas | 1 | 0 | 0 | 0 |

Problem:

- raw values are harder to interpret
- users usually want grouped sentiment

### Creating the New Variable

**Variable Name:** NPS Score

| Rule | Condition | Output Number | Meaning |
|---|---|---|---|
| Rule 1 | Score between 9–10 | `100` | Promoter |
| Rule 2 | Score between 7–8  | `0` | Passive |
| Rule 3 | Score between 0–6  | `-100` | Detractor |

### What Happens Internally

The system creates a new column:

| Respondent | Recommendation Score | NPS Score |
|---|---|---|
| R1 | 10 | 100 |
| R2 | 9  | 100 |
| R3 | 7  | 0   |
| R4 | 3  | -100 |

Important:

- the original variable still exists
- the new numeric variable is added separately

## Expected Behaviour

Since the output is numeric, the variable should ideally support:

- Mean
- Average
- Sum
- Score calculations

### Eg: Expected Analytical Output

`Rows = Brand`, `Metric = Mean NPS Score`

| Brand | Mean NPS Score |
|---|---|
| Nike   | 66.7 |
| Adidas | -50 |

## Current: Crosstab AFTER Custom Variable

`Rows = Brand`, `Columns = NPS Score`

| Brand / NPS | -100 | 0 | 100 |
|---|---|---|---|
| Nike   | 0 | 1 | 2 |
| Adidas | 1 | 0 | 0 |

Result:

- grouped sentiment distribution
- easier comparison
- cleaner categorization

## Important Understanding

In this crosstab UI, number outputs mostly behave like:

- coded categories
- grouped buckets

NOT automatically like:

- averages
- metrics
- calculations

## Understanding Key Terms

**Variable Name** — the name of the new variable/column.
Example: `NPS Score`.

**Output Number** — the actual numeric value assigned by a rule.
Examples: `-100`, `0`, `100`.

## Mental Model

| | |
|---|---|
| Original Variable | Raw survey values |
| Number Custom Variable | Numeric-coded categories |

## Common Use Cases

| Use Case | Example |
|---|---|
| NPS Coding | -100 / 0 / 100 |
| Satisfaction Scores | 1 / 2 / 3 / 4 / 5 |
| Risk Levels | 0 / 50 / 100 |
| Ranking Tiers | 1 / 2 / 3 |

## Numbers Still Become Columns

When used as crosstab columns, numeric values behave like categories:

`Columns = NPS Score`

| Brand | -100 | 0 | 100 |
|---|---|---|---|

The numbers act like labels in the table, not metrics.

## Important Clarification

Creating a number output does **not** automatically mean:

- averages
- mean calculations
- score analytics

…because the crosstab structure is still:

```text
Rows × Columns × Counts
```

NOT:

```text
Rows × Metrics
```

## Common Misunderstanding

Users may think:

> "Number output means calculations will happen automatically."

But usually:

- the system is only storing numeric-coded values
- the crosstab still shows distributions

## Difference: Text vs Number Output

| Text Output | Number Output |
|---|---|
| Creates groups | Creates scores |
| Example: `Promoter` | Example: `100` |
| Used for segmentation | Used for calculations |

## Final Understanding

Number output custom variables are mainly used for:

- numeric coding
- grouped score buckets
- standardized scoring
- distribution analysis

---

*Sources: [[Custom Variable Creation - Number Output]]*
*Updated: 2026-05-20*
