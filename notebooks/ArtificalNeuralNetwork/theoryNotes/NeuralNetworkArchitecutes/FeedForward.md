# Feed Forward Neural Network (FNN)
FNN is a type of neural network in which information flows in a single direction from input to ouput without any feedback loop or cycles.
It is a foundational architecture used in machine learning tools like classification and regression

### characteristics of FNN
1. unidirectional information flow: information/data flows from input layer to hidden layer to the output layer
2. No feedback loop: Unlike RNN, FNN dont have conenctions that loop back
3. supervised Learning: FNN are commonly used for supervised learning tasks.

### Strucutre 
![FNN](../../images/FNN.png)

Feedward neural network has a structured layered desing where data flows sequentially thorugh each layer.
1. input layer: input layer consists of neuron that recieves input data. Each neuron in the input layer represent a feature of the input data
2. Hidden layer: One or more hidden layer are present between input layer and output layer. Hidden layer are responsible for finding complex patterns in the data.
3. Output layer: this layer is responsible for providing the final output of the network.
The number of neurons in this layer corresponds to the number of classes in classification problems or number of outputs in regression problems.

Each connections between the neurons has associated weights between them which is adjusted during training process to minimize errors in the predictions.

### Activation Function
Activation function introduce non linearity into the network allowing the networks to learn complex data patterns.
![Activationfunction](../../images/ActivationFunction.png)

Common activation functions are:
1. Sigmoid: 1/(1+e^-x)
2. Tanh: (e^x - e^-x )/(e^x+e^-x)
3. Relu: max(0,x)

## Training a Feedforward Neural Network
It involves adjusting weights of the neurons to minimize the error between actual and predicted output. This process is generally perfomed using backpropagaion and gradient descent.
1. Foward propagation: During forward propagation the input data passes through network and ouput is calculated
2. loss calculation: Loss is calculated using loss function such as Mean Square Error for regression task and cross entropy for classification tasks.
3. Backpropagation: error are propagated back through the network to update weights. The gradient of the loss function with respect to each weight is calculated and weights are adjusted using gradient descent.

### Gradient Descent
it is an optimization algorithm used to minimize the loss by iteratively updating the weights in the direction of negative gradient.

## Evaluation of FNN
1. accuracy: proportion of correctly classified instances out of total instances
2. precision: ratio of true positive predictions out of total predicted positive
3. recall: ration of true positive prediction out of actual positives
4. F1 score: harmonic mean of precision and recall

## Implementaion Code
![implementationCode](../../codes/FNN.ipynb)