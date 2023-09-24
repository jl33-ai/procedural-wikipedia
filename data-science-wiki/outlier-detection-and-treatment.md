# Outlier Detection and Treatment
###### Created by @jl33-ai 👦🏻

Outliers is a commonly used term by analysts and data scientists as they evaluate and clean data. An outlier is an observation that is unlike the other observations. It is rare, or distinct, or does not fit in some way. 

### Table of contents 📖
1. [Introduction](#Introduction)
2. [Types of Outliers](#Types-of-Outliers)
3. [Outlier Detection](#Outlier-Detection)
4. [Outlier Treatment](#Outlier-Treatment)
	

## Introduction 🎯

Outliers can be of two types: Univariate and Multivariate. Univariate outliers can be found when we look at a distribution of values in a single feature space. Multivariate outliers can be found in an n-dimensional space (of n-features). Looking at distributions in n-dimensional spaces can be very difficult for the human brain. 


## Types of Outliers 📝

There are three types of outliers:
* **Point outliers**: These are single data points that lay far from the rest of the distribution.
* **Contextual outliers**: These are data points that deviate significantly based on a certain context. 
* **Collective outliers**: These are collections of data points that deviate significantly as a group.

## Outlier Detection 👀

Here are some methods to detect outliers:
* **Z-Score**: If the Z-score of a data point is more than 3, it indicates that the data value is quite different from the other values. Such a data point can be an outlier.
* **IQR Score**: Any data point that falls below the Lower fence (Q1 – 1.5xIQR) or above the Upper fence (Q3 + 1.5xIQR) can be considered an outlier.

Example 📄:
```python
# Using Z-Score
from scipy import stats
z = np.abs(stats.zscore(boston_df))
threshold = 3
print(np.where(z > 3))
```

```python
# Using IQR
Q1 = boston_df.quantile(0.25)
Q3 = boston_df.quantile(0.75)
IQR = Q3 - Q1
print(IQR)
```

## Outlier Treatment 🛠

Removal or adjustment of outliers is a tough decision and a lot depends on the domain knowledge and the problem at hand. 

Some possible outlier treatment methods are:
1. **Deletion**: This is where you completely remove data points that are outliers.
2. **Transformation**: Where you apply a mathematical function to transform the values of outliers.
3. **Imputing**: This is where you replace the outliers with statistics such as mean or median.
4. **Binning**: Binning is the process of converting numerical variables into categorical counterparts.

Example 📄:
```python
# Outlier treatment
# replace every outlier on the lower side by the lower whisker
df[df < (Q1 - 1.5 * IQR)] = Q1 - 1.5 * IQR

# similarly replace every outlier on the upper side by the upper whisker
df[df > (Q3 + 1.5 * IQR)] = Q3 + 1.5 * IQR
```