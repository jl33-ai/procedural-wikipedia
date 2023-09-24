> Created by @jl33-ai 👦🏻
_____

## Contents 
1. [Introduction](#introduction)
2. [How it works](#how-it-works)
3. [Implementation](#implementation)
4. [Compare with other dimensionality reduction algorithms](#compare)
5. [Limitations](#limitations)
6. [Tips for using](#tips)
7. [References](#references)

## 1. Introduction <a name='introduction'></a>
T-Distributed Stochastic Neighbor Embedding (t-SNE) is a machine learning algorithm used for dimensionality reduction. It is well-suited for the visualization of high-dimensional datasets 📊.

## 2. How it works <a name='how-it-works'></a>
* t-SNE initially calculates the similarity between points in the high-dimensional space and also in the corresponding low-dimensional space by using a probabilistic approach. The similarities in the high-dimensional space are calculated using Gaussian joint probabilities and the similarities in the low-dimensional space are calculated using Student’s t-distributions.
* The t-SNE algorithm then minimizes the divergence between these two distributions with respect to the locations of the points in the low-dimensional space using gradient descent.

## 3. Implementation <a name='implementation'></a>
Here is an implementation of t-SNE using sklearn in Python :

```python
from sklearn.manifold import TSNE

# Create a t-SNE instance
tsne = TSNE(n_components=2, random_state=0)

# Fit and transform the data
data_2d = tsne.fit_transform(data)
```

> Note: n_components define the number of dimensions in which we want to visualize the data and random_state is set for the sake of reproducibility.

## 4. Compare with other dimensionality reduction algorithms <a name='compare'></a>
* t-SNE vs PCA 👥: PCA is a linear dimension reduction technique that seeks to maximize variance and preserves large pairwise distances. In contrast, t-SNE is a probabilistic technique specifically designed for high-dimensional data that preserves only small pairwise distances or local similarities whereas PCA is a deterministic approach.

## 5. Limitations <a name='limitations'></a>
There are few potential limitations and things to consider while using t-SNE:
* t-SNE is not a deterministic technique, similar runs with similar parameters can produce different results.
* t-SNE can create clusters even when there are none.
* Interpretability problem, since t-SNE map does not preserve distances between widely separated clusters.

## 6. Tips for using t-SNE <a name='tips'></a>
* Perplexity Parameter 🤔: It can have a big effect on the output. A common value to use is 30, but it could be adjusted from anywhere in the range 5-50.
* Standardize Features ➗: Standardize the features before applying t-SNE, because t-SNE is not scale invariant.
* Multimodal Data ➕: If data is multimodal (has more than one "type" of data), consider applying t-SNE to each part of the data separately.

## 7. References <a name='references'></a>
* [Visualizing Data using t-SNE (Journal of Machine Learning Research 2008)](http://www.jmlr.org/papers/v9/vandermaaten08a.html)  
* [How to Use t-SNE Effectively (Distill 2016)](https://distill.pub/2016/misread-tsne/)