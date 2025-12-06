# Logistic Regression Homework 


Goal: Build and interpret logistic regression models predicting whether a worker earns a **high wage**.

---

## 1. Load and Prepare the Data

**Tasks**

1. Use the following R-code to access the data:
   `income_data = read.csv('')`
   
2. Create a binary outcome variable:

   - `highwage = 1` if wage > 250  
   - `highwage = 0` otherwise

2. Print:
   - First 10 rows  
   - Number of rows and columns  
   - The number of males and females  

4. Compute:
   - Mean of `highwage` for males  
   - Mean of `highwage` for females  
   - Write a sentence comparing the two groups.

5. Make these plots:
   - A scatterplot of `highwage`(Y) and `education`(X).
   - Add the fitted logistic curve into this plot.
   - Now modify the plot to incorporate the `sex` variable.  Your plot should now have two curves representing the two genders.
   


---

## 2. Create Training and Testing Sets

**Tasks**

1. Use a **70% train / 30% test** split. 
2. Report:
   - Number of observations in train and test  
   - Proportion of `highwage = 1` in train and test  
3. Comment on whether the train and test sets look similar in distribution.  What is the purpose of this check?  Think carefully before answering this.

---


## 3. Logistic Regression With Multiple Predictors

Fit the model:

$\text{highwage} \sim \text{sex} + \text{age} + \text{education}$

**Tasks**

1. Fit the model using training data.
2. Write down the fitted model for males and females separately.

3. Compute predicted probabilities for:
   - A 30-year-old male with HS education  
   - A 30-year-old female with HS education  
4. Briefly comment on your findings. (one sentence)

---

## 5. Model Evaluation on Test Set

**Tasks**

1. Compute predicted probabilities for the **test set**.
2. Convert these probabilities into predicted classes using a threshold of **0.5**.
3. Create our famous 'going-to-the-beach' table!

**Congratulations!**  You just finished the last HW for the semeseter!
---
