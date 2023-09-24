# Ensemble Methods: Bagging and Boosting 👾
#### Created by @jl33-ai 👦🏻

## Table of Contents 📚
1. Introduction
2. Bagging
3. Boosting
4. Conclusion


## Introduction 🙋‍♂️
Ensemble methods are machine learning algorithms that rely on the "wisdom of the crowd"; that is, they aggregate the predictions of a group of predictors (classifiers or regressors), which are usually trained on different subsets of the same data. The main goals are to reduce bias and variance, improve predictions, and increase model stability.

Two major groups of ensemble methods are **Bagging** and **Boosting**.


## Bagging 💼
- Also known as Bootstrap Aggregating.
- Involves having each model in the ensemble vote with equal weight.
- Aimed at decreasing variance of the prediction by generating additional data for training from dataset using combinations with repetitions to produce multi-sets of the original data.
- Boosts performance by combining multiple low accuracy (or weak) models together to create a high accuracy (or strong) models.

#### Example: 📝
Random Forest is an example of a bagging model, it combines multiple low accuracy (or weak) decision trees to create a high accuracy (or strong) model.

```python
    from sklearn.ensemble import RandomForestClassifier
    clf = RandomForestClassifier(n_estimators=100, random_state=0)
    clf.fit(X_train, y_train)
    y_pred = clf.predict(X_test)
```


## Boosting ⬆️
- Involves incrementally building an ensemble by training each new instance to emphasize the training instances that previous models mis-classified.
- Aimed at reducing bias and variance in supervised learning.
- Boosting converts weak models to strong ones, typically by building a weighted average that weighs each prediction by its performance.

#### Example: 📝
XGBoost is an example of a boosting model, where new models are added to correct the errors made by existing models.

```python
    from xgboost import XGBClassifier
    clf = XGBClassifier(use_label_encoder=False)
    clf.fit(X_train, y_train)
    y_pred = clf.predict(X_test)
```


## Conclusion 🏁
- Bagging and Boosting both can lead to improved accuracy over prediction with single models.
- They both create a collection of models and predict based on the aggregation of the predictions from individual models.
- While bagging helps to decrease the model’s variance, boosting helps to decrease the model’s bias and variance.

#### Tags 🏷️
`#EnsembleMethods` `#MachineLearning` `#Bagging` `#Boosting` `#SupervisedLearning` `#RandomForest` `#XGBoost`