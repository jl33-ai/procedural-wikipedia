# Multi-Layer Perceptron (MLP) 🧠
Created by @jl33-ai 👦🏻

## 🚀 Introduction
Multi-Layer Perceptron (MLP), also known as a feedforward artificial neural network, significantly improves the capacity of the network structure beyond the simple perceptron. 

## 💡 Key Features
1. Multiple layers: MLP consists of at least three layers of nodes - Input, Hidden, and Output layers.
2. Non-linear Activation Function: MLP uses a nonlinear activation function, mainly Relu, sigmoid, or tanh.
3. Capable of modeling complex patterns: MLP can model (approximate) functions that can separate data which is not linearly separable.

## 📚 Table of Contents

- [MLP Architecture](#mlp-architecture)
- [Activation Functions](#activation-functions)
- [Example](#example)
- [References](#references)

## 💼 MLP Architecture

MLP includes multiple layers of neurons (nodes) <b>with at least one (usually more than one) hidden layer</b>. Each layer is fully connected to the next one. Here is a brief explanation on each layers:

- <b>Input Layer:</b> This is the first layer, where the model receives its input.
- <b>Hidden Layer:</b> Layers that perform computations and transfer information from the input nodes to the output nodes.
- <b>Output Layer:</b> This is the final layer that produces the result for given inputs.

```markdown
        Input Layer      Hidden Layer      Output Layer
                .----.       .----.    .
                |    |----->|    |    |.
                '----'       '----'    ||
                .----.       .----.    ||
                |    |----->|    |    |'
                '----'       '----'    |
```

## 🌈 Activation Functions
- <b>Sigmoid:</b> It is a squashing function that transforms the input into a range between 0 and 1.
- <b>Tanh:</b> It is similar to the sigmoid function, but squashes the input into a range between -1 and 1.
- <b>ReLU (Rectified Linear Units):</b> It transforms the input to the maximum of either 0 or the input itself. This function is the most used activation function since it reduces the likelihood of the gradient to vanish.

## 📜 Example

Here is an example of how to build a basic MLP model using sklearn for the classification task.

```python
from sklearn.neural_network import MLPClassifier
from sklearn.datasets import make_classification
from sklearn.model_selection import train_test_split

# Create dataset
X, y = make_classification(n_samples=100, random_state=1)

# Split dataset
X_train, X_test, y_train, y_test = train_test_split(X, y, stratify=y, random_state=1)

# Define MLP Classifier
clf = MLPClassifier(random_state=1, max_iter=300)

# Train Model
clf.fit(X_train, y_train)

# Generate Predictions
predictions = clf.predict(X_test)
```

## 📚 References

- [Scikit-Learn Documentation](https://scikit-learn.org/stable/modules/neural_networks_supervised.html)

# MLP #MachineLearning #ArtificialNeuralNetwork #sklearn #Python