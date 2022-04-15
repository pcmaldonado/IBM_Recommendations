# Recommendation Systems
As part of the <a href="https://www.udacity.com/course/data-scientist-nanodegree--nd025">Udacity Data Scientist Nanodegree Program</a>, this project explores recommendation systems and create article recommendations based on real data from the IBM Watson Studio platform.

### Tools
This project was done using Python 3.9.7, and the following libraries:
 NumPy, Pandas, Matplotlib and Seaborn. 

## Overview
### Exploratory Data Analysis
Before making recommendations, an exploratory data analysis was conducted. From this analysis, we get the following insights:
* The dataset contains 5148 unique users and a total of 45,993 user-article interactions
* Although on average each user interacts with almost 9 articles, 50% of users in the dataset has only interacted with 3 articles or less. The maximum number of user-article interactions is 364.
* There are 1051 articles, of which 714 have had at least one interaction with at least one user.

### Rank-Based Recommendations
To get Rank-Based recommendations we can simply sort articles based on the number of user-interactions that they have. Then, select the *n* top articles to recommend. 

* This method for generating recommendations can be really useful for new users.

### User-User Based Collaborative Filtering
To recommend articles using user-user based collaborative filtering, we need to create a user-item matrix. Then find similar users using dot product, and finally recommend to our user the articles that they have not read but similar users have read.

* This method for generating recommendations allow for more personalized recommendations.

### Matrix Factorization
To be able to test the performance of our predictions, we can generate recommendations based on Singular Value Decomposition (SVD)

* This method for generating recommendations can be tested offline by spliting the data between train and test sets. However, because of the 'Cold Start Problem', it can only be applied on a small number of users (those who are present in both the train and test sets).
