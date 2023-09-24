##### _Created by @jl33-ai 👦🏻_

This document aims to provide a comprehensive yet concise overview of learning curves and how they connect to the bias-variance tradeoff in machine learning. We'll cover what these terms mean and how you can use them to improve your models.

 ---
## Table of Contents 📑
- [Learning Curves](#Learning-Curves-📈)
- [Bias-Variance Tradeoff](#Bias-Variance-Tradeoff-⚖️)
- [Connecting Learning Curves and Bias-Variance Tradeoff](#Connecting-Learning-Curves-and-Bias-Variance-Tradeoff-🔗)
- [Examples and Applications](#Examples-and-Applications-📝)
- [Conclusion](#Conclusion-🔚)

 ---
## Learning Curves 📈

Learning curves depict the performance of an ML model on both the training and validation datasets over time (or over the number of training instances).

1. `Training curve` **😀**: A plot that shows learning progression on the training dataset as the complexity of the model increases.
    - Usually starts at a perfect score of 1.0 and then decreases asymptotically.
    - Overfitting is indicated by a gap between training and testing performance.

2. `Validation curve` **😃**: A plot that represents the learning progress on the validation dataset.
    - Usually starts at a low score and then increases with model complexity, until reaching a peak, after which it then begins to decrease.
    - Underfitting is indicated by poor performance on both training and testing data.

**Remember**❗️: If the training score and validation score are both low, the estimator will be underfitted. If the training score is high and the validation score is low, the estimator is overfitting.

---

## Bias-Variance Tradeoff ⚖️

The bias-variance tradeoff is a critical concept in machine learning. It pertains to one of the most fundamental trade-offs: the one between overfitting (high variance) and underfitting (high bias).

1. `Bias` **👥**: Bias is an error from erroneous assumptions in the learning algorithm. High bias can cause an algorithm to miss the relevant relations between features and target outputs (underfitting).

2. `Variance` **🎲**: Variance is an error from sensitivity to small fluctuations in the training set. High variance can cause an algorithm to model the random noise in the training data, rather than the intended outputs (overfitting).

**Remember**❗️: There is a tradeoff at play here. Increasing the bias will decrease the variance. Increasing the variance will decrease the bias.

---

## Connecting Learning Curves and Bias-Variance Tradeoff 🔗

Learning curves give us a visual representation of the bias-variance tradeoff.

- If we are in a **high bias** situation (i.e., model is underfitting), the learning curves for both training and validation are close to each other but with high initial error and limited improvement or plateau.
- If we are in a **high variance** situation (i.e., model is overfitting), learning curve for the training data starts at a very low error, but there is a significant gap between the curves for the training and validation datasets.


---

## Examples and Applications 📝

Let's imagine we are using a decision tree model on our data:

- If we restrict the tree to very few splits, the model is not complex enough to capture all the patterns in the data, leading to high bias (underfitting). The learning curves would not improve significantly with more training instances.

- If we allow too many splits, the model becomes overly complex, and we start to capture noise rather than patterns, leading to high variance (overfitting). We would see a large gap between the learning curves for our training and validation datasets.


---

## Conclusion 🔚
