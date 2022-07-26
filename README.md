# Neural_Network_Charity_Analysis  

## Overview   
AlphabetSoup is philanthropic foundation that raises money to support other organizations involved activities to protect the environment, increase human welfare, and to promote global unity.  Through an application process, AlphabetSoup identifies organizations to subsidize and distributes funds directly to them.  The purpose of this project is to ensure that the selection process accurately identifies organizations that will fulfill their commitments to AlphabetSoup.  The successful process and model will reduce or eliminate donations to high-risk organizations.    

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
    o	This mix of layers, neurons, and activation methods seemed to work better than others:  

                hidden_nodes_layer1=80	relu  
                hidden_nodes_layer2=50	relu  
                hidden_nodes_layer3=30	relu  

    o	Dropping Status and Special_Considerations assisted to increase accuracy to the greatest degree I could achieve.  
    o	I was not able to optimize to the 75% goal; however, I was able to increase accuracy from the baseline 72.6% to 72.8%, a gain of .2% or.002.  
    o	The following is a partial representation of the steps I took to try and increase model performance and the results therefrom:  


![image](https://user-images.githubusercontent.com/101474477/180889081-7cf64c7a-4d7c-483b-8d16-ac38c66202bd.png)


## Summary  
The results of this exercise were not adequate for the needs of the client.  The model does not offer enough information to evaluate results in its current context: there is no measurement of sensitivity, specificity, or precision.  It is difficult to infer what the low accuracy is a result of, or how to avoid making distributions to risky organizations.  The model does not provide clarity through the data to guide the foundation’s policy and operations.    

There are some steps which could be taken to help correct the process. Adding more features to develop a wider net for influential variables is an important step, as would running descriptive summary statistics on the existing dataset to get a clear vision of the data and how variables may interact with one another. Based on more data and more features engineering, it could be possible to optimize the model to achieve target accuracy.  

However, I recommend going to another model altogether; namely, the Random Forest model. This model provides clean comprehensive output in the form of confusion matrixes and classification reports.  It also generates a list of features by importance, making it easier to quickly see the weight of individual variables. It is accurate, resistant to overfitting, and highly interpretable.  It is widely used and therefor familiar to most.
