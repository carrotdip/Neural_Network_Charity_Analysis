# Neural_Network_Charity_Analysis
## Overview
Each year, the Alphabet Soup foundation makes investments to a great deal of organizations. The purpose of this analysis was to determine which applicants, among the thousands to apply to Alphabet Soup, will be successful. This was done by preprocessing the past data for a neural network model, which was then used to compile, train, and evaluate the neural network model. Steps were also taken to optimize the model for accuracy over 75%. In the end, a binary classifier was created to predict the success of the applicants to the Alphabet Soup foundation.
## Results
*Data Preprocessing*
- The variable considered to be the **target** of this model is the **IS_SUCCESSFUL** column.
- The variables considered to be the **features** of this model include the **APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL CONSIDERATIONS,** and **ASK_AMT**.
- The variables that **neither** target nor features include the **EIN** and **NAME**, which was removed from the input data.
*Compiling, Traning, and Evaluating the Model*
- For the neural network model, 2 hidden layers with 80 and 30 neurons, respectively, as well as the **relu** activation functions were selected. There was also an output layer with a **sigmoid** activation function.
- This model was unable to achieve the target model performance at 75%. The accuracy for the model was 73.0%.
![initial model](https://github.com/carrotdip/Neural_Network_Charity_Analysis/blob/232bbba8c6cb3db8adc501ba07bd1e96c2cb4cc6/Initial%20Model.png)\
- The *first* step I took to try to increase the model performance was to change the activation function of the first hidden layer to a **leaky relu** function, while keeping everything else the same. This actually slightly decreased the accuracy of the model to 72.8%.
![attempt#1](https://github.com/carrotdip/Neural_Network_Charity_Analysis/blob/232bbba8c6cb3db8adc501ba07bd1e96c2cb4cc6/Attempt%20%231.png)\
- The *second* step I took to attempt to increase the model performance was to increase the number of neurons in the two hidden layers to 100 and 50. This, again, slightly reduced the accuracy of the model to 72.6%.
![attempt#2](https://github.com/carrotdip/Neural_Network_Charity_Analysis/blob/232bbba8c6cb3db8adc501ba07bd1e96c2cb4cc6/Attempt%20%232.png)\
- The *third* step I attempted to increase the model performance was to add a third hidden layer with 20 neurons. The activation functions for all the hidden layers were changed backi to **relu**. The number of enochs was also increased from 100 to 150. This model also did not reach the target model performance, as its accuracy was 72.8%.
![attempt#3](https://github.com/carrotdip/Neural_Network_Charity_Analysis/blob/232bbba8c6cb3db8adc501ba07bd1e96c2cb4cc6/Attempt%20%233.png)\
## Summary
The model reached an accuracy of 72.8% after optimization, but was initially 73.0%. The loss in accuracy may be explained through overfitting, which is a common error in machine learning and neural networks. Because the target model performance of 75% could not be attained, I would recommend a different model to solve this classification problem. 
Because the data is tabular, I would recommend utilizing a Random Forest Classifier, as it is an extremely robust and accurate model. The feature and output selection of random forest models are easy to interpret and can easily handle outliers and nonlinear data. The Random Forest Classifier is also much quicker with comparable predictive accuracy.
