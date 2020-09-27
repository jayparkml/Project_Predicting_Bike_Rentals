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
### Linear Regression with all features
![img](/Images/8.PNG)
### Linear Regression with low correlation features removed

![img](/Images/9.PNG)

The error increased with features removed. Removing features did not increase the accuracy but R^2 is low to say the model is useful for prediction.
### Decision Tree Regressor

![img](/Images/10.PNG)

Train portion shows that model is overfitted.
### Decision Tree Regressor with min_samples_leaf changed
leaf number changed from between 2 to 10 to see the mean values of the models and generate the graph of RMSE

![img](/Images/11.PNG)

Still the model is overfitted and there is huge difference in RMSE values.
### Decision Tree Regressor with min_samples_split changed
Next step is to change the samples split value. It changed between 3 to 10 to generate the values like above.

![img](/Images/12.PNG)

The RMSE value still tells us that model is overfitted. Decision tends to overfit for this problem.
### Random Forest Regressor
Random forest with estimators between 10 to 100 with 5 increment is tested for the same problem.

![img](/Images/13.PNG)

![img](/Images/14.PNG)

Model still looks overfitted. Next, we tried to tune the parameters as we did for decision trees.
### Random Forest Regressor with min_samples_leaf changed
Used same setting for 2 ~ 10 samples

![img](/Images/15.PNG)

![img](/Images/16.PNG)

### Random Forest Regressor with min_samples_split changed

![img](/Images/17.PNG)

![img](/Images/18.PNG)

## 3. Conclusion
![img](/Images/19.PNG)

It is clear that the Random Forest Regressor have least RMSE values. 
In Decision Trees the experiments in the parameters helped to reduce the RMSE value, however in the Random Forest there was a slightly increase in the values. The feature selection in Linear regression did not help at all.
Some of the models were considered overfitted (if we see the MSE and RMSE) and most of them were impossible to reduce. It's strange that the R2 scores did not show signs of overfit.
