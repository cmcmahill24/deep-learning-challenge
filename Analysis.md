# Neural Network Model Analysis for AlphabetSoup Charity

## Overview of the Analysis

The purpose of this analysis is to design, train, and optimize a deep neural network to predict the success of charity donations using the AlphabetSoup dataset. This project involves preprocessing data, building neural network models, and experimenting with different configurations to achieve the highest possible accuracy, aiming for at least 75%.

## Results

### Data Preprocessing
* What variable(s) are the target(s) for your model?
The target variable is IS_SUCCESSFUL, which indicates whether a funding application was successful (1) or not (0).
* What variable(s) are the features for your model?
Features include all other columns in the dataset after preprocessing, such as one-hot encoded categorical variables for:
APPLICATION_TYPE
CLASSIFICATION
USE_CASE
ORGANIZATION
STATUS
INCOME_AMT
SPECIAL_CONSIDERATIONS
ASK_AMT

* What variable(s) should be removed from the input data because they are neither targets nor features?
The following columns were removed:
EIN and NAME: These identifiers do not contribute predictive information to the model.

### Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?

* Initial Model:
Layers: Two hidden layers.
Neurons: 80 and 30 neurons for the hidden layers.
Activation Functions: relu for hidden layers and sigmoid for the output layer.
Reason: These values were chosen as a starting point based on common practices for binary classification problems.

* Optimized Model:
Layers: Two hidden layers.
Neurons: Increased to 100 and 50 for better learning capacity.
Activation Functions: Experimented with tanh for hidden layers.
Reason: Increasing neurons and trying tanh helped improve the model's performance slightly.

* Were you able to achieve the target model performance?
The best accuracy achieved was 73.12%, which is slightly below the target accuracy of 75%. Despite multiple optimizations, further refinements or alternative models are needed to reach the target.

* What steps did you take in your attempts to increase model performance?
Adjusted the number of neurons in the hidden layers (80/30 to 100/50).
Experimented with different activation functions (relu vs. tanh).
Dynamically adjusted the learning rate during training.
Tested additional epochs to allow the model to converge further.

## Summary
### Overall Results:
The final optimized neural network achieved an accuracy of 73.12%. While this is a reasonable result, it doesn't reach the target accuracy of 75%.
Adjusting hidden layers, neurons, and activation functions showed improvements in model performance.
Recommendation:
To improve performance, a different model such as a Random Forest Classifier or Gradient Boosting Classifier could be used. Tree-based models are less sensitive to feature scaling and can naturally handle categorical features, making them more robust for this type of classification problem.
