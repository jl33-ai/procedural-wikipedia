# Linear Discriminant Analysis (LDA)
> Created by @jl33-ai 👦🏻

____
## Table of contents

- [1. Introduction](#introduction)
- [2. How LDA works](#how-lda-works)
- [3. Use cases for LDA](#use-cases)
- [4. Python example](#python-example)
- [5. Pros and Cons](#pros-and-cons)
- [6. Conclusion](#conclusion)

____
## 1. Introduction <a name="introduction"></a>

Linear Discriminant Analysis (LDA) is a dimensionality reduction technique used as a preprocessing step in Machine Learning (ML) and pattern recognition 🕹. LDA aims to find a linear combination of features that characterises or separates two or more classes. 

----
## 2. How LDA Works <a name="how-lda-works"></a>

The basic idea of LDA is to project data points onto a line where:
* The classes of data points are well separated 🔍.
* Each class’s data points are close together 🧲.

LDA works under the following assumptions:
* Each sample class follows a Gaussian distribution 📊.
* All classes share the same covariance matrix 💹.

Here’s a simple step-by-step overview of how LDA works:
1. Compute the separability between different classes 🎯.
2. Project it into another dimension via a line (or a vector) 📈.
3. The projected points (with their class labels) are the desired, reduced-dimension data points that are used for further ML tasks ⚙️.

----
## 3. Use Cases for LDA <a name="use-cases"></a>

Here are some common use cases of LDA:
* Face recognition 🧑🏻‍💼.
* Text classification 💬.
* Image classification 🖼.
* Signal processing 📈.

----
## 4. Python Example <a name="python-example"></a>

Here's a simple example of how LDA can be used in Python:

```python
import numpy as np
from sklearn.discriminant_analysis import LinearDiscriminantAnalysis

# Two classes:
X = np.array([[-1, -1], [-2, -1], [-3, -2], [1, 1], [2, 1], [3, 2]])
y = np.array([1, 1, 1, 2, 2, 2])

# LDA fit
lda = LinearDiscriminantAnalysis()
lda.fit(X, y)

print(lda.predict([[-0.8, -1]]))
```

----
## 5. Pros and Cons <a name="pros-and-cons"></a>

**Pros:**
* Computationally efficient 🚀.
* Insensitive to small changes in training data 👍.

**Cons:**
* Assumes that all classes share the same covariance matrix, which may not always be the case 👎.
* Not suitable for non-linear separable classes 👀.

----
## 6. Conclusion <a name="conclusion"></a>

Linear Discriminant Analysis (LDA) is a powerful dimensionality reduction tool that can increase the efficiency of many Machine Learning tasks. However, it's important to remember the assumptions LDA relies on to draw conscious conclusions! 🎉