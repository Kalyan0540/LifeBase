## Simple Mental Model
Variable output custom variables are useful when values from multiple variables need to be combined into one single analysis variable.

---

# Example

## Existing Variables

| Respondent | Purchased Product | Mobile Brand | Laptop Brand |
|---|---|---|---|
| R1 | Mobile | Apple | — |
| R2 | Laptop | — | Dell |
| R3 | Mobile | Samsung | — |
| R4 | Laptop | — | HP |

---

# Problem

Mobile Brand and Laptop Brand are separate variables.

So analysis becomes split.

Example:

## Columns = Mobile Brand

| Apple | Samsung |
|---|---|
| 1 | 1 |

Only mobile users are included.

---

## Columns = Laptop Brand

| Dell | HP |
|---|---|
| 1 | 1 |

Only laptop users are included.

---

# Creating New Variable

## Variable Name
Purchased Brand

---

## Rules

| Condition                  | Output = Variable |
| -------------------------- | ----------------- |
| Purchased Product = Mobile | Mobile Brand      |
| Purchased Product = Laptop | Laptop Brand      |

---

# What Happens Internally

System creates a NEW column using values from different variables.

| Respondent | Purchased Product | Purchased Brand |
|---|---|---|
| R1 | Mobile | Apple |
| R2 | Laptop | Dell |
| R3 | Mobile | Samsung |
| R4 | Laptop | HP |

Original variables still exist separately.

---

# Crosstab AFTER Custom Variable

## Columns = Purchased Brand

| Apple | Samsung | Dell | HP |
|---|---|---|---|
| 1 | 1 | 1 | 1 |

Now:
- all brands are combined into one variable
- analysis becomes simpler
- one single crosstab can be used

---

# Important Understanding

Text Output:
Assigns fixed labels

Example:
Young Adult

---

Number Output:
Assigns fixed numeric values

Example:
100

---

Variable Output:
Copies values dynamically from different variables

Example:
Apple / Dell / Samsung / HP