# Understanding DataFrames 🧠💻🔍
> Created by @jl33-ai  👦🏻

This markdown document provides an introduction to `DataFrames` in `pandas` with simple & easily understandable examples. 🎓

## Table of Contents 🗂 
* [Introduction](#introduction)
* [Creation of DataFrame](#creation)
* [Selection in DataFrame](#selection)
* [Addition in DataFrame](#addition)
* [Deletion in DataFrame](#deletion)
* [Rename Columns of DataFrame](#rename_columns)

## Introduction <a name="introduction"></a>
A `DataFrame` is a two-dimensional size-mutable, potentially heterogeneous tabular data structure with labeled axes (rows and columns). 

_Attributes:_ 
- The data is aligned in a tabular fashion in rows and columns.
- Can Perform Arithmetic operations on rows and columns.



## Creation of DataFrame <a name="creation"></a>
A `pandas DataFrame` can be created using the following constructor −

```python
pandas.DataFrame( data, index, columns, dtype, copy)
```
_Example:_
```python
import pandas as pd

data = {'Name':['Tom', 'nick', 'john', 'juli'],
        'Age':[20, 21, 19, 18]}

df = pd.DataFrame(data)

print(df)
```

## Selection in DataFrame <a name="selection"></a>
Selection is done in the following ways -
- by Label
- by integer Location etc.
_Example:_
```python
df.loc[:, 'Name']
df.iloc[:, [1]]
```
## Addition in DataFrame <a name="addition"></a>
You can add rows using `.append()` function and for adding columns you can use the `.insert()` function.
_Example:_
```python
df2 = pd.DataFrame({"Name": ["Anna"], "Age": [22]})
df = df.append(df2)
df['Gender'] = ['M', 'M', 'M', 'F', 'F']
```
## Deletion in DataFrame <a name="deletion"></a>
For deleting a columns or rows we use `.drop()` method. 

_Example:_
```python
df.drop(["Gender"], axis=1)
```
## Rename Columns of DataFrame <a name="rename_columns"></a>
To rename the columns of a DataFrame, we can use `.rename()` function.
_Example:_
```python
df.rename(columns = {"Name": "FirstName", 
                     "Age":"AgeInYears"}, 
                                 inplace = True) 
```
# Conclusion 🏁🎯
This markdown document provides an overview of the fundamental operations that can be performed on a `DataFrame`. To know more and explore additional functionalities, refer to the [official documentation](https://pandas.pydata.org/pandas-docs/stable/reference/frame.html).