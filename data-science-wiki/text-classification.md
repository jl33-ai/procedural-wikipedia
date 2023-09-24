_Created by [@jl33-ai](https://github.com/jl33-ai) 👦🏻_

<br/>

Text classification is a commonly used technique in Natural Language Processing (NLP). It automatically classifies the text into one or more predefined categories. This notebook will provide a simple guide on how to use Python for text classification problems. 

Table of Contents
----------------------
- Dependencies
- Load Data
- Data Preprocessing
- Model Building
- Model Evaluation
- Conclusion

## Dependencies 📃
Ensure that following libraries are installed and correctly loaded:

```python
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.naive_bayes import MultinomialNB
from sklearn.metrics import accuracy_score, classification_report
```

## Load Data 📂
After the necessary dependencies, it's time to load the data. You will need a labeled dataset for training the text classification model.

```python
df = pd.read_csv("data/text_data.csv")
```

## Data Preprocessing 🛠️
In order to extract useful features from the text data, we need to clean and preprocess it.

1. Normalize the case: Convert all text to lowercase to maintain uniformity and avoid duplication based on casing.

2. Remove stop words: Stop words do not contribute much to the overall meaning of a document. Example, `the`, `and`, `is`, `in` etc.

3. Stemming or Lemmatization: Reducing derived words from their word stems. For example, `jumping` -> `jump`.

4. Vectorization: Convert texts into numerical vectors that can be easily understood by machine learning algorithms.

```python
# Example of vectorization
vectorizer = TfidfVectorizer()
X = vectorizer.fit_transform(df['text'])
```

## Model Building 🏗️
We will be using a multinomial naive bayes model for our text classification task. This is a commonly used model for text classification due to its simplicity and effectiveness.

```python
# Splitting data into testing and training
X_train, X_test, y_train, y_test = train_test_split(X, df['label'], test_size=0.2, random_state=42)

# Defining and training the model
model = MultinomialNB()
model.fit(X_train, y_train)
```

## Model Evaluation 🎯
After the model is trained, it's time to evaluate how it performs on unseen data (test data). This can be done using accuracy score and classification report functions.

```python
# Predicting using trained model
y_pred = model.predict(X_test)

# Evaluating the model
print(f'Accuracy: {accuracy_score(y_test, y_pred)}')
print(classification_report(y_test, y_pred))
```

## Conclusion 🎭
Text classification is a vital task in natural language processing. Python has a range of built-in libraries which make it relatively straightforward to build such a model. The above notebook is a simple guide to perform text classification tasks. It forms the basis which you can extend for solving complex problems.

---
