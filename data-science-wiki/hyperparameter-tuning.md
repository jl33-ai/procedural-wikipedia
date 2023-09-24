
### Contents
1. [Overview](#overview)
2. [Types of Hyperparameters](#types)
3. [Techniques for Hyperparameter Tuning](#techniques)
4. [Examples](#examples)
5. [Tips and Guidance](#tips)

> __Created by @jl33-ai 👦🏻__

---

## 💡 Overview <a id="overview"></a>

Hyperparameters are parameters that are not learned from the data but are set prior to the start of the learning process. They directly control the behaviour of the training algorithm and have a significant impact on the performance of the model. Therefore, it's crucial to establish an efficient technique for their tuning.

---

## 📚 Types of Hyperparameters <a id="types"></a>

1. **Learning Rate**: This hyperparameter is used in the gradient descent optimization algorithm, which controls the step size taken to reach the global minimum.
2. **Number of Epochs**: The number of times the learning algorithm will work through the entire training dataset.
3. **Batch Size**: The total number of training examples present in a single batch.
4. **Number of Hidden Layers and Neurons in Neural Network**: The intermediate layers between input and output layers.
5. **Regularization Parameters**: It is used to prevent overfitting in a model.
6. **Momentum**: This parameter helps in accelerating Gradient Descent.
   
---

## 🛠️ Techniques for Hyperparameter Tuning <a id="techniques"></a>

1. **Grid Search**: Exhaustively search through a specified subset of the hyperparameter space.
2. **Random Search**: Randomly sample the search space and evaluate sets from a specified probability distribution.
3. **Bayesian Optimization**: Technique that uses a probabilistic model to map the hyperparameters to a probability score on the objective function.
4. **Gradient-Based Optimization**: This technique uses the gradients of the hyperparameters to optimize with respect to the validation set performance.
5. **Evolutionary Algorithms**: Based on the principles of evolution and natural selection, this technique uses a process of mutation and combination to find the most optimal hyperparameters.

---

## 🧪 Examples <a id="examples"></a>

Here are examples of how you can perform hyperparameter tuning in popular Machine Learning libraries:

1. **Scikit-Learn**

```python
from sklearn.model_selection import GridSearchCV

# Hyperparameters to tune
param_grid = {'C': [0.1,1, 10, 100], 'gamma': [1,0.1,0.01,0.001,0.00001]}
grid = GridSearchCV(SVC(), param_grid, refit=True)
grid.fit(X_train, y_train)
```

2. **Keras**

```python
from keras.wrappers.scikit_learn import KerasClassifier
from sklearn.model_selection import GridSearchCV

# Function to create model, required for KerasClassifier
def create_model(optimizer='adam'):
    # create model
    model = Sequential()
    model.add(Dense(12, input_dim=8, activation='relu'))
    model.add(Dense(1, activation='sigmoid'))
    # Compile model
    model.compile(loss='binary_crossentropy', optimizer=optimizer, metrics=['accuracy'])
    return model

model = KerasClassifier(build_fn=create_model)
optimizers = ['rmsprop', 'adam']
epochs = [50, 100]
batches = [5, 10, 20]
param_grid = dict(optimizer=optimizers, epochs=epochs, batch_size=batches)
grid = GridSearchCV(estimator=model, param_grid=param_grid)
grid_result = grid.fit(X, Y)
```

---

## 💎 Tips and Guidance <a id="tips"></a>

* Always normalise or standardise your features before performing hyperparameter tuning.
* Train various simple models before moving to more complex ones.
* Use adequate validation strategies (like cross-validation) during the hyper parameter tuning.
* Tuning the model on a subset of the whole data can save time.
* Always keep an eye out for overfitting while tuning your hyperparameters.
