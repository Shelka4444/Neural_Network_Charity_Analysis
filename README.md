# Neural Network Charity Analysis

# Overview of the analysis: 

Using  machine learning and neural networks to create a binary classifier that is capable of predicting whether applicants will be successful if funded by a corporate sponsor, Alphabet Soup. Analysing a CSV file containing more than 34,000 organizations, the dataset is preprocessed to extract and clean the columns with the most relevant data for the problem at hand. The data is then trained, compiled, and evaulated in a series of neural network models using Tensoflow's library of available classification functions. The target model performance is set at 75%.

# Results: 

## Data Preprocessing
- In the Data Preprocessing stage, it was determined that the IS-SUCCESSFUL column is the target for the model. 
- The following categories will become the features used to build the model's prediction capabilites: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT.  
- The EIN and NAME columns were dropped from the dataframe because these identification columns do not carry information which will affect the analysis.  

## Compiling, Training, and Evaluating the Model
- After the data preprocessing was complete, the dataframe was sorted into training and testing variables. The code for the original model is as follows:

<p align='center'>
  <img src="https://github.com/Shelka4444/Neural_Network_Charity_Analysis/blob/main/Images/Original_Summary.png" alt="Original Code" width=750>
</p>

There are 86 neurons in the first hidden layer and 30 in the second layer. The activation functions for the hidden layers are relu which takes values from 0 to infinite. The output function is sigmoid which is bound between 0 and 1 which translates easily into a binary classifcation system. 

The target model performance did not reach the set evaluation level. This model returned a value of approximately 72.5%. 
<p align='center'>
  <img src="https://github.com/Shelka4444/Neural_Network_Charity_Analysis/blob/main/Images/Original_Accuracy.png" alt="Original Accuracy" width=650>
</p>

<strong> First Attempt: </strong> 
- In order to increase the models performance, I first tried to add a third hidden layer with a relu activation function which increased the number of parameters being evaluated, as seen below:                         
<p align='center'>
  <img src="https://github.com/Shelka4444/Neural_Network_Charity_Analysis/blob/main/Images/Attempt1_code.png" alt="First Attempt Code" width=750>
  <img src="https://github.com/Shelka4444/Neural_Network_Charity_Analysis/blob/main/Images/Attempt1_summary_table.png" alt="First Attempt Parameters" width=750>
</p>   

The target model performance did not reach the set evaluation level. This model returned a value of approximately 72.5%. 
<p align='center'>
  <img src="https://github.com/Shelka4444/Neural_Network_Charity_Analysis/blob/main/Images/Attempt1_Accuracy.png" alt="First Attempt Accuracy" width=650>
</p>

                                                                                                                      
How many neurons, layers, and activation functions did you select for your neural network model, and why?
Were you able to achieve the target model performance?
What steps did you take to try and increase model performance?

# Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
