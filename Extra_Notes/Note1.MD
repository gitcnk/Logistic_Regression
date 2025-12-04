# Logistic Regression Example


We are studying whether people develop a certain disease (Disease = 1 if yes, 0 if no).  
We have two predictors:

1. **Risk factor (X₁)**: 1 = person has risk factor, 0 = person does not.  
2. **Age (X₂)**: Age in years.  

We want to model the probability of disease as a function of these predictors.

---

## Logistic Regression Model

The logistic regression model is:

$
\log\left(\frac{p}{1-p}\right) = \beta_0 + \beta_1 \text{Risk} + \beta_2 \text{Age}
$

where $(p = P(\text{Disease} = 1 \mid \text{Risk, Age})\).$

Suppose we fit the model and get:

| Coefficient | Estimate |
|------------|----------|
| Intercept ($beta_0$) | -3.0 |
| Risk (\(\beta_1\))      | 1.5  |
| Age (\(\beta_2\))       | 0.05 |

---

## Interpreting Coefficients

### Risk Factor (Binary)
- \(\beta_1 = 1.5\)  
- **Odds ratio (OR)**:

\[
\text{OR} = e^{\beta_1} = e^{1.5} \approx 4.48
\]

**Interpretation**:  
People with the risk factor have about **4.5 times higher odds** of disease than people without the risk factor, **holding age constant**.

### Age (Continuous)
- \(\beta_2 = 0.05\)  
- **OR per year increase**:

\[
\text{OR per year} = e^{0.05} \approx 1.05
\]

**Interpretation**:  
Each additional year of age **increases the odds of disease by about 5%**, holding risk factor constant.

---

## Predicted Probabilities Table

| Risk | Age | Probability | Odds |
|------|-----|------------|------|
| 0    | 30  | 0.182      | 0.223 |
| 0    | 50  | 0.378      | 0.607 |
| 0    | 70  | 0.623      | 1.649 |
| 0    | 75  | 0.668      | 2.012 |
| 0    | 80  | 0.690      | 2.225 |
| 0    | 85  | 0.741      | 2.857 |
| 1    | 30  | 0.500      | 1.0   |
| 1    | 50  | 0.731      | 2.718 |
| 1    | 70  | 0.881      | 7.389 |
| 1    | 75  | 0.905      | 9.500 |
| 1    | 80  | 0.924      | 12.182|
| 1    | 85  | 0.946      | 17.444|

**Notes**:

- Probability rises with age for both risk groups.  
- Having the risk factor shifts the probability curve upward.  
- At very high ages, probabilities approach 1, especially for Risk = 1.

---

## Example Calculation for Probability

For someone with **Risk = 1** and **Age = 50**:

1. Compute log-odds:

\[
\text{log-odds} = -3 + 1.5 \cdot 1 + 0.05 \cdot 50 = 1.0
\]

2. Convert to probability:

\[
p = \frac{e^{1.0}}{1 + e^{1.0}} = \frac{2.718}{1 + 2.718} \approx 0.731
\]

So this person has a **73% chance of disease**.

---

## Summary

- Logistic regression models the **log-odds** of an event.  
- **Exponentiating coefficients gives odds ratios**, which are easier to interpret.  
- Continuous predictors: OR = change in odds per unit increase.  
- Binary predictors: OR = multiplicative change in odds compared to reference category.  
- Use predicted probabilities to **illustrate effects visually** for students.
