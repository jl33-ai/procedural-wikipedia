Created by @jl33-ai 👦🏻

## 💡Overview 

This notebook aims to introduce and explore sentiment analysis by implementing several machine learning models. 

## 📋 Table of Contents 

1. [Introduction](#introduction)
2. [Toolkit](#toolkit)
3. [Dataset](#dataset)
4. [Preprocessing](#preprocessing)
5. [Modeling](#modeling)
6. [Evaluation](#evaluation)
7. [Conclusion](#conclusion)


### Introduction <a name="introduction"></a>
Sentiment Analysis, sometimes referred to as Opinion Mining, is the use of natural language processing, text analysis and computational linguistics to identify and extract subjective information from source materials. 

- It is used commonly in social media monitoring, allowing us to learn about the wider public opinion on certain topics. 

### Toolkit <a name="toolkit"></a>
The major tools and libraries we will be using include: 

- Python 🐍 
- Pandas 🐼 
- Scikit-learn 🛠️
- NLTK 📚

### Dataset <a name="dataset"></a>
The dataset we will be using in this project is the Twitter Sentiment Analysis dataset, essentially a large collection of tweets that have been manually annotated for sentiment. 

- It contains tweets marked as positive 🌟, negative 🚫, or neutral ⏺️.

### Preprocessing <a name="preprocessing"></a>
Prior to training our sentiment analysis models, we need to preprocess our text data. Here's an overview of the steps involved: 

1. Tokenization 📝
    - This is the process of breaking down the text into individual words (or tokens). 
    - Example: "I love playing football" -> ["I", "love", "playing", "football"]
    
2. Stop word removal 🚫
    - Removing common words that don't carry much useful information. 
    - Example: ["I", "love", "playing", "football"] -> ["love", "playing", "football"]

3. Lemmatization 📘
    - It is the process of reducing words to their base or root form.
    - Example: "am", "are", "is" -> "be"; "car", "cars", "car's", "cars'" -> "car"

### Modeling <a name="modeling"></a>
For this project, we will use model following machine learning models for sentiment analysis:

1. Naive Bayes Model
2. Logistic Regression
3. Support Vector Machine
4. Random Forest 

### Evaluation <a name="evaluation"></a>
The performance of the models will be evaluated using the following metrics:

- Validations accuracy 📈
- Confusion Matrix 💡
- ROC Curve 📊

### Conclusion <a name="conclusion"></a>