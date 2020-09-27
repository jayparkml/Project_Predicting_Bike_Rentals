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
