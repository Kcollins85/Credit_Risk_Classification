# Credit Risk Classification Analysis

## Purpose of Analysis:

In this module we are build a model that can predict loan risk on future borrowers based on their financial status.

In order to do this, we use a historic dataset to train and test the model on. 

## Method used for Analysis:

For the analysis, we will set our dependant varilable (y value) as the loan status to determine if the loan is healthy or at risk.

The remaining fields were then set to be the independant variables (X values) - this includes the loan size, interest rate, borrowers income, borrowers debt to income ratio and total debt.  

First off, using sklean we want to split our data into training and test sets using our defined dependant and indepentant variables.  From there we use the logistics regression model and fit the traning data to this model.

Using the fitted trainnig data, we then use the test data to make predictions.

Finally, we create a confusion matrix to evaulate the successfulness of the model.

We then redo these steps, but using imbalanced learning to resample data and make the data more balanced. 


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Logistics Regression Model - using original data:
  * Balanced accuracy Score - 0.952047

                            precision    recall  f1-score   support

   Healthy Loan (Low Risk)       1.00      0.99      1.00     18765
Unhealthy Loan (High Risk)       0.85      0.91      0.88       619

                  accuracy                           0.99     19384
                 macro avg       0.92      0.95      0.94     19384
              weighted avg       0.99      0.99      0.99     19384



* Logistics Regression Model - using resampled data:
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


Comparing the two confusion matrices it appears that the model's performance has improved in terms of recall for the Unhealthy Loan (High Risk) class after using the RandomOverSampler.

In the first confusion matrix, the recall for the Unhealthy Loan (High Risk) class was 0.91, while in the second confusion matrix, the recall for the same class has increased to 0.99. This indicates that the model is now able to correctly identify a higher proportion of actual Unhealthy Loans, which is reflected in the higher recall score.

However, the precision for the Unhealthy Loan (High Risk) class has decreased from 0.85 in the first confusion matrix to 0.84 in the second confusion matrix. This means that the model may now have slightly more false positives, as reflected in the lower precision score.

Overall, the second confusion matrix with the RandomOverSampler indicates improved recall but slightly lower precision for the Unhealthy Loan (High Risk) class compared to the first confusion matrix. The trade-off between recall and precision may need to be carefully considered based on the specific requirements and context of the application in order to determine the model's overall performance.

Given that the overall accuracy and f1-score is above 90% I believe this is a good model and could be recommended to be used.


