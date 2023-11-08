# Neural Network Model Report [Module 21]
## 1.	Overview: 
### The purpose of the analysis is to develop a binary classifier tool (deep learning model). This tool will be used to predict whether an applicant will be successful if funded by Alphabet Soup (a nonprofit foundation). The accuracy target is => 75%.  

## 2.	Results:
### o	Data Preprocessing 
###    •	The following variables were dropped EIN and NAME (identification columns).
###    •	The target variable is IS_SUCCESSFUL (was the money used effectively).
###    •	The following variables are the features of the model:
####       APPLICATION_TYPE—Alphabet Soup application type *Used binning for better results.
####       AFFILIATION—Affiliated sector of industry
####       CLASSIFICATION—Government organization classification *Used binning.
####       USE_CASE—Use case for funding
####       ORGANIZATION—Organization type
####       STATUS—Active status
####       INCOME_AMT—Income classification
####       SPECIAL_CONSIDERATIONS—Special considerations for application
####       ASK_AMT—Funding amount requested

### o	Compiling, Training, and Evaluating the Model
###     1st  attempt – I used 2 hidden layers, first one had 8 neurons and the second had 5. The activation function ‘relu’ was used for the hidden layers. The number of Epochs was 100. I started with this setup using one of our class examples.
I reran the model many times using different activation functions, 150 epochs and 3 hidden layers, using 10 neurons each. My best accuracy was just under 72. 

## 3.	Summary: 
###    The best accuracy achieved for this challenge is 72.944%. Here is the setup for the Optimized (final) model ->  3 hidden layers with 10 neurons each, all using 
activation function ‘tanh’. I also added an Adam optimizer, that noticeably boosted the accuracy. It may be possible to meet the 75% accuracy using a more preprocessing (binning  or removing more columns etc.).
###    As neural network models are continuously evolving, I believe there is a model that can meet and exceed the 75% accuracy requirement.
