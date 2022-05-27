# ServerTemperaturePredictionToBeShared

## Parameters v/s hyperparameters: 

1. Parameters are variables that allow the model to learn the rules from the data.
2. Hyperparameters are also variables that control how the model is training.
3. Parameters learn their own values from data. In contrast, hyperparameters do not learn their values from data. We need to manually specify them before training the model.
4. Parameter values are updated during the training process. Hyperparameter values remain fixed during the model training process.

5. In a neural network model, the following are the hyperparameters that control the values of Ws and bs:

Number of layers in the network
Number of nodes in each layer (also called Layer size)
Type of loss function
Type of optimizer
Type of activation function(s)
Batch size
Epochs


Read more about hyperparameter v/s parameter: https://rukshanpramoditha.medium.com/parameters-vs-hyperparameters-what-is-the-difference-5f40e16e2e82

###########################################################

## Training set vs validation set vs test set:

The training set is used to fit the parameters of the model on a fixed combination of hyperparameters.
The validation test is useful for hyperparameter tuning or selecting the best model out of different models. In some contexts, the validation set is also called the Development (Dev) set.
The performance of that model using the test set

In summary, the training set is used to fit the model parameters, the validation set is used to tune model hyperparameters. Finally, we use the test set to evaluate the best model.

Read more: https://towardsdatascience.com/why-do-we-need-a-validation-set-in-addition-to-training-and-test-sets-5cf4a65550e0

##########################################################

# Model with dataloader: 
https://colab.research.google.com/drive/1_X306vLbDoXWTheLBvD3tOZ6Mb126d6y#scrollTo=3Y1M2wkzTF88
