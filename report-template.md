# Module 20 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

* Factors considered in the analysis included data on:
the size of the loan
its interest rate
the borrower's income
the debt to income ratio
the number of accounts the borrower held
derogatory marks against the borrower
the total debt

<img width="876" alt="Screenshot 2023-07-17 at 9 56 35 PM" src="https://github.com/Evis-S/credit-risk-classification/assets/125109090/0d74f318-b73d-4feb-89ab-3e2051f57ef4">


The dataset (77,536 data points) was split into training and testing sets. 


<img width="388" alt="Screenshot 2023-07-17 at 9 55 50 PM" src="https://github.com/Evis-S/credit-risk-classification/assets/125109090/f06931fa-ba4d-495c-9e37-258a5b07d33c">

The training set was used to build an initial logistic regression model (Logistic Regression Model 1) using the LogisticRegression module from scikit-learn. 
Logistic Regression Model 1 was then applied to the testing dataset. The purpose of the model was to determine whether a loan to the borrower in the testing set would be low- or high-risk and results are summarized below.

This intial model was drawing from a dataset that had 75,036 healthy  loan data points and 2,500 high-risk data points. To resample the training data and ensure that the logistic regression model had an equal number of data points to draw from, the training set data was resampled with the RandomOverSampler module from imbalanced-learn. This generated 56,277 data points for both healthy loan (0) and high-risk (1) loans, based on the original dataset.

The resampled data was used to build a new logistic regression model (Logistic Regression Model 2). The purpose of Logistic Regression Model 2 was to determine whether a loan to the borrower in the testing set would be healthy loan or high-risk loan. The results are summarized below.


*** Results:**

Logistic Regression Model 1:

Screenshot 2023-07-17 at 9 44 24 PM
The logistic regression model with these scores indicate excellent performance for '0'(healthy loans) with the precision 1.00 and reasonably good performance for '1' (high-risk loans) with the precision 0.85. The overall accuracy of the model is 0.99. The macro-average F1-score, for the model is 0.94, reflecting good overall performance across both labels. The weighted average F1-score, considering the class imbalance in the dataset, is 0.99, indicating high accuracy.

*Logistic Regression Model 2:

Screenshot 2023-07-17 at 9 46 46 PM

The logistic regression model fit with oversampled with these scores indicate excellent performance for '0'(healthy loans) with the precision 1.00 and reasonably good performance for '1' (high-risk loans) with the precision 0.84. The overall accuracy of the model is 0.99. The macro-average F1-score, for the model is 0.95, reflecting good overall performance across both labels. The weighted average F1-score, considering the class imbalance in the dataset, is 0.99, indicating high accuracy.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
