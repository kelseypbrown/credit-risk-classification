# Module 20 Report

## Overview of the Analysis

The analysis aimed to examine the capabilities of a supervised machine learning model for loan candidates. The model was designed to determine if the candidate was a healthy or high-risk loan applicant. It was created using an original data set of over 77,000 candidates. For each of the candidates the following information was given: loan size, interest rate, income, loan debt in relation to income, number of bank accounts, if they have any derogatory marks, their total debt, and loan status (healthy or high-risk). Loan status was separated, 0 for healthy and 1 for high-risk, and a value count was calculated. A large majority was determined healthy (75,036) and the remainder high-risk (2,500). The data was split between training and testing and fit to a logistic regression model. The model predicted the testing data (19,384 random candidates) and the results of the prediction were analyzed using a balanced accuracy score, confusion matrix, and classification report. 

## Results

*Balance accuracy score
    -The model scored 95% on overall accuracy
    
*Confusion Matrix
    -The matrix showed the model correctly identified 18,663 healthy candidates and 563 high-risk candidates. 
    -There were 56 false negatives. Healthy candidates misidentified as high-risk.
    -There were 102 false positives. High-risk candidates misidentified as healthy.
    
*Classification Report
    -For healthy loan candidates: precision of 1.00, recall of 0.99, f1-score of 1.00
    -For high-risk loan candidates: precision of 0.85, recall of 0.91, f1-score of 0.88

## Summary

The results shows the model reliably predicts healthy loan candidates with all scores in the classification report near or at 100%. That being said, the high-risk loan candidates are predicted with slightly less accuracy as there were more of them misidentified (false positives) than the healthy and the high-risk scored lower in each calculation of the report. This result could be due to the imbalanced data set. Originally, only 3% of total candidates were deemed high-risk. The small sample size means that the machine learning model does not have as much data to learn from and cannot perform predictions for those candidates as readily as the healthy loan candidates. However, I would still recommend this model because even the high risk candidates were being identified 85% of the time. The model could further be improved with more high risk data to learn from but can still perform at an acceptable level without. 