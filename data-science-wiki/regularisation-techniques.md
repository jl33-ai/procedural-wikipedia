
*Created by @jl33-ai 👦🏻*


In machine learning and statistics, regularisation techniques are helpful to reduce the error by fitting a function appropriately to the given training set and avoid overfitting. This document covers three main types of regularisation techniques: Ridge Regression (L2 Regularisation), Lasso Regression (L1 Regularisation), and Elastic Net.

## Table of Contents

1. [Ridge Regression (L2 Regularisation)](#ridge-regression)
2. [Lasso Regression (L1 Regularisation)](#lasso-regression)
3. [Elastic Net](#elastic-net)
4. [Comparison and Conclusion](#comparison-and-conclusion)


## Ridge Regression (L2 Regularisation) <a name="ridge-regression"></a>

Ridge Regression technique works by adding a penalty equivalent to the square of the magnitude of the coefficients. This reduces the low impact feature values and helps to reduce overfitting.

```python
from sklearn.linear_model import Ridge

ridge = Ridge(alpha=1.0)
ridge.fit(X_train, y_train)
```

### Advantages 🔍
- It prevents overfitting.
- It's effective when we have more features, because it will keep all of the features but reduces their values.

### Disadvantages 🚧
- It includes all features present in the model, thereby may include unnecessary features.


## Lasso Regression (L1 Regularisation) <a name="lasso-regression"></a>

Lasso (Least Absolute Shrinkage and Selection Operator) Regression works by adding a penalty equivalent to the absolute of the magnitude of the coefficients. This can lead to feature selection out of given features.

```python
from sklearn.linear_model import Lasso

lasso = Lasso(alpha=1.0)
lasso.fit(X_train, y_train)
```

### Advantages 🔍
- It can lead to a simpler model (some feature coefficients may become exactly zero).
- It performs feature selection, providing a sparse solution.

### Disadvantages 🚧
- It can lead to underfitting.


## Elastic Net <a name="elastic-net"></a>

Elastic Net is a type of regularisation regression that combines the penalties of L1 and L2 regularisation. This allows for learning a sparse model where few of the weights are non-zero like Lasso, while still maintaining the regularization properties of Ridge.

```python
from sklearn.linear_model import ElasticNet

elastic = ElasticNet(alpha=1.0)
elastic.fit(X_train, y_train)
```

### Advantages 🔍
- It balance between Ridge and Lasso Regression.
- It performs feature selection like Lasso and reduces magnitude like Ridge.

### Disadvantages 🚧
- It can suffer from double shrinkage, which leads to increased bias and poor predictions.


## Comparison and Conclusion <a name="comparison-and-conclusion"></a>

- **Ridge**: It reduces the coefficients for those predictors which are correlated to each other and not to the target variable.
- **Lasso**: It reduces some coefficients exactly to zero. Thus, this performs better where few predictors are significant.
- **Elastic Net**: Combines the penalties of L1 and L2 to balance between the two. 

Regularisation is a powerful technique to avoid overfitting by including penalties. The choice of whether to use L1, L2, or a combination (Elastic Net) depends on the specific application and domain.
