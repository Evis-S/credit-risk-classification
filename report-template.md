# Module 20: Report Credit-Risk-Classification


## Overview of the Analysis

* The purpose of this analysis is to generate a model that will be able to correctly identify 'healthy loan' and 'high risk loan' applicants based on application factors.
  
## Factors considered in the analysis included data on:
  
*size of the loan,
* interest rate
*borrower's income
* debt to income ratio
*number of accounts the borrower held
*derogatory marks against the borrower
*the total debt

<img width="850" alt="Screenshot 2023-07-17 at 11 42 46 PM" src="https://github.com/Evis-S/credit-risk-classification/assets/125109090/4b3c2446-2899-4479-afe7-3ea80eb209f3">

Steps: 
* Split the Data into Training and Testing Sets
* 
Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
Split the data into training and testing datasets by using train_test_split.
<img width="540" alt="Screenshot 2023-07-18 at 12 40 04 AM" src="https://github.com/Evis-S/credit-risk-classification/assets/125109090/d68e8f24-9c57-4a79-9598-b2b1716541db">

*Create a Logistic Regression Model 1  with the Original Data
*
Fit a logistic regression model by using the training data (X_train and y_train).
Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
Evaluate the model’s performance by doing the following:
Generate a confusion matrix.
Print the classification report.
<img width="531" alt="Screenshot 2023-07-18 at 12 47 27 AM" src="https://github.com/Evis-S/credit-risk-classification/assets/125109090/658249a4-aed0-4961-aadc-9bee855e3bc9">

*Create a Logistic Regression Model 2  with the  Oversample Data
*
Import RandomOverSampler 
Fit a logistic regression model by using the training data (X_train and y_train).
Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
Evaluate the model’s performance by doing the following:
Generate a confusion matrix.
Print the classification report.

<img width="559" alt="Screenshot 2023-07-18 at 12 57 15 AM" src="https://github.com/Evis-S/credit-risk-classification/assets/125109090/1705536d-c353-4244-9a7f-35adbbdd89dc">




The dataset (77,536 data points) was split into training and testing sets. 
<img width="413" alt="Screenshot 2023-07-17 at 11 42 52 PM" src="https://github.com/Evis-S/credit-risk-classification/assets/125109090/0be72611-e94d-48b3-9040-7dd333160641">


This intial model was drawing from a dataset that had 75,036 healthy  loan data points and 2,500 high-risk data points. To resample the training data and ensure that the logistic regression model had an equal number of data points to draw from, the training set data was resampled with the RandomOverSampler module from imbalanced-learn. This generated 56,277 data points for both healthy loan (0) and high-risk (1) loans, based on the original dataset.


The training set was used to build an initial logistic regression model (Logistic Regression Model 1) using the LogisticRegression module from scikit-learn. 
Logistic Regression Model 1 was then applied to the testing dataset. The purpose of the model was to determine whether a loan to the borrower in the testing set would be healthy or high-risk. The resampled data was used to build a new logistic regression model (Logistic Regression Model 2). The purpose of Logistic Regression Model 2 was to determine whether a loan to the borrower in the testing set would be healthy loan or high-risk loan. 



*** Results:**

Logistic Regression Model 1:

<img width="542" alt="Screenshot 2023-07-17 at 11 42 10 PM" src="https://github.com/Evis-S/credit-risk-classification/assets/125109090/6ac0ddb0-87f9-4591-a379-a26be009abb1">


The logistic regression model with these scores indicate excellent performance for '0'(healthy loans) with the precision 1.00 and reasonably good performance for '1' (high-risk loans) with the precision 0.85. The overall accuracy of the model is 0.99. The macro-average F1-score, for the model is 0.94, reflecting good overall performance across both labels. The weighted average F1-score, considering the class imbalance in the dataset, is 0.99, indicating high accuracy.

*Logistic Regression Model 2:
<img width="635" alt="Screenshot 2023-07-17 at 11 42 29 PM" src="https://github.com/Evis-S/credit-risk-classification/assets/125109090/b490497c-6ee2-48ac-ac6b-4e1be35bf5c0">



The logistic regression model fit with oversampled with these scores indicate excellent performance for '0'(healthy loans) with the precision 1.00 and reasonably good performance for '1' (high-risk loans) with the precision 0.84. The overall accuracy of the model is 0.99. The macro-average F1-score, for the model is 0.95, reflecting good overall performance across both labels. The weighted average F1-score, considering the class imbalance in the dataset, is 0.99, indicating high accuracy.

## Summary
Based on the evaluation metrics, Logistic Regression Model 2, which is fitted with oversampled data, performs slightly better than Model 1. It has a higher precision for the '0' label and a higher macro-average F1-score, indicating better overall performance across both labels. The recall for the '1' label is also higher in Model 2.

* I would recommend using the second model because of its increased ability to accurately detect 'high risk loans'.
 While the first model may have a slightly higher accuracy in identifying 'healthy loans', the cost of misclassifying a 'healthy credit' applicant is generally lower compared to lower compared to the cost of misclassifying a 'loan bad' with 'high risk'. on the other hand, the enhanced ability of the second model to accurately identify 'high-risk loans' exceeds the slightly higher accuracy for 'healthy loans' in the first model.


