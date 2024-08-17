# Module 12 Report Template
Open Jupyter Notebook
Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
Run the boxes to split the data, test it, and create a logistic regression line.
Check the success of the training model with a confusion matrix and classification report.
Analysis available below.

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis: Using seven metrics, including but not limited to loan size, borrower's income, and debt size, the model attempts to predict if these requests for loans will be paid back (healthy), or if the borrower might default on the loan (high-risk).
  
* Explain what financial information the data was on, and what you needed to predict: The focus for this financial information was: the size of the loan, what the interest rate is, the income of the borrower, the borrower's debt-to-income ratio, how many accounts the borrower has, if there have been issues in the past with the borrower, and the borrower's total debt amount.  With this criteria, the end goal was to predict if these metrics could categorize a borrower would be able to pay back a potential loan (healthy), or would default on repaying (high-risk).
   
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`): The dependent variable in this exercise was the y/loan_status.  As a banker or financial institution, it's important to weigh options for loaning money because if a borrower can't or doesn't pay back a loan, if can be costly for the bank.  Because of this, it's essential to analyze the chances of a borrower not paying back a loan.  If someone is a high-risk for the bank, it makes sense financially to deny them a loan.
  
* Describe the stages of the machine learning process you went through as part of this analysis: Because there are so many elements to consider accepting loan applications and humans can think only in 3D, machine learning played a big role in combining and analyzing data to predict loan repayment chances.  To create a more reliable method, it was important to create a training and testing set for the supervised learning.  To do that, I separated the independent variables from the dependent variable and then further divided those into training and testing.  This hopefully removes the chance the machine will "memorize" answers instead of using methodology to predict outcomes when new data is given to the machine.  Once the data is divided into training and testing, I can run a logistic regression line and fit the data to make predictions.  The machine compiles the data and runs the data to create a readable dataframe that can be turned into a visualization or read from the dataframe.


* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms): I used the logistic regression model because there are two finite outcomes: healthy (safe to loan to borrower) or high-risk (borrower should not receive a loan).  Since there are two outcomes and the goal is to find the probability of an event (to loan or not to loan to a borrower), logistic regression works well for this data as it can predict and classify borrowers into the two categories. I also used confusion and classification matrices. This is to check if correct labels were assigned to the input data.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model-logistic regression:
    * Accuracy: 99%.  That means that the number of samples that were classified as either healthy or high-risk out of all the samples in the dataset were almost always labeled correctly.
    * Precision: Healthy loans = 100%; High=risk loans = 87%.  Out of all the predictions that the application was healthy, the model was always correct, which is a great sign.  On the other hand, looking at the false positives (67), there were still issues predicting a high-risk loan application as healthy.  
    * Recall: Healthy loans = 100%; High=risk loans = 89%.  The model continued to do well at predicting if a healthy application was in fact healthy.  However, the false negatives were still 80.  Being at 89% could still be harmful to a financial institution as that's a lot of lost revenue from those loan applications that were incorrectly assigned as healthy.   

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* According to the confusion and classification matrices, the logistic regression model performed quite well when predicting loan applications.  However, with lower scores for predicting high-risk loan applications, I would encourage the use of other models to gather more information.  A ransom forest model might be a good solution as it protects against overfitting because fewer parameters are used.
   
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? ): I think correctly predicting high-risk loans is more important as failure to repay the loan is more detrimental to the financial institution and the borrower.  

If you do not recommend any of the models, please justify your reasoning.
