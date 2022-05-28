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

![image](https://user-images.githubusercontent.com/33154959/170734860-e34e61d8-6329-40cf-bb81-41d522468f59.png)


### Sequence length usage: 
So, given i and the sequence_length, we return the block of data from i - sequence_length through row i. If i is at the beginning of the dataset, we pad by repeating the first row as many times as needed to make the output have sequence_length rows. The only trick is avoiding off-by-1 errors in the slicing and padding.

Refer this for more explanation: https://www.crosstab.io/articles/time-series-pytorch-lstm




##########################################################

### criterion:
This criterion computes the cross entropy loss between input and target.

optimizer.step()

### optimizer.step
is performs a parameter update based on the current gradient (stored in .grad attribute of a parameter) and the update rule. As an example, the update rule for SGD is defined here:
https://github.com/pytorch/pytorch/blob/cd9b27231b51633e76e28b6a34002ab83b0660fc/torch/optim/sgd.py#L63 


### loss.backward()
Calling .backward() mutiple times accumulates the gradient (by addition) for each parameter. This is why you should call optimizer.zero_grad() after each .step() call. Note that following the first .backward call, a second call is only possible after you have performed another forward pass.

So for your first question, the update is not the based on the “closest” call but on the .grad attribute. How you calculate the gradient is upto you.

https://discuss.pytorch.org/t/how-are-optimizer-step-and-loss-backward-related/7350

##########################################################

# Model with dataloader: 
https://colab.research.google.com/drive/1_X306vLbDoXWTheLBvD3tOZ6Mb126d6y#scrollTo=3Y1M2wkzTF88

# Model with dataloader with correct data split:
https://colab.research.google.com/drive/19a_0kZ4qljT_t5aDLPe0VP6vzy3DfUc6#scrollTo=4N8fT51gTq48
