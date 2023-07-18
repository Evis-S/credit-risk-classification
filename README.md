# credit-risk-classification
Background

In this Challenge, I used various techniques to train and evaluate a model based on loan risk. I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

*Factors considered in the analysis included data on:

the size of the loan
its interest rate
the borrower's income
the debt to income ratio
the number of accounts the borrower held
derogatory marks against the borrower
the total debt

* Results:
* Logistic Regression Model 1:
 <img width="438" alt="Screenshot 2023-07-17 at 9 44 24 PM" src="https://github.com/Evis-S/credit-risk-classification/assets/125109090/24165dd6-d9b4-4165-8584-822fab72efb9">

The logistic regression model with  these scores indicate excellent performance for '0'(healthy loans) with the precision 1.00 and reasonably good performance for '1' (high-risk loans) with the precision 0.85.
The overall accuracy of the model is 0.99.
The macro-average F1-score, for the model  is 0.94, reflecting good overall performance across both labels.
The weighted average F1-score, considering the class imbalance in the dataset, is 0.99, indicating high accuracy.

Logistic Regression Model 2:
<img width="544" alt="Screenshot 2023-07-17 at 9 46 46 PM" src="https://github.com/Evis-S/credit-risk-classification/assets/125109090/58eef757-411e-47ef-8093-c26d7cd13ba8">

The logistic regression model fit with oversampled  with  these scores indicate excellent performance for '0'(healthy loans) with the precision 1.00 and reasonably good performance for '1' (high-risk loans) with the precision 0.84.
The overall accuracy of the model is 0.99.
The macro-average F1-score, for the model  is 0.95, reflecting good overall performance across both labels.
The weighted average F1-score, considering the class imbalance in the dataset, is 0.99, indicating high accuracy.
