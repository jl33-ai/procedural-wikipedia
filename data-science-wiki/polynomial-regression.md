
# Polynomial Regression in Machine Learning 🤖📚
### Created by @jl33-ai 👦🏻

## Introduction 

Polynomial regression is a type of regression analysis in which the relationship between the independent variable `x` and the dependent variable `y` is modelled as an `n`th degree polynomial. It is a form of linear regression in which the relationship between the independent variable `x` and the dependent variable `y` is modelled as an `n`th degree polynomial. 

## Contents
- [What is Polynomial Regression](#what-is)
- [Why Polynomial Regression](#why)
- [Use Cases](#use-cases)
- [Code Example](#code)
- [Pros and Cons](#pros-and-cons)
- [Conclusion](#conclusion)

<a name="what-is"></a>
## What is Polynomial Regression? 🤔

* Polynomial Regression is a form of regression analysis where the relationship between the independent variable `x` and the dependent variable `y` is modelled as an `n`th degree polynomial. It's a type of multiple linear regression.
* It's used to model relationships between variables that aren't linear. 
                   
<a name="why"></a>
## Why Polynomial Regression? 🎯

* Polynomial regression models can flexibly fit data where the relationship between variables is curvilinear. 
* It can model complex relationships which linear regression cannot.
* It can fit a wide range of functions.

<a name="use-cases"></a>
## Use Cases of Polynomial Regression 🛠

* Polynomial regression can be used in business for trend forecasting, or estimating the impacts of scale on operations.
* It's used in the field of medicine to examine the growth rates of diseases, or patient responses to treatment.
* It's commonly used in financial analysis and econometrics.

<a name="code"></a>
## Code Example 💻

Here is a small piece of code in Python using the scikit-learn library for a simple polynomial regression:

```python
import numpy as np
from sklearn.preprocessing import PolynomialFeatures
from sklearn.linear_model import LinearRegression

# data 
x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 3, 5, 8, 14])

# reshape
x = x[:, np.newaxis]
y = y[:, np.newaxis]

# polynomial features
polynomial_features = PolynomialFeatures(degree=2)
x_poly = polynomial_features.fit_transform(x)

# model
model = LinearRegression()
model.fit(x_poly, y)

# prediction
y_pred = model.predict(x_poly)
```
<a name="pros-and-cons"></a>
## Pros and Cons of Polynomial Regression 👍👎

Pros:
* Polynomial function has a wide range of function shapes such as quadratic, cubic, quartic, and many more.
* Polynomial provides the best approximation of the relationship between the dependent and independent variable.
* A broad range of function can be fit under it.

Cons:
* These are too sensitive to the outliers.
* The presence of one or two outliers in the data can seriously affect the results of a nonlinear analysis.
* In addition there are unfortunately fewer model validation tools for the detection of outliers in nonlinear regression than there are for linear regression.

<a name="conclusion"></a>
## Conclusion 📚

Polynomial Regression is a very handy form of linear regression that allows us to fit a model to datasets with non-linear relationships. It has wide use cases in the industry and will continue to be in future with the rise of ML and AI.
