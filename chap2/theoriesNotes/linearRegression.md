# Linear Regression
Linear Regression is the statistical tool used to find the relationship between variables. In Ml context it is used to find out the relationship between features and label.

The equation of linear Regression in ML context is: y = w1x1+b:
                                                where y = output label, prediction
                                                      w1 = weight of feature, weight
                                                      x1 = feature-input, feature value 
                                                      b = bias
x1,b are calculated from training

## Loss
Loss are the numerical value that describes how wrong the model predictions are. It describes how far the model prediction value from the actual values. The goal of training the model is to minimize this loss.

We always takes the absoulte value in the loss as we dont care about direction instead we focus on the actual value.
The two methods to remove the sign are : take absolute value, square the difference between actual value and predicted values

In linear Regression there are four types of loss: L1 loss, Mean absolute error, L2 loss, Mean squared error

L1 loss = sum of absolute value between the difference between actual value and predicted value
Mean Absolute error = average of the value of L1 Loss 
L2 loss = sum of square of difference between actual value and predicted value
Mean Squared Error = the average of loss of l2 loss


# chosing a loss function
Deciding upon MSE or MAE depends on the way you want to handle certain predictions. 
An outlier refers to how far the model prediction is from actual values.
When choosing the best loss function consider how you want to treat the outliers. You if want your model near to outliers use MSE and if you want your model more close to the data points use MAE.

# Gradient Descent
Gradient Descent is a mathmatical technique that iteratively calculates the weight and bias that produce the model with minimum loss. The model begins training with randomized weights and bias near zero and then repeats the following steps:
1. calculate loss with current bias and weight
2. Determine the direction to move the weights and bias that reduce loss
3. move the weight and bias values a small amount in the direction of reduce loss
4. return to step 1 and repeat the process until the model cannot reduce the loss any further


# Hyperparameter 
Hyperparameter are variables that controls different aspects of training. Three common hyperparameters are learning rate, epoch, batch size.

## Learning Rate: 
It is a floating point number that influences how fast the model converges. If the learning rate is too low, model would take long time to converge. However if learning rate is too high it might never converges. The goal is to take learning rate not too high or low so that model converges quickly.
## Batch size: 
It refers to number of examples the model processes before updating its weight and bias. A dataset might contains hundreds of thousands of data so calculating loss of every example isnt practical. ie full batch size. Two of the common techniques to get the right gradient on average without the need of looking at every example are stochasitc gradient descent and mini batch stochasitic gradient descent.

## Epochs
During training, an epoch means that the model has processed every example in the training set once. For example, given a training set with 1000 examples and a mini batch size of 100 examples, it will take the model 10 iterations to complete one epoch.

