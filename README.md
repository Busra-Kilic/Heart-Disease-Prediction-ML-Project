## Heart-Disease-Prediction

This project aims to predict whether individuals are at risk of heart disease using machine learning techniques.We used a dataset available on Kaggle, which you can access [here](https://www.kaggle.com/datasets/mexwell/heart-disease-dataset)
 
#### Data Preparation

In the data preparation phase, we followed the following steps:

###### Exploratory Data Analysis

- There was no missing value problem in the data set. However, since it is not possible for values such as cholesterol, blood pressure and fasting blood sugar to be 0, we considered these variables as missing data. Since the percentage of missing values was around 14%, we filled the missing data with the KNN imputer method instead of deleting them.
- One-hot encoding method was applied to categorical variables and Standard Scaler method to numeric variables.

###### Feature Engineering

- To improve prediction accuracy, we added new features such as New age, New cholesterol, New resting bp s and New max heart rate based on age.
- New max heart rate based on age Represents the person's age-adjusted max heart rate.This variable is calculated by subtracting the person's age from their maximum heart rate.

###### Model Development

In the model development phase, we followed the following steps:

###### Model Selection

	- We tried different algorithms such as Logistic Regression, K-Nearest Neighbors Classifier, Decision Tree Classifier, Random Forest Classifier, SVC, XGB Classifier, CatBoost Classifier, LightGBM Classifier.
	- Before applying these models, we split the dataset into training and testing sets and also used cross-validation techniques.
 
###### Hyperparameter Tuning

- To improve performance, the hyperparameters of the models were adjusted using the Stratified k-fold cross-validation technique.
- For each model, the best performing hyperparameters were identified.
  
#### Model Evaluation

	- The models were evaluated using performance measures such as accuracy, precision, recall and F1-score.
	- The overall performance of the model was visualized using techniques such as confusion matrix and ROC curve.
 
#### Final Model Selection

	- The Catboost model was selected as the best performing model among all models.
	- The selected model was evaluated on the test set and its performance was verified.
 - These steps ensured the successful execution of the project and as a result, we implemented the Catboost model in a web application for users.

#### Web Application

- We have developed a user-friendly web application using Streamlit that offers the following features.
- If the app is asleep due to Streamlit's policy, please wait a few minutes for it to wake up.

As a result, our web app provides a platform for users to discover whether they are at risk of heart disease using machine learning techniques.
