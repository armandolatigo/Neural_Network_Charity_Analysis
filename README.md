

## Neural Network Analysis of charity investments
Using TensorFlow to design a neural network that uses binary classification to determine if a charity that receives funding will be successful or not

## Overview
Dataset includes investments in more than 34,000 organizations, including a binary column stating whether or not the money was used effectively. After cleaning the dataset and using sklearn's OneHotEncoder() to standardize the dataset, we're setting the outcome column as the target, with the remaining columns set as features to split the data into train and testing data. We then use sklearn's StandardScaler() and TensorFlow to determine accuracy using different nodes and activation functions.

## Data Processing
The outcome column ('is_successful') was set as the target
The 'EIN' and 'name' columns were removed from the dataset, as they do not aid in analyzing the outcome
The remaining nine columns are the features considered in the analysis
Evaluating the model
Use of different combination of nodes, layers and activation functions to determine whether results can be optimized to achieve 75% accuracy.

Original attempt:
hidden node layers: 3
layer 1: 80
layer 2: 30
activcation: relu
epochs: 100

Result:

[pic]

First attempt:
hidden node layers: 3
layer 1: 80
layer 2: 30
layer 3: 20
Activation: relu
epochs: 500

[pic]

Second attempt:
hidden node layers: 3
layer 1: 100
layer 2: 80
layer 3: 50
activation: tanh
epochs: 1000

[pic]

Third attempt: (less is more)
hidden node layers: 1
layer 1: 80
activation: relu
epochs: 100

[pic]

Fourth Attempt:
hidden node layers: 1
layer 1: 50
activation: relu
epochs: 100

[pic]

## Summary
None of the models were able to reach an accuracy score of 75%. Using different cut-off points for bucketing some of the feature data (increasing or decreasing the number of buckets) also did not change the outcome. The use of different activation functions similarly did not have an impact on the accuracy.