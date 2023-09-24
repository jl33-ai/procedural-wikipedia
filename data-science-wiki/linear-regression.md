# Linear Regression Tutorial 📈
#### Created by @jl33-ai 👦🏻
---

## Contents 
1. [Introduction To Linear Regression](#intro)
2. [Hypothesis Function](#hypo)
3. [Cost Function](#cost)
4. [Gradient Descent](#gd)
5. [Example Implementation](#exmp)
6. [Conclusion](#conc)

---

<a name="intro"></a>
## Introduction To Linear Regression 💼

Linear regression is one of the most commonly used predictive analysis techniques. The main purpose of linear regression is to find the best-fitting line through the points of a dataset.

Key Features:
* It is generally used when the relationship between variables is linear.
* It's easy to interpret and compute.
* It serves as a good jumping-off point for more complex algorithms.

---

<a name="hypo"></a>
## Hypothesis Function 👁‍🗨

In the context of linear regression, we use a Hypothesis Function to predict the output. For Linear Regression, we have:

`h(x) = theta_0 + theta_1 * x`

Here, 
* `h(x)` is the predicted output,
* `theta_0` is the bias term,
* `theta_1` is the weight for the input feature `x`,

---

<a name="cost"></a>
## Cost Function 💰

Cost Function (also known as Loss Function ) measures the difference between the actual value and the predicted value.

`J(theta_0, theta_1) = 1/2m * Σ (h(x^i) - y^i)²`

Here,
* `h(x^i)` is the predicted value for `i-th` instance,
* `y^i` is the actual value for `i-th` instance,
* `m` is the number of instances,

The goal is to minimize the Cost Function.

---

<a name="gd"></a>
## Gradient Descent 🎢

Gradient Descent is an optimization algorithm used to minimize the Cost Function. It iteratively tweaks the parameters of our Hypothesis Function in order to minimize the Cost Function to its minimum.

---

<a name="exmp"></a>
## Example Implementation 💻

In Python, applying Linear Regression is straightforward through the Scikit-Learn library. Here is a basic example:

```python
from sklearn.linear_model import LinearRegression
import numpy as np

# Create example data
X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
y = np.array([2, 4, 5, 4, 5])

# Initialize a LinearRegression model
model = LinearRegression()

# Fit the model to the data
model.fit(X, y)

# Predict some values
predictions = model.predict([[6], [7]])
print(predictions)
```

---

<a name="conc"></a>
## Conclusion 🏁

Linear Regression, while simple, is a powerful tool in the arsenal of a Data Scientist. With just a few lines of code, we can make useful predictions. As always, the quality of your results will depend on the quality of your data.

Tags: `#DataScience` `#MachineLearning` `#LinearRegression` `#Python`