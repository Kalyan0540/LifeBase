---
type: concept
---

# Custom Variable - Text Output

Sub-concept of [[Custom Variable Creation]]. Shared rules (originals preserved, first-match-wins, no-match behaviour) are documented on the parent page.

Text output custom variables are used to:

- group raw data into readable categories
- simplify crosstab analysis
- create reusable segments

The system works like:

```text
IF condition matches
→ assign a text label
```

## Example — Age Grouping

**Existing variable: Age**

| Respondent | Age |
|---|---|
| R1 | 19 |
| R2 | 22 |
| R3 | 34 |
| R4 | 52 |

### Crosstab BEFORE Custom Variable

`Rows = Brand`, `Columns = Age`

| Brand / Age | 19 | 22 | 34 | 52 |
|---|---|---|---|---|
| Nike   | 1 | 1 | 0 | 0 |
| Adidas | 0 | 0 | 1 | 0 |
| Puma   | 0 | 0 | 0 | 1 |

Problem:

- too many unique values
- difficult to analyze patterns

### Creating the New Variable

**Variable Name:** Age Group

| Rule | Condition | Output Text |
|---|---|---|
| Rule 1 | Age between 18–24 | Young Adult |
| Rule 2 | Age between 25–44 | Adult |
| Rule 3 | Age 45+ | Senior |

### What Happens Internally

The system creates a new column:

| Respondent | Age | Age Group |
|---|---|---|
| R1 | 19 | Young Adult |
| R2 | 22 | Young Adult |
| R3 | 34 | Adult |
| R4 | 52 | Senior |

Important:

- the original Age variable still exists
- the new variable is added separately

### Crosstab AFTER Custom Variable

`Rows = Brand`, `Columns = Age Group`

| Brand | Young Adult | Adult | Senior |
|---|---|---|---|
| Nike   | 2 | 0 | 0 |
| Adidas | 0 | 1 | 0 |
| Puma   | 0 | 0 | 1 |

Result:

- cleaner table
- easier grouping
- easier comparison

## Understanding Key Terms

**Variable Name** — the name of the new variable/column.
Example: `Age Group`.

**Output Text** — the actual category value assigned by a rule.
Examples: `Young Adult`, `Adult`, `Senior`.

## Mental Model

| | |
|---|---|
| Original Variable | Raw survey data |
| Text Custom Variable | Readable grouped categories |

## Common Use Cases

| Use Case | Example |
|---|---|
| Age Grouping | Young Adult / Adult |
| NPS Segments | Promoter / Passive |
| Income Bands | Low / Medium / High |
| Customer Segments | Heavy Buyer |

## Final Understanding

Text output custom variables are mainly used for:

- grouping
- segmentation
- cleaner crosstabs
- readable analysis

They behave like normal categorical variables and can be used in:

- rows
- columns
- filters
- charts

---

*Sources: [[Custom Variable Creation - Text Output]]*
*Updated: 2026-05-20*
