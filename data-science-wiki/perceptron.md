**Created by @jl33-ai 👦🏻**

Perceptron is a fundamental concept in the world of Machine Learning and Neural Networks. It serves as the building block for more complex and deep neural networks. 🧠💡

This markdown is an effort to brief you about the concept of Perceptron in a simple and concise way. 

## What is Perceptron? 

The perceptron is a machine learning algorithm developed in 1957 by Frank Rosenblatt. It is a type of linear classifier, i.e., a classification algorithm that makes its predictions based on a linear predictor function combining a set of weights with the feature vector. 

![Image](https://upload.wikimedia.org/wikipedia/commons/thumb/3/31/Perceptron.svg/1200px-Perceptron.svg.png) 

## Working of Perceptron: 

- Basically, a perceptron works by taking several binary inputs, `x1, x2, ..., xn` and producing a single binary output. 

- In the simplest case, a perceptron uses a step function as an activation function. In the case of a binary classification problem, if the output is above a certain threshold, the perceptron would classify the input as the positive class; otherwise, it would classify it as the negative class. 

## Perceptron Learning Algorithm: 🛠

Here is a brief step-by-step guide to the Perceptron Learning Algorithm:

1. Initialize the weights and the threshold. Weights may be initialized to 0 or to a small random number. 

2. For each example j in our training set, perform the following steps over the input `xj and desired output dj.`

    a. Calculate the actual output:
        
        ```
        yj = prediction(xj, w, t)

        ```
        
    b. Update the weights:

        ```
        for each weight wi, update as: 

        wi = wi + η(dj − yj) xji

        ```

    Where `η` (eta) is the learning rate. 
  
## Example:

For the binary classification problem described above, the perceptron's classifier might look like this (using Python):

```python
class Perceptron:

    def __init__(self, input_length, weights=None):
        if weights==None:
            self.weights = np.ones(input_length) * 0.5
        else:
            self.weights = weights

    def unit_step_function(self, x):
        if x > 0.5:
            return 1
        return 0

    def __call__(self, inputs):
        weighted_input = self.weights * inputs
        weighted_sum = weighted_input.sum()
        return self.unit_step_function(weighted_sum)
  
p = Perceptron(2, np.array([0.5, 0.5]))
inputs = np.array([1, 1])
output = p(inputs)
print(output) # Output will be 1.
```

This is a simple implementation and the perceptron model tries to classify the input into two categories. Based on the sum of the weighted input, the unit step function decides whether the perceptron fires or not. 

## Conclusion 🏁
