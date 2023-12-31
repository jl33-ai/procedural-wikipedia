# procedural-notes

📚 Used a combination of **recursion and generative AI** to autonomously and procedurally create an entire mini-wikipedia notebook from a single prompt as a **`proof of concept`**.

`Topic -> Generate topic tree -> generate a fully formed .md markdown file for each concept, interlinked`

`💬->📕📗📘📙📗->🌐`

# Concepts used: 
**Recursion:** To traverse nested list of semantic topcis

**Generative AI:** use of the OpenAI API to use a predefined engineered model, which is told to output a library of .markdown files in your directory. 

These fully formatted notepages can then be viewed in Obsidian, GitHub, or any markdown previewer. 

Technically this could be applied to anything: 
- Enter the overarching topic of the wikipedia page
- The number of subtopics you would like
- Specify directory
- Preferences
  - Emojis
- [ ] Add folder functionality
- [ ] Better structure control
- [ ] Create a GUI
 
# Results:
A complete, interlinked, tagged, completely 'original' mini-wiki of Data Science concepts 

<img width="727" alt="image" src="https://github.com/jl33-ai/procedural-notes/assets/127172022/ee532e01-0fa4-4ccf-bb75-49eab6dcf3e7">

![image](https://github.com/jl33-ai/procedural-notes/assets/127172022/fb177b14-ddff-4fdc-a5dc-f8ed210e579d)

<img width="1401" alt="image" src="https://github.com/jl33-ai/procedural-notes/assets/127172022/eabfe643-a9fd-4217-83e6-85040c40173d">


# Complete Example
📃 **`A complete example output for the concept 'Support Vector Machines:`**

# Support Vector Machines
Created by @jl33-ai 👦🏻

## Table of Contents
1. [Introduction](#intro)
2. [How SVM Works](#svmwork)
3. [Advantages and Disadvantages](#advdisadv)
4. [Practical Applications](#applications)
5. [Working Example](#example)

---
<a id='intro'></a>
## 1️⃣ Introduction 

Support Vector Machines (SVM) are a set of supervised learning methods used for classification, regression and outliers detection. SVMs are one of the most robust prediction methods.

`Tags: Classification, Supervised learning, Robust prediction`

---

<a id='svmwork'></a>
## 2️⃣ How SVM Works ‍‍💁‍♀️

- SVM model is a representation of different classes in space, separated by as wide as possible margin.
- New examples are then mapped into that same space and predicted to belong to a category based on the side of the margin they fall.
- These points are called vectors, and the space is divided by using hyperplanes.

**Diagram**

```python
  Negative class (-)                           Positive class (+)
1 ------------------------| Support Vector |---------------------3
                         -|---------------|- 
                      -   |               |   -
                   -      |               |      -
                -         |               |         -
             2         -  |  Hyper Plane   |  +         4
                -         |               |         -
                   -      |               |      -
                      -   |               |   -
                         -|---------------|-       
1 ------------------------| Support Vector |---------------------3
```
 
`Tags: Support Vectors, Hyperplane, Space, Categories`
    
---

<a id='advdisadv'></a>

## 3️⃣ Advantages and Disadvantages 💼👎

**Advantages**
- Effective in high dimensional spaces.
- Uses a subset of training points, so it is also memory efficient.
- Different kernel functions can be specified for the decision function.

**Disadvantages**
- If the number of features is much greater than the number of samples, the method may perform poorly.
- SVMs do not directly provide probability estimates.

`Tags: Pros and Cons, Features, Samples, Kernel Functions`

---

<a id='applications'></a>
## 4️⃣ Practical Applications 🛠

- Text classification tasks with many features, SVMs can yield a more robust model.
- Hand-written characters can be recognized using SVM.

`Tags: Text Classification, Character Recognition, Use Cases`
    
---

<a id='example'></a>
## 5️⃣ Working Example 🧑‍💻

```python
# Loading necessary libraries
from sklearn import svm, datasets
from sklearn.model_selection import train_test_split
from sklearn.metrics import confusion_matrix

# Load Iris dataset
iris = datasets.load_iris()
X = iris.data
y = iris.target

# Split dataset into training and test data
X_train, X_test, y_train, y_test = train_test_split(X, y, random_state=0)

# Create SVM classifier
classifier = svm.SVC(kernel='poly', C=1).fit(X_train, y_train)

# Make predictions
y_pred = classifier.predict(X_test)

# Evaluate the model
print(confusion_matrix(y_test, y_pred))
```

`Tags: Python, Sklearn, SVM, Example, Code`

---
























