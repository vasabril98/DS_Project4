# HR Promotion Data Model


## Overview of the Analysis
  In this project we use a HR dataset retrieved from Kaggle.com to run a model that predicts employee promotions.  The goals are to see what factors play a role or the most significant roles in employee promotion within this dataset, and to create a model that reaches at least 75% accuracy.  The dataset used contains 13 columns and has features like "awards_won?", "age", "education", and "region" to name a few.  We used Random Forest Classifer for our model and used SMOTE to normalize our data because the the dataset column for "is_promoted" was unbalanced.  We also used a Logistic regression model to optimize the model for more accuracy.
## Instructions

  First we used Pyspark to read in the CSV file with the HR dataset. We Then clean the data by droping unecessary files such as "employee id" and fill nul values with 0 for "previous year rating" and "education columns".  We Then take the columns with catagorical data and use get_dummies to transform the columns to numerical values. From here we split our data into the target variable and features, then we use sklearns Random Forest to run the data through a model.
## Results
* Machine Learning Model 1:
 * Description of Model 1 Accuracy: 91%
 *Precision: 97% for promoted, 87% for not promoted
 *Recall scores: 85.0% for promoted, 96% for not promoted


## Summary


