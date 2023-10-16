# Data Preprocessing and Logistic Regression for Titanic Dataset

This repository contains code for a simple classification task on the Titanic Spaceship passenger dataset. The goal of this project is to predict whether passengers were transported to their destination or not.

This was a simple project for entertainment purposes which contains 2 attempts:

## The simple approach with no imputers or complex computations. It includes the following steps:

1. **Data Loading**: The code starts by loading the training dataset (`train.csv`) using the Pandas library.

2. **Feature Analysis**: The code provides an initial analysis of the dataset by displaying the first few rows, running descriptive statistics, and showing value counts for some columns.

3. **Feature Engineering**: The "PassengerId" column is split into "group" and "number" to extract potentially meaningful information. The "Name" column, which is deemed not important, is removed from the dataset.

4. **Label Encoding**: The "Transported" and "VIP" columns are label encoded to convert boolean values (True/False) into numerical format (1/0).

5. **Handling Missing Values**: The code handles missing values in the "VIP" column by filling them with the dominant value (False). Missing values in the "Age" column are filled with the median age, and missing values in the "Destination" column are filled with a default value, "TRAPPIST-1e."

6. **Label Encoding (Destination)**: The "Destination" column is label encoded to convert categorical values into numerical format.

7. **Handling Other Missing Values**: Missing values in the columns "RoomService," "FoodCourt," "ShoppingMall," "Spa," and "VRDeck" are filled with their respective column means.

8. **Feature Scaling**: Standard scaling is applied to the entire dataset using the StandardScaler from Scikit-learn.

9. **Train-Test Split**: The training dataset is split into a training set and a test set for model evaluation.

The code uses a simple Logistic Regression model to predict whether passengers were transported or not.
GridSearchCV is used to find the best combination of hyperparameters including the solver, penalty, and regularization parameter (C).

## The Quick Approach notebook performs data preprocessing and logistic regression for the Titanic dataset. It includes the following steps:

1. Importing necessary libraries.
2. Loading the Titanic dataset from a CSV file.
3. Extracting titles from passenger names.
4. Dropping unnecessary columns.
5. Filling missing age values with the mean age of passengers with the same title.
6. Encoding the 'Sex' column.
7. Processing the 'Ticket' column to extract numeric ticket values.
8. Fitting a logistic regression model.
9. Performing hyperparameter tuning using GridSearchCV.
10. Fitting the final logistic regression model with optimized parameters.

You can run this script to preprocess the data, train a logistic regression model, and make predictions on the test dataset.
Please make sure to adjust file paths accordingly when using this script in your environment.
