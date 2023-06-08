# HR Promotion Data Model


## Overview of the Analysis

  In this project we use a HR dataset retrieved from Kaggle.com to run a model that predicts employee promotions.  The goals are to see what factors play a role or the most significant roles in employee promotion within this dataset, and to create a model that reaches at least 75% accuracy.  The dataset used contains 13 columns and has features like "awards_won?", "age", "education", and "region" to name a few.  We used Random Forest Classifer for our model and used SMOTE to normalize our data because the the dataset column for "is_promoted" was unbalanced at 91.48% to 8.52%.  We also used a Logistic regression model to optimize the model for more accuracy.
  
## Instructions

  First we used Pyspark to read in the CSV file with the HR dataset. We Then clean the data by droping unecessary files such as "employee id" and fill nul values with 0 for "previous year rating" and "education columns".  We Then take the columns with catagorical data and use get_dummies to transform the columns to numerical values. From here we split our data into the target variable and features, then we use sklearns Random Forest to run the data through a model.
  
## Results

* Machine Learning Model 1:
  - Description of Model 1 Accuracy- 91%
  - Precision- 97% for promoted, 87% for not promoted
  - Recall scores- 85.0% for promoted, 96% for not promoted


## Summary
  
   Once the model was run we found that the top 5 features by importance to accuracy were average training score, previous year rating, awards won, male gender, and recruitment channel other.  Logically it makes sense that average training score would influence promotion because it reflects job competency. Previous year rating and awards won would indicate recent job performance. Male gender was also a top predictor but it is important to note that the data set was skewed with a 35,295 male count versus a 14,845 female. 

![image](https://github.com/vasabril98/DS_Project4/assets/118862894/e3354af6-c41e-4a36-b31e-e73f362fb442)
