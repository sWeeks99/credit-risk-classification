Credit Risk Classification
Overview of the Analysis
For this analysis, we built a machine learning model to predict the creditworthiness of borrowers based on loan risk. The dataset contained financial information such as:

Loan size
Interest rate
Income
Debt-to-income ratio
Number of accounts
Derogatory marks
Total debt
Loan status
Our goal was to predict whether a borrower would:

Repay the loan (0)
Have a high risk of defaulting (1)
The main variable we aimed to predict was loan_status.

Stages in the Machine Learning Process
Data Preprocessing:
Loaded the CSV data (lending_data.csv) from a local folder.
Label Creation:
Created the labels set (y) from the loan_status column.
Created the features set (X) containing the other columns.
Data Splitting:
Split the data into training and testing datasets using train_test_split to allow the model to learn the patterns and relationships in the data.
Model Training:
Fitted a Logistic Regression model using the training data (X_train and y_train).
The solver parameter was set to 'lbfgs', which is suitable for small to medium-sized datasets.
Prediction:
Saved the predictions on the testing data labels using the testing feature data (X_test) and the fitted model.
Printed out the resulting DataFrame.
Model Evaluation:
Evaluated the model's performance using a confusion matrix and classification report.
Results
Logistic Regression Model
Accuracy: 99%

Precision:

Class 0 (Repaid): 1.00
Class 1 (Defaulted): 0.87
Recall:

Class 0: 1.00
Class 1: 0.89
F1-Score:

Class 0: 1.00
Class 1: 0.88
Support:

Class 0: 18,759 instances
Class 1: 625 instances
Summary
The Logistic Regression model demonstrated excellent overall performance with an accuracy of 99%. It was particularly strong in predicting Class 0 (loans that were repaid), achieving perfect precision, recall, and F1-score. Although the results for Class 1 (defaulted loans) were not perfect, they still showed high performance with a precision of 87% and a recall of 89%.

Recommendation
Given the Logistic Regression model's overall performance, it is suitable for application in a real-world environment, even with the slightly lower precision and recall for Class 1. To further improve the model's performance on predicting defaults, we could explore other models such as Random Forest or Gradient Boosting.
