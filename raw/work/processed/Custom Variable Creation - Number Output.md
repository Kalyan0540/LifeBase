## Simple Mental Model

Number output custom variables are used to:

- assign numeric codes/scores
- create numeric categories
- support scoring-based analysis

The system works like:

IF condition matches  
→ assign a numeric value

---

# Example 1 — NPS Scoring

## Existing Variable: Recommendation Score

| Respondent | Recommendation Score |
|---|---|
| R1 | 10 |
| R2 | 9 |
| R3 | 7 |
| R4 | 3 |

---

# Crosstab BEFORE Custom Variable

## Rows = Brand
## Columns = Recommendation Score

| Brand/R-Score | 3   | 7   | 9   | 10  |
| ------------- | --- | --- | --- | --- |
| Nike          | 0   | 1   | 1   | 1   |
| Adidas        | 1   | 0   | 0   | 0   |

Problem:
- raw values are harder to interpret
- users usually want grouped sentiment

---

# Creating New Variable

## Variable Name
NPS Score

---

## Rule 1

Condition:
Score between 9–10

Output Number:
100

Meaning:
Promoter

---

## Rule 2

Condition:
Score between 7–8

Output Number:
0

Meaning:
Passive

---

## Rule 3

Condition:
Score between 0–6

Output Number:
-100

Meaning:
Detractor

---

# What Happens Internally

System creates a NEW column:

| Respondent | Recommendation Score | NPS Score |
|---|---|---|
| R1 | 10 | 100 |
| R2 | 9 | 100 |
| R3 | 7 | 0 |
| R4 | 3 | -100 |

Important:
- original variable still exists
- new numeric variable is added separately

---
# Expected Behavior  
  
Since the output is numeric, the variable should ideally support:  
  
- Mean  
- Average  
- Sum  
- Score calculations  
  
---  
  
# Eg: Expected Analytical Output  
  
## Rows = Brand  
## Metric = Mean NPS Score  
  
| Brand | Mean NPS Score |  
|---|---|  
| Nike | 66.7 |  
| Adidas | -50 |  
  
---  
  
# Difference Between Text vs Number Output  
  
| Text Output | Number Output |  
|---|---|  
| Creates groups | Creates scores |  
| Example: Promoter | Example: 100 |  
| Used for segmentation | Used for calculations |

---
# Current: Crosstab AFTER Custom Variable

## Rows = Brand
## Columns = NPS Score

| Brand/NPS | -100 | 0   | 100 |
| --------- | ---- | --- | --- |
| Nike      | 0    | 1   | 2   |
| Adidas    | 1    | 0   | 0   |

Result:
- grouped sentiment distribution
- easier comparison
- cleaner categorization

---

# Important Understanding

In this type of crosstab UI:

Number outputs mostly behave like:
- coded categories
- grouped buckets

NOT automatically like:
- averages
- metrics
- calculations

---

# Understanding Key Terms

## Variable Name

Name of the NEW variable/column.

Example:
NPS Score

---

## Output Number

Actual numeric value assigned.

Examples:
-100
0
100

---

# Mental Model

Original Variable:
Raw survey values

Number Custom Variable:
Numeric-coded categories

---

# Common Use Cases

| Use Case | Example |
|---|---|
| NPS Coding | -100 / 0 / 100 |
| Satisfaction Scores | 1 / 2 / 3 / 4 / 5 |
| Risk Levels | 0 / 50 / 100 |
| Ranking Tiers | 1 / 2 / 3 |

---

# Difference Between Text vs Number Output

| Text Output | Number Output |
|---|---|
| Young Adult | 1 |
| Promoter | 100 |
| High Risk | 3 |

Text:
- readable labels

Number:
- numeric-coded labels

---

# Important Behavior

## Numbers Still Become Columns

Example:

## Columns = NPS Score

| Brand | -100 | 0 | 100 |
|---|---|---|---|

Meaning:
numbers behave like categories in the table.

---

# Important Clarification

Creating number output does NOT automatically mean:

- averages
- mean calculations
- score analytics

because your crosstab structure is still:
Rows × Columns × Counts

NOT:
Rows × Metrics

---

# Common Misunderstanding

Users may think:
"Number output means calculations will happen automatically."

But usually:
- system is only storing numeric-coded values
- crosstab still shows distributions

---

# Important Behavior

## First Match Wins

If multiple rules match:
system usually applies the first matching rule.

---

## No Match

If no condition matches:
system may return:
- blank
- missing
- uncategorized
- null

---

# Final Understanding

Number output custom variables are mainly used for:

- numeric coding
- grouped score buckets
- standardized scoring
- distribution analysis