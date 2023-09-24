### Created by @jl33-ai 👦🏻

Pandas is a high-level data manipulation tool developed by Wes McKinney. It is built on the Numpy package and its key data structure is called the DataFrame. 

## Table of Contents:

1. [Introduction to Pandas](#introduction)
2. [Data Structures](#data-structure)
    - [Series](#series)
    - [DataFrame](#dataframe)
3. [Data Selection in DataFrame](#data-selection)
4. [Handling Missing Data](#missing-data)
5. [Data Manipulation with Pandas](#manipulation)
6. [Grouping and Aggregation](#grouping)
7. [Conclusion](#conclusion)


## Introduction to Pandas <a name="introduction"></a>

Pandas allows us to analyze data, prepare data, and even visualize data. It's often used with other libraries such as NumPy, Matplotlib.

To use pandas, you'll typically start with the following line of code:

```python
import pandas as pd
```

## Data Structures in Pandas <a name="data-structure"></a>

### Series <a name="series"></a>

- A Series is a one-dimensional labeled array which can hold data of any type (integer, string, float, python objects, etc.) 
- It is basically a column in an excel sheet.

```python
#import the pandas library and aliasing as pd
import pandas as pd
s = pd.Series()
print (s)
```

### DataFrame <a name="dataframe"></a>

- DataFrame is a 2-dimensional labeled data structure with columns of potentially different types.
- It is like an excel spreadsheet or SQL table, or a dict of Series objects. 

```python
import pandas as pd
 
# initialise data of lists.
data = {'Name':['John', 'Paul', 'George', 'Ringo'],
        'Age':[27, 24, 22, 32]}
  
# Create DataFrame
df = pd.DataFrame(data)
  
# Print the output.
print(df)
```

## Data Selection in DataFrame <a name="data-selection"></a>

- Just like we select data in SQL, we can select data from DataFrame. Here is how:
```python
import pandas as pd
  
df = pd.DataFrame(data)
  
# select only 'Age' column
print(df['Age'])

# select specific rows by index
print(df[1:3])
```

## Handling Missing Data <a name="missing-data"></a>

- Missing data is quite common in most data analysis applications. Thankfully, pandas provide some methods to handle it:

```python
# use isnull() function to check missing data
print(df.isnull())

# use dropna() function to drop rows with missing data
print(df.dropna())

# use fillna() function to fill the missing data with a specific value
print(df.fillna(0))
```

## Data Manipulation with Pandas <a name="manipulation"></a>

- Data manipulation is an important part of data analysis, and Pandas provides functions like `merge`, `concatenate`, `reshape`, etc.

```python
# Concatenating
print(pd.concat([dataframe1, dataframe2]))

# Merging
print(pd.merge(dataframe1, dataframe2, on='id'))

# Reshaping
print(dataframe.stack())
```

## Grouping and Aggregation <a name="grouping"></a>

- Grouping involves the combination of splitting the data, applying a function, and combining the results.

```python
# Define a dictionary containing employee data
data = {'Name':['John', 'Paul', 'George', 'Ringo'],
        'Age':[27, 24, 22, 32],
        'City':['New York', 'London', 'London', 'Tokyo'],
        'Country':['USA', 'UK', 'UK', 'Japan']}
  
# Convert the dictionary into DataFrame 
df = pd.DataFrame(data)
 
df.groupby('City').mean()
```

## Conclusion <a name="conclusion"></a>

- Pandas is an essential tool for data cleaning, transformation, and analysis. This document should serve as a quick reference for the basic functionality of this powerful tool.
