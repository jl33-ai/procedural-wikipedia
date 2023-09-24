# Feature Engineering 🧮🛠️
#### Created by @jl33-ai 👦🏻

Feature engineering is a crucial step in the machine learning pipeline. It's the process of using domain knowledge to create features- vectors of machine-readable numeric or categorical values- that make machine learning algorithms work.

In this notebook, we will cover various feature engineering techniques.

---

## Table of Contents

- [Dealing with Categorical Values](#dealing-with-categorical-values)
- [Handling Numerical Values](#handling-numerical-values)
- [Dealing with DateTime Variables](#dealing-with-datetime-variables)

## Dealing with Categorical Values 🐈

Most of the Machine Learning models like to eat data in numerical format. One common type of non-numerical data is categorical data.

### One Hot Encoding

Involves separating the category into a binary format.

```python
pandas.get_dummies(df)
```

### Ordinal Encoding

Each unique category value is assigned an integer value.

```python
from sklearn.preprocessing import OrdinalEncoder
encoder = OrdinalEncoder()
df_encoded = encoder.fit_transform(df)
```

## Handling Numerical Values 🧮

Numerical data is the most common type of data you'll handle, but it too comes with its quirks.

### Rescaling

A common method is to rescale features to have a range between 0 and 1.

```python
from sklearn.preprocessing import MinMaxScaler
scaler = MinMaxScaler()
df_rescaled = scaler.fit_transform(df)
```

### Standardization

Make the distribution of values have a mean of 0 and a standard deviation of 1.

```python
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
df_standardized = scaler.fit_transform(df)
```

### Binning

This involves creating a new category feature from a numerical feature.

```python
bins = [0, 10, 20, 30, 40, 50, 100]
labels = ['0-10', '10-20', '20-30', '30-40', '40-50', '50+']
df['age_group'] = pd.cut(df.age, bins, labels = labels)
```

## Dealing with DateTime Variables 📅

Datetime variables can be broken down into several different features.

### Time Since

The difference between a certain date and the datetime feature.

```python
df['time_since'] = (pd.Timestamp('now') - df['date']).dt.days
```

### Decompose Datetime

A datetime can be broken down to year, month, day.

```python
df['year'] = df['date'].dt.year
df['month'] = df['date'].dt.month
df['day'] = df['date'].dt.day
```

---

And there you have it, some of the key feature engineering techniques you'll need. Explore and have fun experimenting! 🧪🎉
