# Project: The secrets behind popular restaurants

## Introduction
Popularity has become a really important criterion when we make a choice. It also applies to the dining industry. We've always preferred eating in a popular restaurant, as it will guarantee the food quality, dining environment and services, etc. Besides, it is also a good experience to post on social media. This project explores a range of restaurants in Texas based on Foursquare location data, and further, a machine learning method, namely random forest regression, is used to find the factors that the popular restaurants share in common. The result can work as a guide to decision making, especially for restaurant operators and potential investors.

## Data Acquisition and Cleaning
This study uses the location data acquired from Foursquare. The restaurants within a radius of 20 kilometers from three universities in Texas are studied. 
The dependent variable is the rating of a restaurant. The predictors are:
   1. whether this restaurant is verified (binary variables);
   2. distance from the university;
   3. located county (binary variables for each county);
   4. whether there is any delivery provider (binary variables);
   5. Count of photos of this restaurant that are public;
   6. price tier of the restaurant;
   7. count of reviews;
   8. how many people have added the restaurant to their lists.
 After data cleaning, there are 10 columns for predictors and 1 column for the dependent variable. The total number of sample is 145, namely 145 rows.
 The data is divided into two parts, 75% for training and 25% for testing.

## Methodology
#### Random Forest Prediction
Random forest is a widely used machine learning approach to classification, but it also works very well in regression. The main reasons I chose random forest are: 
   1. It is a non-parametric method using decision trees to fit the data, which provides certain extent of nonlineraity. 
   2. Random forest algorithm reduces the correlation between each decision tree by using only part of the predictors for each tree.
   3. It has less hyperparameters to tune.
   4. We can visualize the trees and acquire the importances of each variable.
   
First, a base random forest model is trained. Then a grid search is applied to find the best hyperparameter setting, and the computation time is saved by using "RandomizedSearchCV", which is a cross-validation based hyperparameter tuning function from scikit-learn library.

## Results
#### Accuracy
After getting the best model via hyperparameter tuning, we use the model on the tetsing data. The accuracy is 89.88%.

#### Variable Importance ranking
[Variable Importances](http://url/to/img.png)

## Discussion

## Conclusion
