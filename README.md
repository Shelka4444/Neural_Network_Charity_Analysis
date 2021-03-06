# Neural Network Charity Analysis

# Overview of the analysis: 

Machine learning and neural networks are used to build a binary classifier mdoel that is capable of predicting whether applicants will be successful if funded by the corporate sponsor, Alphabet Soup. Analysing a CSV file containing more than 34,000 organizations, the dataset is preprocessed to extract and clean the columns with the most relevant data for the problem at hand. The data is then trained, compiled, and evaulated in a series of neural network models using Tensoflow's library of available classification functions. The target model performance is set at 75%.

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

There are 86 neurons in the first hidden layer and 30 in the second layer. The activation function for the hidden layers is relu which takes values from 0 to infinite. The output function is sigmoid which is bound between 0 and 1 and as such, translates easily into a binary classifcation system. 

The target model performance did not reach the set evaluation level. This model returned a value of approximately 72.5%. 
<p align='center'>
  <img src="https://github.com/Shelka4444/Neural_Network_Charity_Analysis/blob/main/Images/Original_Accuracy.png" alt="Original Accuracy" width=650>
</p>

<strong> First Attempt: </strong> 
- In order to increase the models performance, a third hidden layer with a relu activation function was added. This addition increased the number of parameters being evaluated, as seen below:                         
<p align='center'>
  <img src="https://github.com/Shelka4444/Neural_Network_Charity_Analysis/blob/main/Images/Attempt1_code.png" alt="First Attempt Code" width=750>
  <img src="https://github.com/Shelka4444/Neural_Network_Charity_Analysis/blob/main/Images/Attempt1_summary_table.png" alt="First Attempt Parameters" width=750>
</p>   

The target model performance did not reach the set evaluation level. This model returned a value of approximately 72.5%. 
<p align='center'>
  <img src="https://github.com/Shelka4444/Neural_Network_Charity_Analysis/blob/main/Images/Attempt1_Accuracy.png" alt="First Attempt Accuracy" width=650>
</p>

<strong> Second Attempt: </strong> 
- In order to increase the models performance, the second layer of the original code was ammended to a tanh activation function, as seen below:                         
<p align='center'>
  <img src="https://github.com/Shelka4444/Neural_Network_Charity_Analysis/blob/main/Images/Attempt2_code.png" alt="Second Attempt Code" width=750>
  <img src="https://github.com/Shelka4444/Neural_Network_Charity_Analysis/blob/main/Images/Attempt2_summary_table.png" alt="Second Attempt Parameters" width=750>
</p>   

The target model performance did not reach the set evaluation level. This model returned a value of approximately 72.6%. 
<p align='center'>
  <img src="https://github.com/Shelka4444/Neural_Network_Charity_Analysis/blob/main/Images/Attempt2_Accuracy.png" alt="Second Attempt Accuracy" width=650>
</p>


<strong> Third Attempt: </strong> 
- For this attempt, the original code was amended to increase the number of epochs used to train the model. The original model was set at 100 epochs while this model increased the number of iterations to 150, as seen below:                         
<p align='center'>
  <img src="https://github.com/Shelka4444/Neural_Network_Charity_Analysis/blob/main/Images/Attempt3_Epochs.png" alt="Third Attempt Code" width=750>
</p>   

This third attempt also produced a modest result of 72.5% which did not reach the set evaluation level. 
<p align='center'>
  <img src="https://github.com/Shelka4444/Neural_Network_Charity_Analysis/blob/main/Images/Attempt3_Accuracy.png" alt="Third Attempt Accuracy" width=650>
</p>
                                                                                                                      

# Summary: 
None of the deep learning models created were able to reach the set evaluation accuracy measure of 75%. There are a number of changes which can be implemented to build a stronger model, such as finessing the input data with better preprocessing techniques, adding more neurons to hidden layers, adding a new hidden layer, using different activation functions, and/or adjusting the number of epochs. A unique combination of these components could yield higher results which are necessary for building stronger business application models. Since this problem is a binary classification analysis, logistic regression, linear regression, and support vector machine algorithms may produce stronger results overall since these algorithms are already built to deal with two class systems.
