

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

# Results:

<img width="624" alt="1" src="https://user-images.githubusercontent.com/92451164/158042593-4881a51b-c050-47b7-ba1d-4da3ac6e393f.png">

First attempt:
hidden node layers: 3
layer 1: 80
layer 2: 30
layer 3: 20
Activation: relu
epochs: 500

<img width="641" alt="2" src="https://user-images.githubusercontent.com/92451164/158042600-fd15cab0-4ecb-4649-9f33-5b15f44ad561.png">

Second attempt:
hidden node layers: 3
layer 1: 100
layer 2: 80
layer 3: 50
activation: tanh
epochs: 1000

<img width="641" alt="2" src="https://user-images.githubusercontent.com/92451164/158042613-4138cf0f-3668-4b85-8b9d-145904809a15.png">

Third attempt: (less is more)
hidden node layers: 1
layer 1: 80
activation: relu
epochs: 100

<img width="646" alt="3" src="https://user-images.githubusercontent.com/92451164/158042619-111342a6-17ae-48a3-914a-92c6a65109a6.png">

Fourth Attempt:
hidden node layers: 1
layer 1: 50
activation: relu
epochs: 100

<img width="661" alt="4" src="https://user-images.githubusercontent.com/92451164/158042625-8aa4b701-0e8a-42cc-812f-b761574f8789.png">

## Summary
None of the models were able to reach an accuracy score of 75%. Using different cut-off points for bucketing some of the feature data (increasing or decreasing the number of buckets) also did not change the outcome. The use of different activation functions similarly did not have an impact on the accuracy.
