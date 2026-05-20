## Simple Mental Model

Text output custom variables are used to:

- group raw data into readable categories
- simplify crosstab analysis
- create reusable segments

The system works like:

IF condition matches  
→ assign a text label

---

# Example 1 — Age Grouping

## Existing Variable: Age

| Respondent | Age |
|---|---|
| R1 | 19 |
| R2 | 22 |
| R3 | 34 |
| R4 | 52 |

---

# Crosstab BEFORE Custom Variable

## Rows = Brand
## Columns = Age

| Brand/Age | 19  | 22  | 34  | 52  |
| --------- | --- | --- | --- | --- |
| Nike      | 1   | 1   | 0   | 0   |
| Adidas    | 0   | 0   | 1   | 0   |
| Puma      | 0   | 0   | 0   | 1   |

Problem:
- too many unique values
- difficult to analyze patterns

---

# Creating New Variable

## Variable Name
Age Group

---

## Rule 1

Condition:
Age between 18–24

Output Text:
Young Adult

---

## Rule 2

Condition:
Age between 25–44

Output Text:
Adult

---

## Rule 3

Condition:
Age 45+

Output Text:
Senior

---

# What Happens Internally

System creates a NEW column:

| Respondent | Age | Age Group |
|---|---|---|
| R1 | 19 | Young Adult |
| R2 | 22 | Young Adult |
| R3 | 34 | Adult |
| R4 | 52 | Senior |

Important:
- original Age variable still exists
- new variable is added separately

---

# Crosstab AFTER Custom Variable

## Rows = Brand
## Columns = Age Group

| Brand | Young Adult | Adult | Senior |
|---|---|---|---|
| Nike | 2 | 0 | 0 |
| Adidas | 0 | 1 | 0 |
| Puma | 0 | 0 | 1 |

Result:
- cleaner table
- easier grouping
- easier comparison

---

# Understanding Key Terms

## Variable Name

Name of the NEW variable/column.

Example:
Age Group

---

## Output Text

The actual category value assigned.

Examples:
- Young Adult
- Adult
- Senior

---

# Mental Model

Original Variable:
Raw survey data

Text Custom Variable:
Readable grouped categories

---

# Common Use Cases

| Use Case | Example |
|---|---|
| Age Grouping | Young Adult / Adult |
| NPS Segments | Promoter / Passive |
| Income Bands | Low / Medium / High |
| Customer Segments | Heavy Buyer |

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

---

# Final Understanding

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