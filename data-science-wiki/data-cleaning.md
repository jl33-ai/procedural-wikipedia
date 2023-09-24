Created by @jl33-ai 👦🏻

In this guide, we'll cover how to conduct proper data cleaning for your datasets. Data cleaning, also referred to as "data cleansing" or "data scrubbing", is the process of identifying and resolving issues with data.

## Table of Contents

1. [Why is Data Cleaning Important? 💡](#importance)
2. [Data Cleaning Techniques 💻](#techniques)
3. [Common Tools for Data Cleaning 🛠️](#tools)
4. [Key Considerations for Data Cleaning 🤔](#consider)
5. [Data Cleaning Examples 💼](#examples)

<a name="importance"></a>
## 1. Why is Data Cleaning Important? 💡

- **Reduced errors**: Cleaning data helps to reduce the number of errors in the dataset.
- **Increased efficiency**: Having a clean dataset can make data analysis and predictive modeling more efficient.
- **Better decision-making**: Accurate data leads to more reliable results and decisions.

<a name="techniques"></a>
## 2. Data Cleaning Techniques 💻

There are several common techniques and approaches to clean your data:

- **Removing duplicates**: Duplicates can give an inaccurate representation of the data.
```python
df.drop_duplicates()
```

- **Handling missing values**: Missing data can skew the analysis. One standard approach is to fill in the missing data with the mean, median, or mode. Other options may include dropping the rows or columns with missing data.
```python
df.fillna(df.mean())
```

- **Data type conversions**: Ensure each column is of the correct data type for accurate calculations.
```python
df['ColumnName'] = df['ColumnName'].astype('int')
```

- **Handling outliers**: Outliers can distort the outcome of an analysis. There are multiple ways of detecting and handling outliers.
```python
Q1 = df.quantile(0.25)
Q3 = df.quantile(0.75)
IQR = Q3 - Q1
filter = (df >= Q1 - 1.5 * IQR) & (df <= Q3 + 1.5 *IQR)
df_no_outlier = df[filter]
```

<a name="tools"></a>
## 3. Common Tools for Data Cleaning 🛠️

Here are common tools to facilitate data cleaning in Python:

- **Pandas**: Provides data structures and functions needed to manipulate structured data.
- **NumPy**: Adds support for arrays, enabling mathematical and logical operations on arrays.
- **Matplotlib**: Used for creating static, animated, and interactive visualizations.

<a name="consider"></a>
## 4. Key Considerations for Data Cleaning 🤔

- **Never delete data**: Until it's proven beyond doubt that certain data is incorrect, keep it in a separate dataset. Data, once deleted, cannot be recovered.
- **Understand your data**: Know what's normal for the dataset to identify outliers.
- **Check duplicate data**: Duplicates might occur due to various reasons such as system errors or data merging.

<a name="examples"></a>
## 5. Data Cleaning Examples 💼

This section will describe a few simple examples of the data cleaning techniques mentioned above.

- Cleaning null values example:
```python
# Fill nulls with mean
df['ColumnName'].fillna((df['ColumnName'].mean()), inplace=True)
```

- Removing duplicates example:
```python
# Drop duplicate rows
df.drop_duplicates(inplace=True)
```

- Converting data types example:
```python
# Convert to datetime
df['date'] = pd.to_datetime(df['date'])
```
