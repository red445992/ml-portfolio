# Logistic Regression
Logistic Regression is a type of ML model that predicts probabilities. Logistic Regression Model has following characteristics:
1. The label is categorial. The term logistic regression usually refers to binary logistc regression that is to a model that calculates probabilites for labels with two possible values.
2. The loss function during training is LogLoss.

**For example**: Consider a logistic regression model that calculates the probability of an input email being either spam or not spam. During inference suppose the model predicts 0.72. Therefore the model is estimating: 72% chance of the email being spam. 28% chance of the email not being spam.

A logistc regression model uses the following two step architecture:
1. the mdoel generates a raw prediction by applying a linear function of input features.
2. the model uses that raw predcition as input to a sigmoid function which converts the raw prediction to a value between 0 and 1


## Logistic regression Calculating a probability with sigmoid function
