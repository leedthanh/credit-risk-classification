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

# Write a Credit Risk Analysis Report

