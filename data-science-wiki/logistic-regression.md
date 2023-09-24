
**Created by @jl33-ai 👦🏾**

## Table of Contents

1. [Introduction](#introduction)
2. [The Math behind Logistic Regression](#math)
3. [Advantages and Disadvantages](#adv-disadv)
4. [Applications](#applications)
5. [Logistic Regression in Python](#python-example)
6. [Conclusion](#conclusion)


<a id='introduction'></a>
## Introduction 🎉

- Logistic regression is used when the dependent variable is categorical.
- In other words, logistic regression is used for classification problems, not regression problems.
- It’s called “logistic” because the core of the method is the logistic function.

<a id='math'></a>
## The Math Behind Logistic Regression 👩‍🔬

- The logistic regression takes an input `-b0 + b1*X1` and puts it into the logistic function.
- Logistic Function (Sigmoid function):

    ```shell
    g(z) = 1 / (1 + e^-z) 
    ```

- Being a regression algorithm, the output of a logistic regression is a number. For a binary classification problem, this number is transformed into a probability that the input sample belongs to class '1'.
- It uses the logistic function or sigmoid function to squeeze the output between 0 and 1. 


<a id='adv-disadv'></a>
## Advantages and Disadvantages of Logistic Regression 📈📉

**Advantages**:
- It is easier to implement, interpret, and very efficient to train.
- Makes no assumptions about distributions of classes in feature space.
- Provides probabilities for outcomes and it is simple to extend to multi-class classification.

**Disadvantages**:
- It assumes linearity of independent variables and target.
- It cannot handle a large number of categorical variables well.
- It is prone to overfitting.

<a id='applications'></a>
## Applications 🤖

- Logistic regression is widely used in various fields, including machine learning, medical fields, and social sciences. 
- It can be used to predict the risk of developing a given disease (based on inputs like eating habits, exercise habits, etc).
- It can be used in machine learning applications to predict whether an email is spam or not.

<a id='python-example'></a>
## Logistic Regression in Python (Example) 🧠

```python
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler

# assuming X and y are your features & labels
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.2, random_state = 42)

sc = StandardScaler()
X_train = sc.fit_transform(X_train)
X_test = sc.transform(X_test)

model = LogisticRegression(random_state=0)
model.fit(X_train, y_train)

y_pred = model.predict(X_test)
```
<a id='conclusion'></a>
## Conclusion 🏁

- Logistic Regression is a go-to method for binary classification problems (problems with two class values).
- It is easy-to-implement and with the proper preprocessing, it can achieve good results.
- It is crucial to properly tune your model, preselect predictors, avoid overfitting.

For further reading and more advanced topics, checkout the resources below:
- [Advanced Data Analysis from an Elementary Point of View](http://www.stat.cmu.edu/~cshalizi/ADAfaEPoV/ADAfaEPoV.pdf)