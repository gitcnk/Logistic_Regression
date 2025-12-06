# Logistic Regression Homework  


Goal: Build and interpret logistic regression models predicting whether a worker earns a **high wage**.

---

## 1. Load and Prepare the Data

**Tasks**

1. Use the following R-code to access the data:
   `income_data = read.csv('https://raw.githubusercontent.com/gitcnk/Data/refs/heads/master/Stat254/Income_data.csv')
`
   
2. Create a binary outcome variable:

   - `highwage = 1` if income > 50K  
   - `highwage = 0` otherwise

2. Print:

   - The number of males and females
   - The number of White and Black employees  

4. Compute:
   - Proportion of `highwage` for Whites  
   - Proportion of `highwage` for Blacks    
   - Write a sentence comparing the two groups.

5. Make these plots:
   - A scatterplot of `highwage`(Y) and `education`(X).
   - Add the fitted logistic curve into this plot.
   - Now modify the plot to incorporate the `race` variable.  Your plot should now have two curves representing the two races.
   


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

$\text{highwage} \sim \text{race} + \text{age} + \text{education} + \text{education}*\text{race}$

**Tasks**

1. Fit the model using training data. *Please use the numerical variable of education not the edication category.*
2. Write down the fitted model for Whites and Blacks separately.

3. Compute predicted probabilities for:
   - A 30-year-old White with HS education  
   - A 30-year-old Black with HS education  
4. Briefly comment on your findings. (one sentence)
5. If you fit the model correctly, you'll see that the interaction term is not *statisitically significant'.  What does this mean in this context.  Don't just say that coefficient is zero, or this is a result of chance.  Relate this to education, race and the response of highwages.
   
6. Compute the ratio of odds between Whites and Blacks. You may ingore the interaction term for this.  Interpret this value in context.
   
7. Compute the ratio in odds for two groups of individuals who differ by 5 years in age. Interpret this value in context.  As before, you may ingore the interaction term for this.

---

## 5. Model Evaluation on Test Set

**Tasks**

1. Compute predicted probabilities for the **test set**.
2. Convert these probabilities into predicted classes (highwage or not) using a threshold of **0.5**.
3. Create our famous 'going-to-the-beach' table!

**Congratulations!**  You just finished the last HW for the semeseter!
---
