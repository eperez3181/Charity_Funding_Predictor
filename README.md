# Deep-Learning
## Report on the Neural Network Model
Created by: Estela Perez
## Overview
The purpose of this analysis was to help nonprofit foundation Alphabet Soup select the applicants for funding with the best chance of success in their ventures. With my knowledge of machine learning and neural networks, I used the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. 

Alphabet Soup's business team provided me with a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within that dataset are a number of columns that capture metadata about each organization, such as:
* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special consideration for application
* ASK_AMT—Funding amount requested
* IS_SUCCESSFUL—Was the money used effectively

## Results
* ### Data Processing

#### Read in the data
![image](https://user-images.githubusercontent.com/98370960/190320012-0369d2ca-4cb0-4791-816e-108a7d46d11f.png)

#### Dropped the non-beneficial ID columns because they are neither targets nor features
![image](https://user-images.githubusercontent.com/98370960/190320589-9e9d1829-03e6-465b-93cd-10d7b4013b20.png)

#### Determined Target Variable for the model
* IS_SUCCESSFUL

#### Determined Feature Variables for the model:

* APPLICATION_TYPE
* AFFILIATION
* CLASSIFICATION
* USE_CASE
* ORGANIZATION
* STATUS
* INCOME_AMT
* SPECIAL_CONSIDERATIONS
* ASK_AMT

![image](https://user-images.githubusercontent.com/98370960/190341013-cf40164b-d849-4319-9cd6-25c40f936f89.png)
![image](https://user-images.githubusercontent.com/98370960/190341150-98a4e808-4a80-4762-bcad-3b59db7e6993.png)
![image](https://user-images.githubusercontent.com/98370960/190341274-497d3868-1ed7-4267-9b49-befd6b97090c.png)
![image](https://user-images.githubusercontent.com/98370960/190341381-f05a69b2-db5a-44e4-a8bd-0389ae1da132.png)
![image](https://user-images.githubusercontent.com/98370960/190341537-044c68b6-d736-4df1-9f6b-031268ffc7a7.png)
![image](https://user-images.githubusercontent.com/98370960/190341646-a6c14010-c992-4a0c-8159-c9e5c86f6c78.png)
![image](https://user-images.githubusercontent.com/98370960/190341912-e104a89e-d593-418b-b42c-878a64708a50.png)
![image](https://user-images.githubusercontent.com/98370960/190342080-c8f9533d-b208-4bd0-8a74-8d9fc4b08c79.png)

* ### Compiling, Training, and Evaluating the Model

The model was built with the following parameters with low computation time in mind:

The input (node) feature was 43, and after many trials, the best decision for my model was 2 hidden layers with 80, 45 neurons split - with a hidden layer activation function of relu.

Output node is 1 as it was binary classifier model with only one output: was the funding application succesfull yes or no. The output layer activation of sigmoid was used since the model output is binary classification between 0 and 1.

In order to gain a lower loss and higher accuracy, I made a decision to add a 3rd layer with 35 neurons:

![image](https://user-images.githubusercontent.com/98370960/190488231-b8cd4185-bba0-45cb-afd6-f9786d806099.png)
![image](https://user-images.githubusercontent.com/98370960/190488610-19958291-2443-430e-b880-d9a01e611130.png)
![image](https://user-images.githubusercontent.com/98370960/190488722-c5b051f8-1c62-462f-9c64-bae3492ccf77.png)
![image](https://user-images.githubusercontent.com/98370960/190488787-b949909c-8820-4c44-b2a5-9565215d509c.png)
![image](https://user-images.githubusercontent.com/98370960/190488863-25123c18-cf02-4ea5-a2e2-dc5522e60d03.png)


* ### Optimizing the Model

First I had to leave the "NAME" column and only remove "EIN" because that's what helped in reaching accuracy over 75%
![image](https://user-images.githubusercontent.com/98370960/190492593-138745dd-1160-47a5-9efb-33cd5c386bea.png)

Used an automated model optimizer to get the most accurate model possible by creating a method that creates a keras Sequential model using the keras-tuner library with hyperparametes options. Below is what had to be done step-by-step before our best model of 75% or higher was achieved:

![image](https://user-images.githubusercontent.com/98370960/190492986-bc29cb4e-67a1-4a8b-80ee-00640154794e.png)
![image](https://user-images.githubusercontent.com/98370960/190493090-1de47b98-70f4-4608-bc13-9fc32ea24f79.png)
![image](https://user-images.githubusercontent.com/98370960/190493207-6e53ae91-756a-485f-b0ef-fe4256012910.png)

* ### Summary

The automatically optimized neural network trained model from the keras tuner method achieved close to 80% prediction accuracy with a 0.45 loss, using a sigmoid activation function with input node of 86; 5 hidden layers at a 16, 11, 26, 26, 1, neurons split and 50 training epochs. Performing better than the non automized model. Keeping the Name column was crucial in achieving and and going beyond the target.


