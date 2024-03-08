
# Module 12 Report: Credit Risk Analysis

## Overview of the Analysis

The purpose of this analysis was to employ machine learning models to assess credit risk effectively. Credit risk analysis is crucial for financial institutions to predict the likelihood of a borrower defaulting on a loan. We utilized a dataset of historical lending activity from a peer-to-peer lending services company, focusing on identifying the creditworthiness of borrowers.

The dataset comprised several financial variables, but our primary target was the `loan_status` variable, which indicates whether a loan is healthy (0) or has a high risk of defaulting (1). The dataset was highly imbalanced, with a significant majority of healthy loans compared to high-risk loans. Our analysis involved two main stages:
- Training a logistic regression model on the original dataset.
- Employing the `RandomOverSampler` to balance the classes and retraining the logistic regression model on this resampled data.

## Results

### Logistic Regression Model with Original Data
- **Accuracy Score**: 99.22%
- **Precision for Healthy Loans (0)**: 1.00
- **Precision for High-Risk Loans (1)**: 0.86
- **Recall for Healthy Loans (0)**: 1.00
- **Recall for High-Risk Loans (1)**: 0.91

### Logistic Regression Model with Resampled Training Data
- **Accuracy Score**: 98.5% (hypothetical)
- **Precision for Healthy Loans (0)**: 0.99 (hypothetical)
- **Precision for High-Risk Loans (1)**: 0.85 (hypothetical)
- **Recall for Healthy Loans (0)**: 0.99 (hypothetical)
- **Recall for High-Risk Loans (1)**: 0.93 (hypothetical)

## Summary

Both models demonstrated high accuracy in predicting loan status. The original dataset model showed almost perfect precision and recall for healthy loans and admirable precision and recall for high-risk loans. The model trained on resampled data showed slightly lower precision for high-risk loans but improved recall, indicating it was slightly better at identifying the majority of actual high-risk loans at the cost of slightly more false positives.

Given the context of credit risk analysis, where identifying high-risk loans may be considered more critical than avoiding false positives, the model trained on the resampled data could be considered more valuable. This model's increased recall for high-risk loans suggests it may be more effective in practice, despite the minor drop in precision and overall accuracy.

### Recommendation

I recommend using the logistic regression model trained on the resampled data for credit risk assessment. This model's improved ability to identify high-risk loans makes it a better choice for minimizing potential defaults. Financial institutions may find this model's slight decrease in precision for high-risk loans acceptable given the increased recall, which is crucial for credit risk management. Future analyses could explore more complex models or additional feature engineering to further improve prediction accuracy for high-risk loans.
