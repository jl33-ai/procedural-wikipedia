# Numpy-Python Documentation with Examples

## Created by @jl33-ai 👦🏻

## Table of Contents:

* [Introduction](#introduction-)
* [Installation](#installation-)
* [Numpy Fundamental](#numpy-fundamental-)
* [Numpy Arrays](#numpy-arrays-)
* [Numpy Operations](#numpy-operations-)
* [Conclusion](#conclusion-)

## Introduction 📝

NumPy, short for 'Numerical Python', is one of the most important foundational packages for numerical computing in Python. Most computational packages providing scientific functionality use NumPy's array objects for data exchange.

## Installation 💻

Before you can use NumPy, you need to install it. Use the following command in your terminal:

    pip install numpy

If you are using a Jupyter notebook, use the following command:

    !pip install numpy

## Numpy Fundamental 📚
- Numpy's main object is the `ndarray`, or simply an `array`.
- An `array` is a grid of values, all of the same type, there are corresponding indexes for each dimension.
- The dimensions are referred to as `axes`. The number of `axes` is `rank`.

## Numpy Arrays 🧮
Numpy array is the fundamental object.

### To Create Numpy Array 👇
```python
import numpy as np

a = np.array([1, 2, 3]) # create 1D array
print(a)

b = np.array([(1.5,2,3), (4,5,6)]) # create 2D array
print(b)
```
### Array Attributes 👀
```python
import numpy as np

a = np.array([[1, 2, 3], [4, 5, 6]])
print(a.shape)  # prints: (2, 3)

print(a.ndim) # prints: 2

print(a.dtype.name) # prints: 'int64'
```

## Numpy Operations ➕
Numpy provides numerous mathematical operations.

### Array Mathematics 🔢
```python
import numpy as np

a = np.array([1, 2, 3])
b = np.array([10, 20, 30])

print(np.subtract(b, a)) # prints: [ 9 18 27]
print(np.add(b, a)) # prints: [11 22 33]
print(np.divide(b, a)) # prints: [10. 10. 10.]
```

### Aggregation 🎲
```python
import numpy as np

a = np.array([1, 2, 3,4,5])

print(np.sum(a)) # prints: 15
print(np.min(a)) # prints: 1
print(np.mean(a)) # prints: 3.0
```

## Conclusion 🏁
Numpy is a core library for scientific computing in Python providing a high-performance multidimensional array object and tools for working with arrays. It has many useful features and mathematical operations. This documentation is just a brief, make sure to explore more about Numpy. Happy coding! 🚀