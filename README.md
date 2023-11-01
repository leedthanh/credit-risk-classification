# credit-risk-classification

# Split the Data into Training and Testing Sets
Read the lending_data.csv data from the Resources folder into a Pandas DataFrame
![Screen Shot 2023-11-01 at 1 01 14 AM](https://github.com/leedthanh/credit-risk-classification/assets/135544908/63d631f6-fb49-46de-98dc-b2dd844b9a11)

Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
Check the balance of the labels variable (y) by using the value_counts function

![Screen Shot 2023-11-01 at 1 03 05 AM](https://github.com/leedthanh/credit-risk-classification/assets/135544908/996c81b8-9fa6-4b42-b471-55679b34ca83)

labels variable (y) is not balanced so we will need to resample it.
Split the data into training and testing datasets by using train_test_split

# Create a Logistic Regression Model with the Original Data
Fit a logistic regression model by using the training data (X_train and y_train)

![Screen Shot 2023-11-01 at 1 07 11 AM](https://github.com/leedthanh/credit-risk-classification/assets/135544908/e72d7f72-e13f-4eee-8e72-dba96e921eb2)

Save the predictions on the testing data labels by using the testing feature data (X_test) and the fitted model

Evaluate the model’s performance by doing the following:

Calculate the accuracy score of the model.

Accuracy =  0.9520479254722232

Generate a confusion matrix.

[[18663   102]
 [   56   563]]

 
Print the classification report.                     


![Screen Shot 2023-11-01 at 1 09 14 AM](https://github.com/leedthanh/credit-risk-classification/assets/135544908/54cd7211-34a7-4001-98e7-f7a623328d32)


# Write a Credit Risk Analysis Report
The model predict bothe the '0' healthy loan with a 100% accuracy high precision. For label '1' high-risk loan. the precision is .85, indicating that when the model predicts high-risk it is correct 85% of the time. The model also correctly identifies 99% of the 'healthy' loans because the recal is .99 and for high-risk loans the model correctly identifies 91% of the actual high-risk loans. The F1-score show 100% accuracy between precision and recall for '0' healthy loans and 88% for '1' high-risk loans.

# Predict a Logistic Regression Model with Resampled Training Data

Use the RandomOverSampler module from the imbalanced-learn library to resample the data.
resample label 0    56271
1    56271
Name: loan_status, dtype: int64

Use the LogisticRegression classifier and the resampled data to fit the model and make predictions

Evaluate the model’s performance by doing the following

Calculate the accuracy score of the model.
0.9936781215845847

Generate a confusion matrix.

confusion matrix [[18649   116]
 [    4   615]]

Print the classification report.

![Screen Shot 2023-11-01 at 1 12 01 AM](https://github.com/leedthanh/credit-risk-classification/assets/135544908/96de6d70-bf9b-44a5-9797-6fe9f040e118)

# Write a Credit Risk Analysis Report
The logistic regression model fit with oversampled data predict '0' healthy loan with 100% precision which is very likely correct.  The model also correctly identifies 99% given the recall is .99 on healthy loan and the F-1 score is 1 indicated a perfect balanced between precision and recall.  
For label '1' high-risk loan the precision is 84% indicating the model is correct 84% of the time.  recall is 99% and F1-score is 0.91.  overall the model is performing very well for both healthy loan and high-risk-loan.  I would highly recommend the model with fit resampled training data.

