# New York Taxi Spending Analysis

## Problem definition
Predict the average money spent on taxi rides for each region of New York per given day and hour.

This problem is a supervised regression problem. It is a supervised problem because we have the actual values of the values we’re trying to predict. It is a regression problem because what we’re trying to predict is a continuous variable (as opposed to categorical).

## Initial Columns

['VendorID', 'tpep_pickup_datetime', 'tpep_dropoff_datetime',
       'passenger_count', 'trip_distance', 'RatecodeID', 'store_and_fwd_flag',
       'PULocationID', 'DOLocationID', 'payment_type', 'fare_amount', 'extra',
       'mta_tax', 'tip_amount', 'tolls_amount', 'improvement_surcharge',
       'total_amount', 'congestion_surcharge', 'airport_fee']

Some of these columns were not useful for the problem statement, so they were removed.

#### Useful columns

['tpep_pickup_datetime', 'tpep_dropoff_datetime',
       'passenger_count', 'trip_distance', 'RatecodeID','PULocationID', 'DOLocationID', 'payment_type', 'total_amount']

#### Benchmark model

I used DecisionTreeRegressor to set a bench mark score for my model. I used metrics like r squared score, mean squared error and mean absolute error to measure the performace of my model and set a bench mark for future improvements

## Feature Engineering

I added features like "isWeekend" and "isHoliday" to the dataframe as I assumed that these features have an effect on the number of people that would take taxis on a particular day, which in turn affects the total amount made by taxi drivers. 

## Hyper-paramter tuning

I used RandomizedSearchCV to select the best parameters for my model. In order to make a choice on which model to use it on, I compared the results of three differemt models and selected the one with the best metrics. I then used RandomizedSearchCV to select the best parameters and this was my final model

