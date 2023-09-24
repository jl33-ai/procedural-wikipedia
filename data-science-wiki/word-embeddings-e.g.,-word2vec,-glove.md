# Word Embeddings: Word2Vec and GloVe Tutorial 📚💻
---
###### Created by @jl33-ai 👦🏻

## Overview 📋
Word embeddings are basically a form of word representation that bridges the human understanding of language to that of machines. Word embeddings are distributed representations of text in an n-dimensional space. These are essential for solving most NLP problems.

Two primary word embeddings techniques are: 
1. `Word2Vec`
2. `GloVe` (Global Vectors for Word Representation)

---

## Tags 🏷️
* `#Word2Vec` 
* `#GloVe`
* `#NLP` 
* `#Python` 
* `#Machine-Learning` 

---

## Word2Vec 📝

`Word2Vec` is a shallow, two-layer neural networks which is trained to reconstruct linguistic contexts of words. It takes as its input a large corpus of text and produces a vector space, typically of several hundred dimensions. Each unique word in the corpus being assigned a corresponding vector in the space.

* **Continuous Bag of Words (CBOW)**

    In CBOW model, the distributed representations of context (or surrounding words) are combined to predict the word in the middle. 

    Example:
    ![CBOW](https://miro.medium.com/max/700/0*VPIPZ-7_naXNbV7s.png)

* **Skip-Gram model**

    In Skip-gram model, the distributed representation of the input word is used to predict the context. 

    Example:
    ![Skip-Gram](https://miro.medium.com/max/700/0*V-Uzu6LV8-i78Y4v.png)

---

## GloVe 📝

`GloVe` (Global Vectors for Word Representation), is a word embedding technique based on factorizing a matrix of word co-occurrence statistics. Its main benefit over Word2Vec is it takes into account the global statistical information of the corpus in generating word vectors, hence the name *Global Vectors*.

The core concept behind GloVe is it leverages both global statistical information (total occurrences of words) and local information (specific word-context pairs).

Example:
![GloVe](https://miro.medium.com/max/1838/0*8nn_yK3CwRFD1cLe.jpg)

---

## Useful Links and References 📚
- [Word2Vec Paper](https://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf)
- [GloVe Paper](https://nlp.stanford.edu/pubs/glove.pdf)
- [Word2Vec Explained](http://mccormickml.com/2016/04/19/word2vec-tutorial-the-skip-gram-model/)
- [GloVe: Global Vectors for Word Representation](https://nlp.stanford.edu/projects/glove/)