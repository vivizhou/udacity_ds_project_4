# Udacity Capstone project: User churn prediction using PySpark

## Introduction
This project was one of the Udacity nanodegree Data Science Capstone projects. The motivation was to practice big data manipulation and machine learning using Spark and python.
Churn prediction is to predict which users will unsubscribe from a service based on their behaviors. 
The data analysed in this project is frictional data created by Udacity, which consitsts of user activity record in a music streaming application.
I wrote a blog for this project at Medium: https://medium.com/@vivizhouxw02/churn-prediction-using-pyspark-95907bd9899f.

## File
sparkify.ipynb: the Jupyter notebook of this project.

## Data description
Data Scheme

- artist: (string) The artist that the user listened to
- auth: (string) User login status
- firstName: (string)
- gender: (string)
- itemInSession: (long) the number of items in a session
- lastName: (string)
- length: (double) The duration of the session
- level: (string) Free or paid use
- location: (string) User location 
- method: (string) Get or Put
- page: (string) Visited page
- registration: (long) 
- sessionId: (long)
- song: (string) song name
- status: (long) page status
- ts: (long) Timestamp
- userAgent: (string) User agent
- userId: (string)

## Sorfware and library version
- Python 3.6.3
- Spark 2.4.3
- numpy 1.12.1
- pandas 0.23.3
- matplotlib 2.1.0
- seaborn 0.8.1
- scipy 1.2.1

## Machine learning models
- Logistic Model
- Random Forest Model
- Gradient Boosted Trees Classifier

## Variables selected for prediction
- Catagorical variables: gender, user platform, having visited page thumbs down or roll advert or not 
- Numerical variables: percentage of use in the first half of the month, percentage of use in the first half of the day, average_itemInSession, average_length, total_length, num_unique_songs, num_unique_artists

## Results
Gradient boosted tree classifier gave the best f1-score (0.73) among the three models. The hyperparameter for the gradient boosted tree model was further tuned using cross validation. I analyzed two hyperparameters max_depth and max_bins, and check the average f1 scores of each combination of parameter. maxDepth of 5 and 10 and maxBins of 20 and 32 both gave similar average f1 scores by validation, at around 63%. So the parameters are selected at the setting: maxDepth = 5 and maxBins = 32. This combination gives a f1 score of 73% and accuracy of 76% in the test set. 

## Copyright
The codes used in this project are free to use.

## Acknowledgement
I would like to thank Udacity for providing the material and platform for practicing this analysis.
