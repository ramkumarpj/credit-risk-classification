# Credit Risk Report 

## Overview of the Analysis

* The goal is to create a Machine Learning model using historcial lending activity to predict credit worthiness of borrowers.

* Following data points are needed to build this model - loan_size,interest_rate,borrower_income,debt_to_income,num_of_accounts,derogatory_marks,total_debt,loan_status

* 'loan_status' provided in the given data set indicates whether the loan is a 'Healthy loan (0)' or a 'High-risk Loan (1)'

* The data provided in the csv file was loaded into a Pandas DataFrame.

* The data was then split into training and test set.
  - The target column 'loan_status' was pulled into a seried named 'y'
  - All the other features except 'loan_status'  were pulled into a dataframe named 'X'
  - Scikit-Learn 'train_test_split' function was used to split X and y to train and test data sets named X_train, y_train and X_test, y_test.

* Logistic Regression model from Scikit Learn was chosen to train and predict the loan status
  - LogisticRegression model was created using solver named 'lbfgs' and random_state=1
 - LogisticRegression Model created was then fitted using training dataset - X_train and y_train.
  - The model is then used to predict loan_status of test dataset 'X_test'

## Results

* Logistic Regression Model :
    * Classification Report
      - Accuracy (0.99), 
      - Loan Status 0 (Healthy Loan) - Precision (1.00), and Recall (1.00).
      - Loan Status 1 (High-Risk Loan) - Precision (0.87), and Recall (0.89).

## Summary

* The Logistic Regression Model has performed well to predict the Loan Status with an accuracy score of 0.99 as reported in the classification report. 

* The precision and recall score for Loan Status '0' are both 1, which means the model was able to correctly predict 'Healty Loan' labels. 

* The precision and recall score for Loan Status '1' are .87 & .89 respectievely so the model was not able to predict 'High-Risk Loan' as accurate as 'healthy loan' but it still has a good success rate.

**Recommends** Logistics Regression Model for predicting credit worthiness of borrowers
