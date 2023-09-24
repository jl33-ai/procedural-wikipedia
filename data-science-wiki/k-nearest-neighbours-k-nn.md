# K-Nearest Neighbours (K-NN)
Created by @jl33-ai 👦🏻

K-Nearest Neighbours, or K-NN, is a type of instance-based learning, or lazy learning where the function is only approximated locally and all the computations are performed, when we do the actual classification. 

---

## Table of Contents 📖
1. [Introduction](#introduction-🎯)
2. [Process](#process-💻)
3. [Choosing a value for K](#choosing-a-value-for-k-🎲)
4. [Pros and Cons](#pros-and-cons-⚖️)
5. [Applications](#applications-🚀)
6. [Example](#example-🔤)

---

## Introduction 🎯

K-NN algorithm is a type of instance-based learning where the function is approximated locally, and all computation is deferred until the function evaluation. It is among the simplest of all machine learning algorithms, both to understand and to implement.

---

## Process 💻

- Load the data
- Initialize K to your chosen number of neighbors
- For each example in the data
  - Calculate the distance between the query example and the current example from the data.
  - Add the distance and the index of the example to an ordered collection
- Sort the ordered collection of distances and indices in ascending order by the distances
- Pick the first K entries from the sorted collection
- Get the labels of the selected K entries
- If regression, return the mean of the K labels. If classification, return the mode of the K labels 

---

## Choosing a value for K 🎲

Selecting the K in K-NN algorithm is mostly selected by the square root of the number of entries. However, always check the accuracy of your model with different K values keeping in mind that a smaller value of K means that noise will have a higher influence on the result and a large value make it computationally expensive. 

---

## Pros and Cons ⚖️

### Pros
- The algorithm is simple and easy to implement.
- There's no need to build a model, tune several parameters, or make additional assumptions.
- The algorithm is versatile. It can be used for classification, regression, and search.

### Cons
- The algorithm gets significantly slower as the number of examples and/or predictors/independent variables increase.
- It is sensitive to irrelevant features and the scale of the data.

---

## Applications 🚀

- Economic Forecasting
- Data Compression
- Genetics: Genetic Nearest Neighbor
- Recommendation Systems 

---

## Example 🔤

```python
from sklearn.neighbors import KNeighborsClassifier
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split

iris = load_iris()

X_train, X_test, y_train, y_test = train_test_split(iris['data'], iris['target'], random_state = 0)

model = KNeighborsClassifier(n_neighbors=1)

model.fit(X_train, y_train)

prediction = model.predict(X_test)
```

---

## Concluding Thoughts 🎈

K-NN algorithm is uncomplicated and elementary but powerful. Foundamental understanding of K-NN algorithm is an essential step for a Data Scientist or Machine Learning Engineer.

---