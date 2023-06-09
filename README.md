# HR Promotion Data Model


## Overview of the Analysis

  In this project we use a HR dataset retrieved from Kaggle.com to run a model that predicts employee promotions.  The goals are to see what factors play a role or the most significant roles in employee promotion within this dataset, and to create a model that reaches at least 75% accuracy.  The dataset used contains 13 columns and has features like "awards_won?", "age", "education", and "region" to name a few.  We used Random Forest Classifer for our model and used SMOTE to normalize our data because the the dataset column for "is_promoted" was unbalanced at 91.48% to 8.52%.  We also used a Logistic regression model to optimize the model for more accuracy.
  
## Instructions
* Steps for running  file:
  - Download HR_predictive_analytics_final.ipynb 
  - Download train.csv file and upload to google drive under content
  - Run file

  First we used Pyspark to read in the CSV file with the HR dataset. We Then clean the data by droping unecessary files such as "employee id" and fill nul values with 0 for "previous year rating" and "education columns".  We Then take the columns with catagorical data and use get_dummies to transform the columns to numerical values. From here we split our data into the target variable and features, then we use sklearns Random Forest to run the data through a model. Then we used Logistic regression to optimize the model and Matplot lib and Tablue to visual the results and dataset exploration.
  
## Results

* Random Forest Model 1:
  - Description of Model 1 Accuracy- 81%
  - Precision- 82% for promoted, 80% for not promoted
  - Recall scores- 79.0% for promoted, 83% for not promoted
  
* Logistic Regession Model 2:
  - Description of Model 2 Accuracy- 88%
  - Precision- 96% for promoted, 82% for not promoted
  - Recall scores- 78.0% for promoted, 97% for not promoted


## Summary
  
   Once the model was run we found that the top 5 features by importance to accuracy were previous year rating, average training score, recruitment channel other, reruitment channel sourcing, and number of trainings.  Logically it makes sense that average training score and number of trainings would influence promotion because it reflects job competency. Previous year rating also makes logical sense because it is a direct indication of recent job performance. Once the dataset was passed through a logistic regession model to optimize it, accuracy increased  form 80% to 88%. The logistic regression model also changed the top 5 to average training score, previous year rating, awards won, length of service, and age. When we filtered the top 5 features through the employees promoted we found that high average trainig scores were the driving force for detrming promotion. Employees who scored 90 or higher on their training  had a 76% chance of getting promoted.
![image](https://github.com/vasabril98/DS_Project4/assets/118862894/79da5c90-c04a-471f-b138-74258e006782)


   
 ## Links: 
 Tablaeu Exploratory Analaysis https://public.tableau.com/app/profile/christopher.cruz1586/viz/HrPredictionAnalysis/HrPredictionAnalysis?publish=yes
![image](https://github.com/vasabril98/DS_Project4/assets/118862894/e3354af6-c41e-4a36-b31e-e73f362fb442)

 Tablaeu Post Ananlysis https://public.tableau.com/app/profile/christopher.cruz1586/viz/HrPredictionAnalysis/HrPredictionAnalysis?publish=yes
 ![image](https://github.com/vasabril98/DS_Project4/assets/118862894/2ad42987-eb77-45fe-b5c0-f7f88ea93ba1)

