# New York Taxi Spending Analysis

## Problem definition
Predict the average money spent on taxi rides for each region of New York per given day and hour.

This problem is a supervised regression problem. Supervised because we have the actual value of the value we’re trying to predict and regression because what we’re trying to predict is a continuous variable (as opposed to categorical).

## Initial Columns

['VendorID', 'tpep_pickup_datetime', 'tpep_dropoff_datetime',
       'passenger_count', 'trip_distance', 'RatecodeID', 'store_and_fwd_flag',
       'PULocationID', 'DOLocationID', 'payment_type', 'fare_amount', 'extra',
       'mta_tax', 'tip_amount', 'tolls_amount', 'improvement_surcharge',
       'total_amount', 'congestion_surcharge', 'airport_fee']
