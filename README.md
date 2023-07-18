# credit-risk-classification
Background

In this Challenge, I used various techniques to train and evaluate a model based on loan risk. I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

Steps:
Split the Data into Training and Testing Sets
Open the starter code notebook and then use it to complete the following steps.
Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
Note A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
Check the balance of the labels variable (y) by using the value_counts function.
Split the data into training and testing datasets by using train_test_split.
Create a Logistic Regression Model with the Original Data
Employ your knowledge of logistic regression to complete the following steps:
Fit a logistic regression model by using the training data (X_train and y_train).
Save the predictions on the testing data labels by using the testing feature data (X_test) and the fitted model.
Evaluate the model’s performance by doing the following:
Calculate the accuracy score of the model.
Generate a confusion matrix.
Print the classification report.

