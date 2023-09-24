# Hierarchical Clustering 👥🔝
Created by @jl33-ai 👦🏻

## Table of Contents 

1. [Introduction](#introduction)
2. [Types of Hierarchical Clustering](#types)
3. [Steps Involved in Hierarchical Clustering](#steps)
4. [Distance Metrics](#distance)
5. [Advantages and Disadvantages](#pros-cons)
6. [Example](#example)

## Introduction <a name="introduction"></a>

Hierarchical Clustering is a form of Machine Learning algorithm that builds a hierarchy of clusters. It starts by treating each observation as a separate cluster. Then, it repeatedly executes the following two steps:

1. Identifies the two clusters that are closest together.
2. Merges the two most similar clusters. 

We keep repeating the process until all the clusters are merged together. 

## Types of Hierarchical Clustering <a name="types"></a>

Hierarchical Clustering is typically of two types:

1. **Agglomerative Hierarchical Clustering**: This is a "bottom-up" approach - each sample starts in its own cluster and pairs of clusters are merged as one moves up the hierarchy.
2. **Divisive Hierarchical Clustering**: This is a "top-down" approach - all samples start in one cluster, and splits are performed recursively as one moves down the hierarchy.

## Steps Involved in Hierarchical Clustering <a name="steps"></a>

1. **Make Each Data Point a Single-Point Cluster** → That Forms N Clusters.
2. **Take the Two Nearest Data Points** and Make Them One Cluster → That Forms N-1 Clusters.
3. **Take the Two Nearest Clusters** and Make Them One Cluster → That Forms N-2 Clusters.
4. **Repeat Step-3** until there is Only One Cluster Left.

## Distance Metrics <a name="distance"></a>

Distance measure could be Euclidean, Manhattan, or Minkowski distance. The choice of distance metric largely depends on the dataset.

1. **Euclidean Distance**: It is the "ordinary" straight-line distance between two points. 
2. **Manhattan Distance**: This distance is the sum of the absolute differences of their coordinates.
3. **Minkowski Distance**: The Minkowski distance is a metric in a normed vector space.

## Advantages and Disadvantages <a name="pros-cons"></a>

**Advantages** 👍🏻
* No need to specify the number of clusters.
* Easy to implement and provides a visualization in dendrogram form.

**Disadvantages** 👎🏻
* Not suitable for large datasets.
* Sensitive to noise and outliers.

## Example <a name="example"></a>

Here's how Hierarchical Clustering might be implemented in Python:

```python
from sklearn.cluster import AgglomerativeClustering
import numpy as np
import matplotlib.pyplot as plt

# Create artificial data
X = np.random.rand(50,2)

# Create clustering model
cluster = AgglomerativeClustering(n_clusters=5, affinity='euclidean', linkage='ward')

# Fit data and predict 
cluster.fit_predict(X)

# Visualize clusters
plt.scatter(X[:,0],X[:,1], c=cluster.labels_, cmap='rainbow')
```
```
Note, that in this example we've decided to create 5 clusters but that's optional.

Feel easy to reach me at @jl33-ai for any queries. Happy clustering! 💫