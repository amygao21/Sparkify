# Sparkify
udacity data scientist nanodegree sparkify 
Motivation
Project objective: manipulate realistic dataset with Spark to engineer relevant features for predicting churn. 

Background
Sparkify is an imaginary music service similar to Spotify, which recommend music based on users tastes. It is free with advertisements implemented in between songs intervals. If customers upgrade to premium subscription, there will pay a flat monthly rate but without interruptions and could enjoy many other customised features. It is important to monitor the churn rate for Sparkify since its business is based on subscriptions. 

Methodologies
The project is a typical customer churn prediction problem, which have been explored by others. In according to common steps and project structures given, I followed steps below:
Clean and load data: fill the nan values, correct the data types, drop the outliers.
Exploratory Data Analysis: define the churns by label the variable as 1 or 0. Exploratory data to look features’ distributions and correlation with churns.
Feature engineering: Extract customer-behavior-features from ‘page’ interactions, which includes actions whether customer click next song, add new friends and other actions might impact their decision on subscriptions. 
Modelling: I choose logistic regression, linear svm classifier, and random forest classifier to train a baseline model and tuning a better model from best of them. 

Overview of the input dataset: 
The subset I used for this project is 128MB large (1% of the original whole dataset which is 12GB large); it consists of 286,500 records in JSON format, containing the following fields:

Modelling: 
The data set is split to 60% for training and 40% for test. Every model will get Accuracy and F1 score against the test set. However, since the churned users are a fairly small subset, I will use only F1 score as the metric to optimize models.
Here I explore three models with hyperparameters tuning information below:
Logistic Regression: regParam, [0.1, 0.01, 0.001]
Random Forest: numTrees[10, 20], maxDepth[10, 20]
Support Vector Machine: maxIter[5, 10]
Performance results:
1. Logistic Regression: F1 score 0.74, Accuracy 0.78
2. Random Forest: F1 score 0.78, Accuracy 0.80
3. Support Vector Machine: F-1 score of 0.71, Accuracy 0.78
As I optimized based on F1, Random Forest is the best model.


Conclusion:
From this project, I put in practice fundamental data science skills, including data analysis, cleaning, feature engineering, machine learning, pipeline building, model evaluation and fine tuning to improve accuracy and ultimately to solve a real-life problem. 
The model performance could be better and more reliable with larger data size on Spark. The features can also be improved if I explore more possible combinations or make more tweaks on the hyperparameters.


