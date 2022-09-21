# Analysis of Charitable Organizations using Neural Network and Deep Learning Models
## Overview
The purpose of this analysis was to help the non-profit organization, Alphabet Soup, to analyze what organizations are worth donating to. Alphabet Soup raises funds for charities and wants to optimize their decision making by using machine a neural network to review the history of each organization and which of them were successful in the past. A CSV file was provided containing data on a variety of charitable organizations that have received funds from Alphabet Soup in previous years. Using this data, a deep learning neural network model using the python TensorFlow library was developed. 

## Results
### Data Pre-processing
Before developing the neural network, the data needed to be cleaned and processed. This was accomplished using a jupyter notebook. 

The variable "IS_SUCCESSFUL" was selected to be the primary target for the proposed model. Below, a list of variables that were also utilized as features in the model can be found. 

Variables:
* IS_SUCCESSFUL
* APPLICATION_TYPE
* AFFILIATION
* CLASSIFICATION
* USE_CASE
* ORGANIZATION
* STATUS

The following variables were not considered significant for the model:
* EIN
* SPECIAL_CONSIDERATIONS

### Compiling, Training, and Evaluating the Model
For the initial attempt, the following parameters were selected:
* 2 hidden layers with "relu" activation 
* 8 neurons in the first layer
* 5 neurons in the second layer
* A sigmoid output

The "relu" activation was selected for training because its a simple first approach. The "sigmoid" output was selected because the model has one binary output based on the variable "IS_SUCCESSFUL"

The model achieved an accuracy of 72.8% with a loss of 55.8%. This was not adequate for the requested target of 75% accuracy. Screenshot of the result is found below:

![initial_attempt_accuracy](https://user-images.githubusercontent.com/104606662/190947452-2e29401a-0bdb-45ec-9058-a61a02bac43f.png)

In order to increase the model's performance, the following changes were made:
1. A third layer was added making neurals layers of 80, 30, and 10 respectively
2. Layer 1 utilized "relu" activation while Layers 2 and 3 utilized the "sigmoid" activation function

This model achieved an accuracy of 78.6% with a loss of 44.6%. This met the requested target of 75% accuracy. A screenshot of the result is included below:

![optimized_function_accuracy](https://user-images.githubusercontent.com/104606662/190947778-c04e96ca-940e-4e52-8325-a15d80ec8050.png)

## Summary
After optimizing the model, the requested accuracy target was exceeded. The optimized model achieved an accuracy of 78.6% and can be utilized to evaluate the potential success of Alphabet Soup's potential targets to receive fundraising assistance. 
