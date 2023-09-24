
Created by @jl33-ai 👦🏻


Text preprocessing is a critical step in working with machine learning and natural language processing (NLP) tasks. In this notebook, we will go through the steps involved in preprocessing text data for your model. 

## Table of Contents 📚

- [Introduction](#intro)
- [Lower-casing](#lowercase)
- [Removing Punctuation](#punctuation)
- [Removing Stop Words](#stopwords)
- [Stemming](#stemming)
- [Lemmatization](#lemmatization)
- [Tokenization](#tokenization)
- [Conclusion](#conclusion)

<a name="intro"></a>
## Introduction 👨‍🏫

Preprocessing text, in essence, means cleaning and formatting the text to be better understood by the algorithms. Following are the steps included in preprocessing. Let's elaborate them in a more detailed manner.

<a name="lowercase"></a>
## Lower-casing 📖

One of the initial steps in text cleaning involves converting all the text into lowercase. This avoids having multiple copies of the same word.

```python
text = "Natural Language Processing with PYTHON"
lowercased_text = text.lower()
print(lowercased_text)
# Output: "natural language processing with python"
```

<a name="punctuation"></a>
## Removing Punctuation ⏹️

Punctuation can provide additional context while in general text applications. However, in natural language processing tasks, it is often helpful to remove punctuation. 

```python
import string
text = "Hello, World!"
translator = str.maketrans('', '', string.punctuation)
no_punctuation = text.translate(translator)
print(no_punctuation)
# Output: "Hello World"
```

<a name="stopwords"></a>
## Removing Stop Words 🚦

Stop words in NLP are the common words like 'is', 'and', 'the' etc. Thankfully, libraries like NLTK come with pre-defined lists of stop words that we can use to remove from our text.

```python
from nltk.corpus import stopwords
stop_words = set(stopwords.words('english'))
text = "This is a sample sentence"
word_tokens = word_tokenize(text)
filtered_sentence = [w for w in word_tokens if not w in stop_words]
print(filtered_sentence)
# Output: ['This', 'sample', 'sentence']
```

<a name="stemming"></a>
## Stemming 🌱

Stemming refers to reducing a word to its word stem. For example, the stem of the word 'jumping' would be 'jump'. This can be useful in NLP for grouping similar words together.

```python
from nltk.stem import PorterStemmer
ps = PorterStemmer()
word = "jumping"
print(ps.stem(word))
# Output: "jump"
```

<a name="lemmatization"></a>
## Lemmatization 🍋

While stemming merely chops off the ends of the words, lemmatization takes into account the morphological analysis of words. So, 'better' would be converted to 'good'.

```python
from nltk.stem import WordNetLemmatizer
lemmatizer = WordNetLemmatizer() 
word = "better"
print(lemmatizer.lemmatize(word, pos ='a'))
# Output: "good"
```

<a name="tokenization"></a>
## Tokenization 🪙

Tokenization is the process of breaking the given text into smaller pieces called tokens.

```python
from nltk.tokenize import word_tokenize 
text = "Hello world"
print(word_tokenize(text))
# Output: ['Hello', 'world']
```

<a name="conclusion"></a>
## Conclusion 👨‍🎓

These represent a few of the most common steps for preprocessing text but keep in mind, not every step is needed every time. Depending on your specific project, some may not be necessary or you may need other preprocessing steps. Happy coding! 🎉
