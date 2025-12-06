# Logistic Regression Homework (Using Sex as Group Variable)

We will use the `Wage` dataset from the **ISLR2** package.  
The dataset includes a group variable `sex` (Male/Female) plus other covariates such as `age`, `education`, `race`, and `wage`.

Your goal: Build and interpret logistic regression models predicting whether a worker earns a **high wage**.

---

## 1. Load and Prepare the Data

**Tasks**

1. Load the `Wage` dataset from **ISLR2**.
2. Create a binary outcome variable:

   - `highwage = 1` if wage > 250  
   - `highwage = 0` otherwise

3. Print:
   - First 10 rows  
   - Number of rows and columns  
   - The number of males and females  

4. Compute:
   - Mean of `highwage` for males  
   - Mean of `highwage` for females  
   - Write 2–3 sentences comparing the two groups.

5. Make these plots:
   - Boxplot of wage by sex  
   - Histogram of age (colored by sex)

---

## 2. Create Training and Testing Sets

**Tasks**

1. Use a **70% train / 30% test** split.
2. Report:
   - Number of observations in train and test  
   - Proportion of `highwage = 1` in train and test  
3. Comment on whether the train and test sets look similar in distribution.

---

## 3. Logistic Regression With Sex Only

Fit the model:

$
\text{highwage} \sim \text{sex}
$




## 3. Logistic Regression With Multiple Predictors

Fit the model:

$
\text{highwage} \sim \text{sex} + \text{age} + \text{education}
$

**Tasks**

1. Fit the model using training data.
2. For each predictor (sex, age, each education level), interpret:
   - log-odds meaning  
   - odds ratio meaning  
3. Compare the sex coefficient between the simple model and this multivariable model:
   - Did it shrink or grow?  
   - Discuss potential confounding.  
4. Compute predicted probabilities for:
   - A 30-year-old male with HS education  
   - A 30-year-old female with HS education  
   Write a short comparison.

---

## 5. Model Evaluation on Test Set

**Tasks**

1. Compute predicted probabilities for the **test set**.
2. Convert these probabilities into predicted classes using a threshold of **0.5**.
3. Create a confusion matrix.
4. Compute:
   - Accuracy  
   - Sensitivity  
   - Specificity  
5. Compute and report the ROC AUC.
6. Write 2–3 sentences on how well the model performs.

---

## 6. Odds Ratio for a 10-Year Age Increase

From the multivariable model, let the coefficient for `age` be \(\beta\).

The odds ratio for a 10-year increase is:

\[
e^{10\beta}
\]

**Tasks**

1. Derive this step-by-step:
   - Change in log-odds  
   - Convert to odds  
   - Exponentiate  
2. Compute the numerical value.
3. Interpret in plain English.

---

## 7. (Optional Bonus)

Fit a model with an interaction:

\[
\text{highwage} \sim \text{sex} * \text{education}
\]

**Tasks**

1. Fit the interaction model.
2. Interpret whether education affects males and females differently.
3. Compare AIC of this model with the earlier multivariable model.
4. Write 2–3 sentences about whether the interaction is useful.

---

## End of Homework


