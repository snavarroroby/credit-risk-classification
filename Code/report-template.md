# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.

The purpose of this analysis is to build a model to predict whether a borrower might be at risk of default based on factors such as loan size, interest rate, the borrower's income and debt-to-income ratio, number of accounts and derogatory marks, and total debt.

* Explain what financial information the data was on, and what you needed to predict.

The data includes financial information such as loan size, interest rate, the borrower's income and debt-to-income ratio, and total debt. The goal is to use these data points to predict whether a loan is "Healthy" (value of 0 inloan status column) or at "high risk" (value of 1 in loan_status column).

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

In the original dataset, 75,036 loans were classified as healthy and 2,500 loans were classified as being at high risk of default based on the values in the loan_status column.

* Describe the stages of the machine learning process you went through as part of this analysis.

We used logistic regression to predict the status of a given loan based on the other fields in the data set as described above. Steps include: 
1. Drop loan_status column from dataset that will be used to train and test the model
2. Instantiate logistic regression model
3. Split data into separate sets for training and testing the model
4. Fit the model to the training data
5. Once the model has been fit to the training data, make predictions for loan status for the loans in the testing data 
6. Compare accuracy of those predictions to the actual known values in the original dataset.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

We used basic Logistic Regression models to predict the value for loan_status based on the other data available. For the second model, we used the RandomOverSampler to oversample data points belonging to the 'High Risk" loan class when constructing the training dataset for the model.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.

• Accuracy: 99%
• Precision (High Risk Loans): 84%
• Precision (Healthy Loans): 100%
• Recall (High Risk Loans): 99%
• Recall (Healthy Loans): 99%

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  
• Accuracy: 99%
• Precision (High Risk Loans): 85%
• Precision (Healthy Loans): 100%
• Recall (High Risk Loans): 91%
• Recall (Healthy Loans): 99%
  


## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

• Machine Learning Model 1:

Overall the model predicted whether a loan was healthy or at high risk of default with 99% accuracy. However, it only predicted whether a loan was high risk with 84% precision (ratio of total predicted high risk loans vs. actual total number of high risk loans), and with 91% recall (ratio of total correctly predicted high risk loans vs. total predicted high risk loans)

• Machine Learning Model 2:

Overall the model predicted whether a loan was healthy or at high risk of default with 99% accuracy. However, it only predicted whether a loan was high risk with 85% precision (ratio of total predicted high risk loans vs. actual total number of high risk loans), and with 91% recall (ratio of total correctly predicted high risk loans vs. total predicted high risk loans)

Model 2 (with oversampling) predicts with slightly higher precision whether a loan should be classified as high-risk (85% precision for Model 2 vs. 84% for Model 1), but with a lower recall (91% for Model 2 vs. 99% for Model 1). Since the difference in precision between the risk level predictions of the two models is so small, Model 1 may be performing slightly better given its higher recall.

