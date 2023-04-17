# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
  * The analysis was based on a dataset around loans and if they are approved. We wanted to review this data to determine if we could create a model that would accurately predict if a loan would be risky to a potential borrower based on the requested loan size, borrower income, total debt of the borrower   
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
  * The Y value was the yes or no status of if a loan was approved, we want to predict if this could accurately be predicted based on the values in the X fields.
  * The X values took into account fields such as the loan size, the loan interest rate, the borrowers income and total debt of the borrower.
* Describe the stages of the machine learning process you went through as part of this analysis.
  * 
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
  * 

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  * Balanced accuracy Score - 0.952047


                            precision    recall  f1-score   support

   Healthy Loan (Low Risk)       1.00      0.99      1.00     18765
Unhealthy Loan (High Risk)       0.85      0.91      0.88       619

                  accuracy                           0.99     19384
                 macro avg       0.92      0.95      0.94     19384
              weighted avg       0.99      0.99      0.99     19384



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  * Balanced accuracy Score - 0.99367
  
                            precision    recall  f1-score   support

   Healthy Loan (Low Risk)       1.00      0.99      1.00     18765
Unhealthy Loan (High Risk)       0.84      0.99      0.91       619

                  accuracy                           0.99     19384
                 macro avg       0.92      0.99      0.95     19384
              weighted avg       0.99      0.99      0.99     19384
## Summary

Summarise the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
