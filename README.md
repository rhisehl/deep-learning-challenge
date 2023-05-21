# Deep Learning: Alphabet Soup Charity Model

## Overview
The intention of the analysis is to assist the nonprofit Alphabet Soup in determining whether or not organizations' ventures will be successful if Alphabet Soup provides capital investment. This is to be evaluated as a binary classification of successful or unsuccessful.


## Results

### Data Preprocessing
The target for analysis is whether or not the venture was successful.
The features are:
  * Application Type
  * Affiliation
  * Classification
  * Use Case
  * Organization type
  * Current Status
  * Income Category
  * Special Considerations
  * The amount asked for
EIN and Company name were removed from the analysis since niether of them should have an impact on venture success.

### Compiling, Training, and Evaluating the Model

Application type and classification values were reduced so low value counts were clustered into an 'other' category. For application type, the frequency cutoff was set to 500. For classification, the frequency cutoff was set to 100.

The initial model was trained using one single layer of neurons with RELU activation, with an output layer of one neuron with Sigmoid activation. This model was trained on 10 epochs.

The initial model's parameters were determined as the smallest neural network, as well as the least amount of classifications and application types. This resulted in a model with 72% accuracy and .5714 loss.

After this, the model's parameters were repeatedly changed, but no model provided an accuracy greater than 73%. Changes included number of hidden layers, number of neurons per layer, activation type, number of combined unique values, and number of epochs.


## Summary

The model was only able to achieve 72-73% accuracy, which is relatively low for a production model. It is possible that dropping additional features and using deep learning to automate the hyperparameters that this model could become more accurate. Other models could also be attempted, such ass the random forest model.
