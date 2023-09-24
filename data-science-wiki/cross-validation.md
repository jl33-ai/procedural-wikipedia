# Cross-Validation :mag_right: :chart_with_upwards_trend:
#### Created by @jl33-ai 👦🏻

Cross-validation is commonly used in machine learning to estimate the skill of a machine learning model on unseen data, more specifically to estimate how accurate a predictive model will perform in practice.

---

### Overview :book:

- Cross-validation is a technique that provides an accurate measure of the performance of a machine learning model.
- It generally involves dividing your data into subsets and then running your machine learning algorithms on different subsets as train and test datasets.
- A key advantage of cross-validation is that it allows you to use your entire dataset for both training and testing, which can be particularly useful when you have limited data.

---

### Types of Cross-Validation :triangular_ruler:

1. **Train/Test Split**: Useful for large datasets, the data is split into two sets: 'train' and 'test'. The model is trained on the 'train' data and scored on the 'test' data. 

2. **K-fold Cross-Validation**: The data is divided into 'k' subsets. The holdout method is repeated 'k' times with each subset serving as the test set once. K-fold cross-validation is particularly useful when you don't have a lot of data and want to make the most of it for training and testing.

3. **Leave One Out Cross-Validation (LOOCV)**: A particular case of k-fold cross-validation where 'k' equals to the total number of your samples. Essentially, each sample gets to be a test set on its own with all other samples forming a training set. This method is highly computationally expensive and should be used on small datasets.

---

### Step-by-Step Guide :footprints:

1. **Split the Data**: Split the dataset into 'k' groups or folds. For example, if we have k=5, this would result in 5 sets of slices from the dataset.

2. **Train and Test**: For each unique group:
   - Take one group as a test set
   - Take the remaining groups as a training set
   - Fit a model on the training set and evaluate it on the test set
   - Retain the test set evaluation score and discard the model.

3. **Result**: The result of k-fold cross-validation is often given as the mean of the model evaluation scores, which is a more robust measure compared to other methods like Train/Test Split.

---

### Python Code Example :computer:

To perform K-fold cross-validation, you can use the cross_val_score function from `sklearn.model_selection`. See the example below:

```python
from sklearn.model_selection import cross_val_score
from sklearn.datasets import load_iris
from sklearn.ensemble import RandomForestClassifier

iris = load_iris()
clf = RandomForestClassifier()
scores = cross_val_score(clf, iris.data, iris.target, cv=5) # 'cv = 5' means you're doing 5-fold cross validation
print(scores)
```

This script will print 5 scores (because we set 'cv=5') which can be averaged to provide a more accurate view of the model's actual performance. The values that 'cross_val_score'returns are accuracy scores.

---

### Conclusion :tada:

Cross-validation offers a way to harness your data more effectively, especially when dealing with small datasets. Not only that, it provides a better generalized evaluation of your model. Always use cross-validation for a fair and truthful assessment of your model’s performance.