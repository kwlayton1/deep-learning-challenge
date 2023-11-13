# Neural Network Model Report [Module 21]
## --------------------------------------------------------------
## As I only received a 92 on this assignment, I am adding more explanation and adjusting the code. 
## The number of Epochs was changed to 50 from 100  (for more efficient running time of the code). I also adjusted the model to use ReLU activation functions on the hidden layers, as this is more appropriate for the input data e.g simple and computationally efficient. I had Tanh in the first attempt because it was the last one I tried and it produced about the same accuracy as all of the other functions. I studied this and Tanh is not really appropriate as it squashes the output to be between -1 and 1, making it zero-centered.  
## Also, I am aware that adding the NAME back into the features for better accuracy in the first submission also affects the training of the model. Now the NAME of the applicant will influence model. In this scenario I would be sure to convey this information to the Alphabet Soup Charity team. The accuracy is now 79.29%


## 1.	Overview: 
### The purpose of the analysis is to develop a binary classifier tool (deep learning model). This tool will be used to predict whether an applicant will be successful if funded by Alphabet Soup (a nonprofit foundation). The accuracy target is => 75%.  

## 2.	Results:
### o	Data Preprocessing 
###    •	The following variables were dropped EIN and NAME (identification columns).
###    •	The target variable is IS_SUCCESSFUL (was the money used effectively).
###    •	The following variables are the features of the model:
####         APPLICATION_TYPE—Alphabet Soup application type *Used binning for better results.
####         AFFILIATION—Affiliated sector of industry
####         CLASSIFICATION—Government organization classification *Used binning.
####         USE_CASE—Use case for funding
####         ORGANIZATION—Organization type
####         STATUS—Active status
####         INCOME_AMT—Income classification
####         SPECIAL_CONSIDERATIONS—Special considerations for application
####         ASK_AMT—Funding amount requested

### o	Compiling, Training, and Evaluating the Model
###     1st  attempt – I used 2 hidden layers, first one had 8 neurons and the second had 5. The activation function ‘relu’ was used for the hidden layers. The number of 
###      Epochs was 100. I started with this setup using one of our class examples.
###     I reran the model many times using different activation functions, 150 epochs and 3 hidden layers, using 10 neurons each. My best accuracy was just under 72. 

## 3.	Summary: 
###   The accuracy achieved for this model is 79.17% and is above the 75% target!
###   Hre is the setup for the Optimized (final) model ->  3 hidden layers with 10 neurons each, all using activation function ‘tanh’. I also added an Adam optimizer, that     boosted the accuracy to 72.944%. Thanks to my tutor 'Geronimo Perez'. His suggestion to not drop the feature ‘NAME’ and bin it with value_counts() 6 as the cutoff for    'Other'. This narrowed in the data and created a much higher accuracy.

