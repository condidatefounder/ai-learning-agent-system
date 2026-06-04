# Neural Network Notes

## Backpropagation

Backpropagation computes gradients layer by layer from the output back to earlier layers. It uses the chain rule to connect how each weight, bias, and activation affects the final loss.

## Chain Rule

The chain rule explains how the derivative of a composed function is calculated. In neural networks, each layer is a function composed with the next layer, so the chain rule allows the model to propagate error signals backward.

## Gradient Descent

Gradient descent updates model parameters in the opposite direction of the gradient. The learning rate controls the step size, and a poor learning rate can make training slow or unstable.

## Activation Functions

Activation functions introduce non-linearity into neural networks. Common examples include sigmoid, tanh, ReLU, and softmax.

## Overfitting

Overfitting happens when a model performs well on training data but poorly on unseen data. Common mitigation methods include regularization, dropout, early stopping, and more representative training data.
