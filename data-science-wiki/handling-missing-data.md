
Created by [@jl33-ai](https://github.com/jl33-ai) 👦🏻

Missing data in datasets is a common problem and a critical issue to manage in any data analysis process. They can stem from various reasons including lack of information, data collection malfunctions, human error, etc. This guide will walk you through several methods of handling missing data.

## Contents 

1. [Identifying Missing Values](#identifying-missing-values)
2. [Dealing with Missing Data](#dealing-with-missing-data)
   - [Dropping Missing Values](#dropping-missing-values)
   - [Filling in Missing Values](#filling-in-missing-values)
   - [Predicting Missing Values](#predicting-missing-values)
3. [Conclusion](#conclusion)
4. [References](#references)

----

## Identifying Missing Values 🔍

Before dealing with missing data, you need to identify them first. In pandas, the isnull() function is used to check missing data. 

```python
import pandas as pd

df = pd.read_csv('your_data.csv')
missing_values = df.isnull().sum()
```

----

## Dealing with Missing Data ⛑

### Dropping Missing Values 🗑

One conventional method to deal with missing data is to simply remove instances/cases with missing data altogether.

```python
df.dropna(inplace=True)
```

This method is not generally recommended as it could potentially remove a lot of data, affecting the model's performance.

### Filling in Missing Values 🕳

Another common method is filling missing data with meaningful values like mean, median or the most frequently occurring value (mode).

```python
# Filling with mean
df.fillna(df.mean(), inplace=True)

# Filling with median
df.fillna(df.median(), inplace=True)

# Filling with mode
df.fillna(df.mode().iloc[0], inplace=True)
```

### Predicting Missing Values 🧙

A more complex method involves using machine learning techniques to predict the missing values based on other data.

For example, we could use `K-Nearest Neighbors` (KNN) method to fill missing values.

```python
from sklearn.impute import KNNImputer

imputer = KNNImputer(n_neighbors=5)
df = pd.DataFrame(imputer.fit_transform(df), columns = df.columns)
```

----

## Conclusion 🏁

Choosing the right method for handling missing data depends on the specific analysis you're conducting, the nature of your data and the extent of the missing data. Remember that not all methods are suited for all situations, and a method that works great in one context might not work as well in another.

## References 📚

1. [Pandas: Working with missing data](https://pandas.pydata.org/pandas-docs/stable/user_guide/missing_data.html)
2. [Handling Missing Data](https://towardsdatascience.com/handling-missing-data-8646b18db0d4)