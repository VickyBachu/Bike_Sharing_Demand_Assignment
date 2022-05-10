# Project Name
- Bikes Sharing Demand

# A brief description of project
 A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system. # So, our project is to find the prediction of demand for these shared bikes using a multiple linear regression model.#

## General Information
We are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market.

## Data Preparation:
For data preparation we have to check some of the variables like 'weathersit' and 'season' which have specific labels associated with them. These numeric values associated with the labels may indicate that there is some order to them - which is actually not the case. So, check that we have to convert such feature values into categorical string values before proceeding with model building. For that we have to refer the data dictionary to get a better understanding of all the independent variables. We noticed the column 'yr' with two values 0 and 1 indicating the years 2018 and 2019 respectively. At the first instinct, we think it is a good idea to drop this column as it only has two values so it might not be a value-add to the model. But in reality, since these bike-sharing systems are slowly gaining popularity, the demand for these bikes is increasing every year proving that the column 'yr' might be a good variable for prediction. 

## Model Building
In the dataset provided, we will notice that there are three columns named 'casual', 'registered', and 'cnt'. The variable 'casual' indicates the number casual users who have made a rental. The variable 'registered' on the other hand shows the total number of registered users who have made a booking on a given day. Finally, the 'cnt' variable indicates the total number of bike rentals, including both casual and registered. The model should be built taking this 'cnt' as the target variable.

## Model Evaluation:
When we will be done with model building and residual analysis and have made predictions on the test set, just make sure we used the following two lines of code to calculate the R-squared score on the test set:

from sklearn.metrics import r2_score
r2_score(y_test, y_pred)
where y_test is the test data set for the target variable, and y_pred is the variable containing the predicted values of the target variable on the test set.# Bike_Sharing_Demand_Assignment
