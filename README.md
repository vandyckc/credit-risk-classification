# credit-risk-classification
## Overview of the Analysis

This analysis employs a supervised model used to predict credit-worthiness of loan borrowers. The dependent (y) variable we are trying to predict represents a healthy loan or a loan at high risk of defaulting. A Logistic Regression Model was created and scored using the original data, then the data was resampled using RandomOverSampler to balance it out since a bias exists toward healthy loans in the original data. Another Logistic Regression Model was performed on this resampled data and then re-scored by looking at the balanced_acccuracy_score of the model, a confusion_matrix, a classification_report.

## Results

* Machine Learning Model 1:
    - The balanced accuracy score returned as: 0.9520479254722232
    - Precision score for healthy loans (0): 1.00, high-risk loans(1): 0.85
    - Recall score for healthy loans (0): 0.99, high-risk loans(1): 0.88


* Machine Learning Model 2:
    - The balanced accuracy score returned as: 0.9936781215845847
    - Precision score for healthy loans (0): 1.00, high-risk loans(1): 0.84
    - Recall score for healthy loans (0): 0.99, high-risk loans(1): 0.99

## Summary

The model using oversampled data (Model 2) was acceptably effective at predicting healthy and high-risk loans based on the features of the provided data. We know this because of the model's confusion matrix, as well as its balanced accuracy, precision, and recall scores being comfortably high. The amount of False Negatives generated by the model for high-risk are very low, which is good, however, there were over 100 False Positives generated for healthy loans, which could be problematic. This might be a sound model to start with, but other models should be tested as well for higher reliability.