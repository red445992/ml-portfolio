# Introduction

In logistic regression we learned about how to use sigmoid function to make probabilistic prediction between 0 to 1. For example predicting that given email has 75% chance of being spam. But what if our task if to find out just if the mail is spam or not.

Classification is the task of predicting which of a set of categories an example belongs to. 

Say we have a logistic regression model that gives probability value of the email being spam or not between the value 0-1. A probability of 50% signifies that it has 50% chance of being spam and the probability of 90% signifies that it has 90% chance of being spam. Now if you want to deploy this model in an email application you need to filter the spam mail into seperate mail folder. To do so you need to convert the model raw numerical output in one of the two category: "Spam" or "not spam"

To make this conversion you need a threshold probability called classification threshold. Examples with a probability above threshold value belongs to positive class and probability below threshold value belongs to negative class.


## Confusion Matrix
Let's say you have a logistic regression model for spam-email detection that predicts a value between 0 and 1, representing the probability that a given email is spam. A prediction of 0.50 signifies a 50% likelihood that the email is spam, a prediction of 0.75 signifies a 75% likelihood that the email is spam, and so on.

You'd like to deploy this model in an email application to filter spam into a separate mail folder. But to do so, you need to convert the model's raw numerical output (e.g., 0.75) into one of two categories: "spam" or "not spam."

To make this conversion, you choose a threshold probability, called a classification threshold. Examples with a probability above the threshold value are then assigned to the positive class, the class you are testing for (here, spam). Examples with a lower probability are assigned to the negative class, the alternative class (here, not spam).

The probability score is not reality or ground truth. There are four possibilities for each outcome in a binary classifier. For spam classifier example if you lay out the ground truth as columns and rows, the following table as confusion matrix is the result:

**.** True positive(TP): A spam mail correctly classified as spam mail.
**.** False positive(FP): A not spam mail is classified as spam mail.
**.** True negative(TN): A not spam mail is correctly classified as not spam mail.
**.** False negative(FN): A spam mail is classified as not spam mail.

## Accuracy: 
It means "Out of all predictions how many were correct?"
ie. Accuracy = (Correct Predictions) / (Total Predictions)
             = (TP+TN)/(TP+TN+FP+FN)

Imagine you have 1000 emails: 990 are not spam, 10 are spam.
If your mail label everything as not spam, it will: correctly label 990 mails, miss all 10 spam mails
so Accuracy = 990/1000 = 99%.
But this model is useless as it didnt catch any spams, even though accuracy is 99%.

## Recall:
Recall says "Out of all the actual positive cases, how many did my model catch?".
Recall = True Positives / (True Positives + False Negatives)
       = TP / (TP + FN)
You have 100 actual spam emails.
Your model correctly catches 80 of them. (TP = 80). It misses 20, thinking they are real. (FN = 20).
Recall = 80 / (80 + 20) = 80 / 100 = 0.8 → or 80%

Why is Recall Important?
In critical tasks, like detecting diseases, fraud, or spam, you want to catch all the real positive cases.

False negatives (missing the actual positive cases) can be very dangerous.

For example: In disease detection, a false negative means a sick person is told they're healthy — a big problem! In spam detection, a false negative means spam reaches your inbox — annoying, but not terrible.

## Accuracy vs Recall
Imagine 1,000 emails:990 are not spam,10 are spam. If your model says "none of them are spam":
Accuracy = 990 / 1000 = 99% 
Recall = 0 / (0 + 10) = 0% 
Your model looks accurate, but fails to detect any spam! That’s why recall is better when: The positive class is rare. Missing a positive is costly

## False Positive Rate
False Positive Rate (FPR) says "Out of all the things that are actually negative, how many did my model wrongly think were positive?"
FPR = False Positives / (False Positives + True Negatives)
    = FP / (FP + TN)
Imagine you have: 900 legit (not spam) emails. Out of these, your model wrongly marks 90 as spam (false alarms).
FPR = 90 / (90 + 810) = 90 / 900 = 0.1 → or 10%. This means: 10% of real emails are being wrongly marked as spam.
Why Is FPR Important? Because in real-world systems: A high FPR means your model creates false alarms. These can cause annoyance, lost trust, or worse.

## Precision
Precision says: "Of all the things my model said are positive, how many are actually positive?"
Precision = True Positives / (True Positives + False Positives)
          = TP / (TP + FP)

Example:
Let’s say your model predicts 50 emails as spam: 40 of those are actually spam (TP). 10 are real emails wrongly marked as spam (FP)
Precision = 40 / (40 + 10) = 40 / 50 = 0.8 → or 80%. 80% of the emails your model marked as spam were actually spam.

Why precision is important?
In some applications, it's very costly to make false positive errors.
Example Use Cases:
    Domain    |             What is a False Positive?	  |      Why It's Bad
Spam detection	|A real email marked as spam	          | You miss important messages
Cancer screening|	Healthy person marked as having cancer|	Causes stress, unnecessary tests
Fraud detection	|A legit transaction flagged as fraud|	User can't complete payment

## Why Choosing the Right Metric Matters
When you train a machine learning model (like a spam filter, disease detector, etc.), you need to evaluate how good it is. But the idea of “good” depends on what kind of mistakes matter most. Different situations need different priorities. That's why you pick metrics based on the cost of errors.
Common Trade-offs
Mistake Type	Description	Example
False Positive (FP)	Predicting something is positive, but it's actually not	Marking a legit email as spam
False Negative (FN)	Predicting something is negative, but it’s actually positive	Missing a spam email

You can't always reduce both at once. Improving one often worsens the other — so you choose what matters most for your problem.

## Which Metric to Use When?
Accuracy
"How many predictions were correct?"
Good for: Balanced datasets (equal positives and negatives)
Bad for: Imbalanced datasets (e.g., 1% of emails are spam)
Use it for:
Early model monitoring
Quick snapshot of training progress
With other metrics for final evaluation
 Example: If 99% of emails are legit and your model just says “not spam” for everything, it gets 99% accuracy — but it's useless.

## Recall (True Positive Rate)
"Of all the actual positives, how many did I catch?"
Use when:
Missing a positive case is risky
False negatives are more expensive
Examples:
Disease detection (missing a sick patient is dangerous)
Spam filters (you want to catch all spam)
 False Positive Rate
"Of all actual negatives, how many did I wrongly flag?"
Use when:
False alarms are costly or annoying
False positives are more expensiveExamples:
Fraud detection (you don't want to block legit transactions)
Security systems (you don’t want false alarms all day)

## Precision
"Of all things I predicted as positive, how many were correct?"
Use when:
You need high confidence in positive predictions
False positives are worse Examples:
Legal document classification (false positives could waste lawyer time)
Email spam detection (you don’t want to lose real emails)