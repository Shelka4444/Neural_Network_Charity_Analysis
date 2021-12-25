# Neural Network Charity Analysis

# Overview of the analysis: 

Using  machine learning and neural networks to create a binary classifier that is capable of predicting whether applicants will be successful if funded by a corporate sponsor, Alphabet Soup. Analysing a CSV file containing more than 34,000 organizations, the dataset is preprocessed to extract and clean the columns with the most relevant data for the problem at hand. The data is then trained, compiled, and evaulated in a series of neural network models using Tensoflow's library of available classification functions.

# Results: 

## Data Preprocessing
- In the Data Preprocessing stage, it was determined that the IS-SUCCESSFUL column is the target for the model. 
- The following categories will become the features used to build the model's prediction capabilites: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT.  
- The EIN and NAME columns were dropped from the dataframe because these identification columns do not carry information which will affect the analysis.  

## Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
Were you able to achieve the target model performance?
What steps did you take to try and increase model performance?

# Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
