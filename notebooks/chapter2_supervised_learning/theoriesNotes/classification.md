# Introduction

In logistic regression we learned about how to use sigmoid function to make probabilistic prediction between 0 to 1. For example predicting that given email has 75% chance of being spam. But what if our task if to find out just if the mail is spam or not.

Classification is the task of predicting which of a set of categories an example belongs to. 

Say we have a logistic regression model that gives probability value of the email being spam or not between the value 0-1. A probability of 50% signifies that it has 50% chance of being spam and the probability of 90% signifies that it has 90% chance of being spam. Now if you want to deploy this model in an email application you need to filter the spam mail into seperate mail folder. To do so you need to convert the model raw numerical output in one of the two category: "Spam" or "not spam"

To make this conversion you need a threshold probability called classification threshold. Examples with a probability above threshold value belongs to positive class and probability below threshold value belongs to negative class.


## Confusion Matrix