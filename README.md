# Neural_Network_Charity_Analysis  

## Overview   
AlphabetSoup is philanthropic foundation that raises money to support other organizations which are involved in research and actions to protect the environment, increase human welfare, and to promote global unity.  Through an application process, AlphabetSoup identifies organizations to subsidize and distributes its funds directly to them.  The purpose of this project is to ensure that the selection process accurately identifies organizations that will fulfill their commitments to AlphabetSoup.  The successful process and model will reduce or eliminate donations to high-risk organizations.    

AlphabetSoup furnished a database of over 2,050 organizations with 34,300 observations and 9 features.  The original features are as follows:   

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

## Results   
#### Pre-processing  
•	The target variable is IS_SUCCESSFUL  
•	Feature variables are:  
APPLICATION_TYPE—Alphabet Soup application type  
AFFILIATION—Affiliated sector of industry  
CLASSIFICATION—Government organization classification  
USE_CASE—Use case for funding  
ORGANIZATION—Organization type  
INCOME_AMT—Income classification  
ASK_AMT—Funding amount requested  

•	Variable(s) that were neither targets nor features and were removed from the input data were:  
EIN and NAME—Identification columns  
STATUS—Active status  
SPECIAL_CONSIDERATIONS—Special consideration for application  

Status and Special_Considerations were removed during the optimization process to further the accuracy of the model.  

#### Compiling, Training, and Evaluating the Model  
•	Neurons, layers, and activation mechanisms   
After several days of concentrated effort and many essays of multiple combinations of feature engineering, increase and/or reduction in training epochs, and substitution in the number of layers, neurons, and activation types, I found the following:  
o	25 epochs gave the highest accuracy in stepwise training iterations from 10 epochs to 150  
hidden_nodes_layer1=80	relu  
hidden_nodes_layer2=50	relu  
hidden_nodes_layer3=30	relu  
o	This mix of layers, neurons, and activation methods seemed to work better than others:  
