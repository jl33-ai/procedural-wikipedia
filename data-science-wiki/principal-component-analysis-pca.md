Created by @jl33-ai 👦🏻

---

Principal Component Analysis (PCA) is a statistical technique which helps in simplifying the data with high dimensions (high number of features) into a data with lower dimensions.

---

## Contents 📋
- [Introduction to PCA](#introduction)
- [How PCA works](#working)
- [Use cases](#use-cases)
- [Pros and Cons](#pros-cons)
- [Code Example](#code-example)

---

### <a name="introduction"></a>1. Introduction to PCA 💡
- PCA is used to overcome features redundancy in a data set.
- These features are low dimensional in nature.
- These features a.k.a components are a resultant of normalized linear combination of original predictor variables.
- These components aim to capture as much information as possible with high explained variance.

---

### <a name="working"></a>2. How PCA works 💼
1. Normalize the data.
2. Calculate the covariance matrix.
3. Calculate the eigenvalues and eigenvectors.
4. Sort the eigenvalues.
5. Choose top k eigenvectors.
6. Transform the original n dimensional data points into k dimensions.

---

### <a name="use-cases"></a>3. Use cases🎯
- Useful in exploratory data analysis and predictive models.
- Used for filtering noise from data, and making the data understanding while visualizing.
- Used in application areas such as face recognition, image compression.

---

### <a name="pros-cons"></a>4. Pros and Cons📝
#### Pros
- Removes Correlated Features: In a real world scenario, it is very often to get correlated features. PCA removes the correlation between the features.
- Improves Algorithm Performance: With fewer features, the performance of the algorithm enhances.
- Reduces Overfitting: Less redundant data implies less chance of falling into the overfitting trap.
- Improves Visualization: It's very tough to visualize and interpret a data in higher dimensions.

#### Cons
- Independent variables become less interpretable: After applying PCA, your original features will turn into Principal Components which are the linear combination of your original features. Principal Components are not as readable and interpretable as original features.
- Data standardization is must before PCA.
- Information Loss.

---

### <a name="code-example"></a>5. Code Example in Python using Scikit-Learn 🐍
```python
from sklearn.decomposition import PCA
from sklearn import datasets

# load dataset
data = datasets.load_iris()
X = data.data

# initialize PCA with first two components
pca = PCA(n_components=2)

# fit and transform data
X_pca = pca.fit_transform(X)
```

> For details about each lines of code, you can follow the [Scikit Learn Official Docs](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html).

---

## Conclusion 🏁
PCA is a handy technique when dealing with high dimensional data. It helps to simplify things but should be used wisely as it can lead to information loss.

---
