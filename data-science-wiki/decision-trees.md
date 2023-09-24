#### Created by @jl33-ai :boy:

This document is all about understanding decision trees, its algorithms, its types and understanding what all of this looks like in Python.

---
## Table of Contents
- [Introduction](#introduction)
- [Types of Decision Trees](#types-of-decision-trees)
- [Algorithms](#algorithms)
- [Python Example](#python-example)

---
## Introduction <a name="introduction"></a>

A decision tree is one of the easiest and popular classification algorithms to understand and interpret. It can be utilized for both classification and regression kind of problems.

:white_check_mark: What are Decision Trees?

- Decision Trees are a type of Supervised Machine Learning where the data is continuously split according to a certain parameter.
- It is a versatile ML algorithm which can perform both classification and regression tasks.
- Plus, it can even perform multi-output tasks.

:bangbang: How does a decision tree work?

- Decision trees use multiple algorithms to decide to split a node into two or more sub-nodes. More on this later.

---

## Types of Decision Trees <a name="types-of-decision-trees"></a>

There are mainly two types of Decision Trees:

1. **Categorical Variable Decision Tree**: Decision Tree which has a categorical target variable then it called a categorical variable decision tree.
2. **Continuous Variable Decision Tree**: Decision Tree which has a continuous target variable then it is called Continuous Variable Decision Tree.

---

## Algorithms <a name="algorithms"></a>

There are few algorithms that we use for constructing a decision tree: 

1. **ID3 (Iterative Dichotomiser 3)**
2. **C4.5 (successor of ID3)**
3. **CART (Classification And Regression Tree)** 
4. **CHAID (Chi-square automatic interaction detection Performs multi-level splits when computing classification trees)** 

:bulb: We mainly use the CART algorithm in real practices!

---

## Python Example <a name="python-example"></a>

Before proceeding, ensure you have installed the necessary libraries: 
```python
!pip install numpy pandas sklearn
```

Here's a simple example of using Decision Trees with Python.

```
import numpy as np
import pandas as pd
from sklearn.model_selection import train_test_split 
from sklearn.datasets import load_iris
from sklearn import tree

# Load the iris dataset
iris = load_iris()

# Formulate the data with the feature names
data = pd.DataFrame(iris.data, columns=iris.feature_names)

# Split into training and testing sets (80-20 split)
X_train, X_test, y_train, y_test = train_test_split(data, iris.target, test_size=0.2)

# Create the Decision Tree Model
classifier = tree.DecisionTreeClassifier(random_state=1234)

# Train it (fitting the model)
classifier.fit(X_train, y_train)

# Use the model to predict the test dataset
y_pred = classifier.predict(X_test)

# Let's examine the output
print(y_pred)
```

Play around with the various parameters and hyperparameters to see how they affect the model's accuracy!

---
