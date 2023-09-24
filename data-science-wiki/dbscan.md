
`Created by @jl33-ai 👦🏻`

DBSCAN is a density-based algorithm that identifies and groups together points in close proximity to each other, and points in low density regions are considered as noise/outlier. 

## Table of Contents
1. [Concepts](#concepts)
2. [Advantages and Disadvantages](#advantages-and-disadvantages)
3. [Parameters](#parameters)
4. [Example](#example)
5. [Use Cases](#use-cases)

## Concepts <a name="concepts"></a>

DBSCAN algorithm involves the following concepts:

- **Core Points**: In DBSCAN, a point is a core point if there are atleast 'min_samples' points within a radius of 'eps' to it (including the point itself).

- **Border Points**: A point which has fewer than 'min_samples' within its 'eps' neighborhood, but lies within the 'eps' radius of another core point is known as Border point.

- **Noise/Outlier**: A point which is neither a Core nor a Border point is a Noise point.

![DBSCAN concepts](https://miro.medium.com/max/875/0*FeIp1t4uEcWkLxlv.png)


## Advantages and Disadvantages <a name="advantages-and-disadvantages"></a>

### Advantages

- DBSCAN does not require to specify the number of clusters.
- DBSCAN can find arbitrarily-sized and arbitrarily-shaped clusters.
- DBSCAN has a notion of noise.

### Disadvantages

- DBSCAN is not good with handling high-dimensional data.
- If the dataset has varying density, DBSCAN will not be able to identify the clusters properly, because it's hard to define a global 'eps' and 'min_samples' that fits all density.

## DBSCAN Parameters <a name="parameters"></a>

DBSCAN algorithm uses two parameters:

- **`eps`**: This is the maximum distance between two samples for them to be considered as in the same neighborhood.

- **`min_samples`**: The number of samples (or total weight) in a neighborhood for a point to be considered as a core point. This includes the point itself.

## Example <a name="example"></a>

```python
from sklearn.datasets import make_moons
from sklearn.cluster import DBSCAN
import matplotlib.pyplot as plt

X, y = make_moons(n_samples=500, noise=0.1)
model = DBSCAN(eps=0.3, min_samples=5)
model.fit(X, y)
plt.scatter(X[:, 0], X[:, 1], c=model.labels_)
plt.show()
```

## Use Cases <a name="use-cases"></a>

DBSCAN can be used in many areas including:

- **Anomaly detection**: DBSCAN can be used to detect fraud detection, data cleaning, public health...

- **Image processing**: Using DBSCAN for image segmentation.
