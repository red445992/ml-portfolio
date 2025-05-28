# Logistic Regression
Logistic Regression is a type of machine learning model that predicts probabilities. It is primarily used for classification problems, especially binary classification. The model outputs a value between 0 and 1, which represents the probability that a given input belongs to the positive class.

## Characteristics
1. The label (target) is categorical, usually binary (e.g., 0 or 1, Yes or No, Spam or Not Spam).
2. Logistic regression does not assume a linear relationship between the dependent and independent variables like linear regression does. Instead, it uses a sigmoid function to map the linear output to a probability.
3. Logistic regression is interpretable, relatively fast, and works well with linearly separable data.

4. Regularization (like L1 and L2) can be applied to avoid overfitting and improve generalization.

## Example:
 A logistic regression model may predict that a given email has a 0.72 (72%) chance of being spam. This means there's a 28% chance it’s not spam. Based on a threshold (commonly 0.5), we classify it as spam.

## Logistic Regression: Calculating a Probability with the Sigmoid Function
After computing the raw prediction from the linear combination of inputs (i.e., 𝑧=𝑤1𝑥1+𝑤2𝑥2+...+𝑏z=w1x1+w2x2+⋯+b), logistic regression uses the sigmoid function to convert this value into a probability:𝜎(𝑧)=1/1+𝑒^−𝑧

Where:

 z is the linear combination of input features and weights,𝜎(𝑧): σ(z) is the output probability between 0 and 1. This probability represents how likely the input belongs to the positive class.

## Loss and Regularization
🔹 Loss Function: Log Loss (Binary Cross Entropy)
Logistic Regression is trained using Log Loss (also called binary cross entropy), which measures how close the predicted probabilities are to the actual binary labels.
🔹 Regularization
Regularization is used to prevent overfitting by penalizing large weights. It’s added to the loss function during training.
Final Loss Function with Regularization:
Regularization Term
Loss=Log Loss+λ⋅Regularization Term
Where 
λ is a hyperparameter controlling how much regularization is applied.