# Neural Network Charity Analysis using deep learning neural network.

## Overview of the analysis:

To create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
From Alphabet Soup’s business team, the CSV contains 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

## Results:

### A. Data Preprocessing

#### 1. What variable(s) are considered the target(s) for your model?
In the code we have used target as y = application_df.IS_SUCCESSFUL, since we are checking if the applicants will be successful if funded by Alphabet Soup.

#### 2. What variable(s) are considered to be the features for your 
We have considered the DataFrame application_df droping the column IS_SUCCESSFUL as feature.

#### 3. What variable(s) are neither targets nor features, and should be removed from the input data?
The EIN and NAME columns would be of no help to increase accuracy and hence can be removed.

### B. Compiling, Training, and Evaluating the Model

#### 1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
##### a.  I selected layer 1 - 100 neurons, layer 2 - 60 neurons, layer 3 - 30 neurons, layer 4 - 10 neurons.
##### b.  First and second layer have relu as the activation while third, fourth and output layers have sigmoid as activation layer.
##### c.  Selecting all the above increased the accuracy to 72.85 % 
  
#### 2. Were you able to achieve the target model performance?
I was not able to achieve the target model performance of 75% but was able to increase the accuracy of model from 72.39% to 72.85% 

#### 3. What steps did you take to try and increase model performance?
The accuracy was achieved by dropping additional columns like 'STATUS','SPECIAL_CONSIDERATIONS',increasing the number of neurons, increasing additional third and fourth layers and chaning the activation for second layer to 'relu'.

Below are the screeshots for the accuracy from initial model from deliverable 1 & 2 and accuracy for the optimized model.
![](https://github.com/Akshaya-Kamble/Neural_Network_Charity_Analysis/blob/main/Reference%20Images/Deliverable%201%262%20accuracy.PNG)
![](https://github.com/Akshaya-Kamble/Neural_Network_Charity_Analysis/blob/main/Reference%20Images/optimized.PNG)

## Summary: 

The model is 72.85 % accurate and therefore can predict 72.85% times accurately if applicants will be successful if funded by Alphabet Soup.

A. Since the dataset is large the neural network model has performed better and achieved more accuracy than logistic regression model.

B. The random forest classifier can also be used for the same data as it has achieved a similar accuracy with less time than the neural network model.If we compare both model's predictive accuracy, their output is very similar. Both the random forest and deep learning models were able to predict correctly if applicants will be successful if funded by Alphabet Soup.Although their predictive performance was comparable, their implementation and training times were not—the random forest classifier was able to train on the large dataset and predict values in seconds, while the deep learning model required a couple minutes to train on the tens of thousands of data points.In other words, the random forest model is able to achieve comparable predictive accuracy on large tabular data with less code and faster performance. 
![](https://github.com/Akshaya-Kamble/Neural_Network_Charity_Analysis/blob/main/Reference%20Images/random%20forest.PNG)
