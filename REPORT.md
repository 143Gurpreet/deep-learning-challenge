# deep-learning-challenge
Overview:
The purpose of the charity funding analysis for Alphabet Soup was to predict where the company would approve/make investments. Our goal was to use machine learning and neural networks to apply target/features on the dataset, create a binary classifier that was capable of predicting whether investors would be successful if funded by Alphabet Soup. We started with 34,000 organizations and 12 columns that captured the metadata about each organization and their past funding outcomes.

Results:
Data Preprocessing
1. What variable(s) are the target(s) for your model?

   The target variable is the 'IS_SUCCESSFUL' column 
3. What variable(s) are the features for your model?
              The feature variables are every other column from dataframe .  this was   defined by    
              dropping the 'IS_SUCCESSFUL' column from the original dataframe.
4. What variable(s) should be removed from the input data because they are neither targets nor features?
              Both 'EIN' and 'NAME' columns were dropped/removed, because they were neither  
              targets nor features for the dataset.

Compiling, Training, and Evaluating the Model
AlphabetSoupCharity_Optimization
Configuration:
* Cutoff for 'APPLICATION_TYPE' and 'CLASSIFICATION': 200 and 100, respectively, with an aim for more binning.
* Random state set to 72.
* Number of input features: 49.
* Three hidden layers with 15, 10, and 5 units, respectively.
* Epochs: 100.
Result:
* Model accuracy: 72%.

AlphabetSoupCharity_Optimization_1
Configuration:
* Cutoff for 'APPLICATION_TYPE' and 'CLASSIFICATION': 1000.
* Random state set to 72.
* Number of input features: 40.
* Four hidden layers with 10, 8, 7, and 5 units initially, then changed to 30, 20, 10, and 15 units in a subsequent test.
* Epochs: 100.
Result:
* Model accuracy: 72%.

AlphabetSoupCharity_Optimization_2
Configuration:
* Cutoff for 'APPLICATION_TYPE' and 'CLASSIFICATION': 100.
* Random state set to 42.
* Number of input features: 50.
* Two hidden layers with 22 and 30 units, respectively.
* Epochs: 200.
Result:
* Model accuracy remained at 72% for both sets of unit configurations.


Compiling, Training, and Evaluating the Model
4. How many neurons, layers, and activation functions did you select for your neural network model, and why?
                     In first attempt Three hidden layers with 15, 10, and 5 units, respectively.
                     In seconed  attempt  Four hidden layers with 10, 8, 7, and 5 units initially,      
                     then changed to 30, 20, 10, and 15 units in a subsequent test.
                      Third attempt  Two hidden layers with 22 and 30 units, respectively. 
    Reason of added layers were just random guess to check the model performance.

5. Were you able to achieve the target model performance?
               I was not able to achieve the 75% model accuracy target

6. What steps did you take in your attempts to increase model performance?
Data Preprocessing: Adjusted binning strategies and varied the number of input features.
Neural Network Architecture: Experimented with different numbers of hidden layers and neurons.
Training Parameters: Varied the number of training epochs and the random state.

Summary
The deep learning model, designed to tackle the classification problem presented by the AlphabetSoupCharity dataset, underwent several rounds of optimization. Despite these efforts, the model consistently achieved an accuracy of approximately 72%. The optimizations involved:
* Adjusting data preprocessing, particularly in binning strategies for categorical variables.

