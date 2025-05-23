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
When choosing the best loss function consider how you want to treat the outliers. You if want your model near to outliers use MSE and if you want your model more close to the data points use MAE