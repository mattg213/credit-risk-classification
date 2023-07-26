# Module 20 Report Template

## Overview of the Analysis

Use various techniques to train and evaluate a model based on loan risk.  The dataset is composed of historic lending data from a peer-to-peer lending services company.  The model will need to identify the creditworthiness of borrowers.

Lending data consists of: loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, and total debt.  From these variables we will predict the loan status - healthy or high risk. 

The data was imported from csv and put into a Pandas DataFrame.  Then separated the y (loan status) from the remaining features (x) in order to split the data into training and testing datasets.  I was then able to create a `LogisticRegression` model and then create a prediction for our loan status variable.  

Evaluated the model's performance by generating a **confusion matrix**:

>[[18679    80]
> [   67   558]]

and a **classification report**:

>              precision    recall  f1-score   support
>
>           0       1.00      1.00      1.00     18759
>           1       0.87      0.89      0.88       625
>
>    accuracy                           0.99     19384
>   macro avg       0.94      0.94      0.94     19384
>weighted avg       0.99      0.99      0.99     19384

## Results

As you can see from the **classification report** the precision and recall of predicting a healthy loan [0] was near perfect.  While the accuracy of predicting a high risk loan [1] was less so at 94%.  Giving a weighted score of 99% for the model.  


## Summary

I believe this model to be a pretty good indicator of healthy loans. Further testing and development could increase the accuracy of it's ability to identiy high risk loans.  
