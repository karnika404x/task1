# Neural Network from Scratch – XOR Classification

### Project Overview

This project implements a basic Neural Network from scratch using NumPy and Matplotlib to solve the XOR classification problem.
All core components such as:
1. Forward Propagation
2. Backward Propagation
3. Activation Functions
4. Loss Calculation
5. Gradient Descent
6. Training Loop

are implemented manually.

### Dataset Used: XOR 
If input is same then output is zero otherwise one, which is not linear therefore cannot be solved using a single linear equation.

| x1 | x2 | Output |
| -- | -- | ------ |
| 0  | 0  | 0      |
| 0  | 1  | 1      |
| 1  | 0  | 1      |
| 1  | 1  | 0      |


### Architecture
Input Layer (2 neurons)

        ↓
Hidden Layer (4 neurons, ReLU activation)

        ↓
Output Layer (1 neuron, Sigmoid activation)
### What each neuron 
Step 1: Multiply and Add

    Z = w1x1+ w2x2 + b

Where:
* x₁, x₂ = inputs
* w₁, w₂ = weights (importance)
* b = bias (adjustment)
* Z = result

This is a straight-line equation.

Step 2: Apply Activation Function

    σ(x)=1/(1 + e**−x1)


XOR needs nonlinear behavior. With activation network does non linear math

### Need of Hidden Layer
Since output of XOR is non linear.Hidden layer helps create nonlinear boundaries.

### Forward Propagation
Forward propagation means: Move from input to output.
Mathematically:

First layer:
   
    Z1= XW1 + b1
Then activation:
A₁ = ReLU(Z₁)

Second layer:

    Z2= A1W2 + b2
Final output:

A₂ = Sigmoid(Z₂)

Where A₂ is your prediction.

### Loss Function
Loss measures error.

    MSE=1/n∑(y(true)−y(spred))^2
If prediction wrong ,loss big.
If prediction correct ,loss small.
### Training Process
* For each epoch:
* Perform forward propagation
* Compute loss
* Perform backward propagation (calculate gradients)
* Update weights using gradient descent:

      W=W−α(dW/dL)
Where:
* α = learning rate
* dL/dW = gradient of loss with respect to weights

The model is trained for 5000 epochs.

### Results
* Loss decreases steadily over epochs.
* Final Accuracy: ~100%
* The model successfully learns the XOR pattern.


### Approach

In this project, I built a small neural network from scratch to solve the XOR problem. First, I designed a simple architecture with one hidden layer because XOR cannot be solved using a single linear equation.
Then, I initialized the weights randomly and performed forward propagation to generate predictions. After that, I calculated the error using a loss function and used backpropagation to understand how much each weight contributed to that error.
Finally, I updated the weights using gradient descent and repeated this process for multiple epochs until the loss reduced and the model achieved high accuracy.
In short, the approach was:
Design → Predict → Measure Error → Adjust → Repeat → Evaluate.






