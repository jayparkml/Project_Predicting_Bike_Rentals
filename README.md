# Project_Predicting_Bike_Rentals
This project focus on predicting bike rentals count with machine learning using Linear Regression, Decision Trees, Random Forest.

## 1. Importing Dataset and Libraries
First import the libraries to use and the dataset bike_rental_hour.csv which has information about Washington D.C's bike rentals.
Starting from exploring first 5 rows...
![img](/Images/1.JPG)

Histogram has been generated to show the distribution of bike rentals in total and right skewed distribution was shown.

![img](/Images/2.png)

Next, is to check out the correlation heat map.

![img](/Images/3.png)

And, the correlation table by count

![img](/Images/4.PNG)

With the heat map and table, cnt, registered, and casual is decided to be ignored since they derived from the target value 'cnt'.

Lastly, data is ready to go by dividing and assigning each hours of day to 4 bins : Morning/Afternoon/Evening/Night

![img](/Images/5.PNG)

## 2. Error Metric
80% of data has been used for training and remaining 20% used for testing with random_state of 1 to make sure we can get the result again. And set the training features and target value for models. We decide to check R^2, MSE, and RMSE value for validation of the data.
![img](/Images/6.PNG)
![img](/Images/7.PNG)
