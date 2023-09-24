# Model Selection Techniques 🤔📊
### _Created by @jl33-ai 👦🏻_

Model selection is a crucial step in any data science workflow that can increase the performance and accuracy of your machine learning model.
This document aims to capture the most commonly used model selection techniques. 

## Table of Contents 📑
1. [Train Test Split](#train-test-split)
2. [Cross-Validation](#cross-validation)
3. [Bootstrap](#bootstrap)
4. [Information Criterion Approaches](#information-criterion-approaches)
5. [Regularization Methods](#regularization-methods)
6. [Nested Cross-Validation](#nested-cross-validation)

## Train Test Split 💔
In this approach, the dataset is split into two parts: 
- Training set (used for creating the model)
- Test set (used for testing the model)

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.25)
model.fit(X_train, y_train)
```

## Cross-Validation ✔️
This approach splits the dataset into `k` parts, or "folds". The model is trained on `k-1` folds, and the remaining fold is used for testing. 

```python
from sklearn.model_selection import cross_val_score

scores = cross_val_score(model, X, y, cv=5)
```

## Bootstrap 🎒
Bootstrap method is a resampling technique used to estimate statistics on a population by sampling a dataset with replacement.

```python
from sklearn.utils import resample

bootstrap = resample(data, replace=True, n_samples=10000)
```

## Information Criterion Approaches 🧠
These methods (like AIC and BIC) measure the goodness of fit of an estimated statistical model and include a penalty function for the number of parameters in the model.

Example with AIC:
```python
from sklearn.linear_model import LassoLarsIC

model_bic = LassoLarsIC(criterion='bic')
model_bic.fit(X, y)
```

## Regularization Methods ⚖️
These methods (like L1 & L2 and Elastic Net) incorporate a penalty term to the loss function thus adding a bias towards certain solutions.

Example with L1 (Lasso):
```python
from sklearn.linear_model import Lasso

model_lasso = Lasso(alpha=0.1)
model_lasso.fit(X,y)
```

## Nested Cross-Validation 🔂
Nested cross-validation (CV) is used to tune hyperparameters and avoid data leakage.

```python
from sklearn.model_selection import GridSearchCV, cross_val_score, KFold
inner_cv = KFold(n_splits=4, shuffle=True, random_state=2)
outer_cv = KFold(n_splits=4, shuffle=True, random_state=2)

grid = GridSearchCV(estimator=model, param_grid=p_grid, cv=inner_cv)
nested_score = cross_val_score(grid, X=X, y=y, cv=outer_cv)
```

Remember that the quality of your output has a direct connection with the **appropriate model selection**. Try different approaches to find out which works best for your data! 🎯💪