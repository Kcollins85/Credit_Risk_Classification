# Credit Risk Classification Analysis

## Purpose of Analysis:

In this module we built a model that can predict loan risk on future borrowers based on their financial status.

In order to do this, we used a historic dataset to train and test the model. 


## Method used for Analysis:

For the analysis, we set our dependant variable (y value) as the loan status to determine if the loan was healthy or at risk.

The remaining fields were then set to be the independant variables (X values) - this included the loan size, interest rate, borrowers income, borrowers debt to income ratio and total debt.  

Using sklean we split the data into training and test sets using the defined dependant and independant variables.  From there we used the logistics regression model and fit the traning data to this model.

Using the fit training data, we then tested the data to make predictions.

Finally, we created a confusion matrix to evaulate the successfulness of the model.

We then redid these steps, but using imbalanced learning to resample data and make the data more balanced. 


## Results

* Logistics Regression Model - using original data:
  	* Balanced Accuracy Score: 0.952047
	* Precision and Recall Scores:
		* Healthy Loan (Low Risk):
		* Precision: 1.00
		* Recall: 0.99
		* Unhealthy Loan (High Risk):
		* Precision: 0.85
		* Recall: 0.91

                            precision    recall  f1-score   support

   Healthy Loan (Low Risk)       1.00      0.99      1.00     18765
Unhealthy Loan (High Risk)       0.85      0.91      0.88       619

                  accuracy                           0.99     19384


* Logistics Regression Model - using resampled data:
	* Balanced Accuracy Score: 0.99367
	* Precision and Recall Scores:
		* Healthy Loan (Low Risk):
		* Precision: 1.00
		* Recall: 0.99
		* Unhealthy Loan (High Risk):
		* Precision: 0.84
		* Recall: 0.99

                              precision    recall  f1-score   support

   Healthy Loan (Low Risk)       1.00      0.99      1.00     18765
Unhealthy Loan (High Risk)       0.84      0.99      0.91       619

                  accuracy                           0.99     19384


## Summary

Comparing the two confusion matrices it appears that the model's performance has improved in terms of recall for the Unhealthy Loan (High Risk) class after using the RandomOverSampler.

In the first confusion matrix, the recall for the Unhealthy Loan (High Risk) class was 0.91, while in the second confusion matrix, the recall for the same class has increased to 0.99. This indicates that the second model is able to correctly identify a higher proportion of actual Unhealthy Loans, which is reflected in the higher recall score.

However, the precision for the Unhealthy Loan (High Risk) class has decreased from 0.85 in the first confusion matrix to 0.84 in the second confusion matrix. This means that the second model may now have slightly more false positives, as reflected in the lower precision score.

Overall, the second confusion matrix with the RandomOverSampler indicates improved recall but slightly lower precision for the Unhealthy Loan (High Risk) class compared to the first confusion matrix. The trade-off between recall and precision needs to be carefully considered to determine if the model would be suitable to a business looking to use.




