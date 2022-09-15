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
### Step 1: Preprocess the Data

* #### Read in the data
![image](https://user-images.githubusercontent.com/98370960/190320012-0369d2ca-4cb0-4791-816e-108a7d46d11f.png)

* #### Dropped the non-beneficial ID columns because they are neither targets nor features
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

