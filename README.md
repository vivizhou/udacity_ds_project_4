# Udacity Capstone project: User churn prediction using PySpark

## Introduction
This project was one of the Udacity nanodegree Data Science Capstone projects. The motivation was to practice big data manipulation and machine learning using Spark and python.
Churn prediction is to predict which users will unsubscribe from a service based on their behaviors. 
The data analysed in this project is frictional data created by Udacity, which consitsts of user activity record in a music application.

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

## Sorfware version
- Python 3.6.3
- Spark 2.4.3

## Machine learning models
- Logistic Model
- Random Forest Model
- Gradient Boosted Trees Classifier

## Variables selected for prediction
- catagorical variables: gender, user platform, having visited page thumbs down or roll advert or not 
- numerical variables: percentage of use in the first half of the month, percentage of use in the first half of the day, average_itemInSession, average_length, total_length, num_unique_songs, num_unique_artists

## Results
Gradient boosted tree classifier gave the best f1-score (0.75), but the random forest model gave the best accuracy (0.77).

## Copyright
The codes used in this project are free to use.

## Acknowledgement
I would like to thank Udacity for providing the material and platform for practicing this analysis.
