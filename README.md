# Neural Network Charity Analysis

## Overview of Analysis
The purpose of this project is to use Deep-Learning Neural Networks with Tensor Flow to analyze and classify the success of the charity donations. 
The analysis consists of three technical analysis deliverables as follows: 
- Deliverable 1: Preprocessing Data for a Neural Network Model
- Deliverable 2: Compile, Train, and Evaluate the Model.
- Deliverable 3: Optimize the Model.

## Results
### Data Preprocessing
- The columns `EIN` and `NAME` are identification information and have been removed from the input data. 
- The `IS_SUCCESSFUL` column contained binary data referring to whether or not the charity donation was used effectively. This variable is then considered as the target for the Deep Learning Neural Network. 
- The features for the model are the following columns: `APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CARE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT`.

### Compiling, Training and Evaluating the Model
- The Deep_Learning Neural Network Model is made of two hidden layers with 80 and 30 neurons. 
- Input data has 43 features and 25,724 samples. 
- Output layer is made of a unique neuron as it is a binary classification. 
- Activation function `ReLU` was used for the hidden layers to speed up the training process. 
- Since the output is a binary classification, `Sigmoid` is used on the output layer. 
- For the compilation, the optimizer is `adam` and the loss function is `binary_crossentropy`
- Model accuracy is under 75% which is not a satisfying performance to help predict the outcome of the charity donations. 
- To help increase the performance of the model, bucketing to the feature `ASK_AMT` was applied and the different values were organized  by intervals. 
- The number of neurons were increased on one of the hidden layers and used a model with three hidden layers. 
- Tried to use a different activation functioni `tanh` but none of these steps helped improve the model's performance. 

## Summary
- Because the Deep Learning Neural Network Model didn't every reach the 75% accuracy target we can conclude that the model is not outperforming. 
- Because the binary classification, we could use a supervised machine learning model such as the Random Forest Classifier to combine a multitude of decision trees to generate a classified output and evaluate its performance against our deep learning model.