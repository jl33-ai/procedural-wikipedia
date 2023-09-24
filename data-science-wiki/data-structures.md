
_Created by @jl33-ai 👦🏻_

In computing, data structure is a [data organization](https://en.wikipedia.org/wiki/Data_structure), management, and storage format that enables efficient access and modification. It is a collection of data values, the relationships among them, and the functions or operations that can be applied to the data.

---

## Table of Contents 
1. [Primitive Types](#Primitive-Types)
2. [Non-Primitive Types](#Non-Primitive-Types)
3. [List](#List)
4. [Tuple](#Tuple)
5. [Set](#Set)
6. [Dictionary](#Dictionary)
7. [Tree](#Tree)
8. [Graph](#Graph)
---

## Primitive Types 🟢

These are the basic data types that a language built-in and they are used to build non-primitive types.

- Integer: represented by `int` in Python
- float: represents real numbers and are written with a decimal point
- String: represented as `str` in Python. E.g. `name = "John Doe"`
- Boolean: Data with one of two possible values either `True` or `False`

---

## Non-Primitive Types 🟣

These data types are derived from the primitive data types and are used to store multiple values.

- List
- Tuple
- Set
- Dictionary
- Tree
- Graph

---

## List

A list is a collection of items that can be ordered, changeable and allow multiple duplicate items. They are written in square brackets `[]`.

Example:
```
grocery_list = ["apple", "banana", "cherry"]
```
---

## Tuple

A tuple is a collection which is ordered and unchangeable. Allows duplicate members. They are written in round brackets `()`. 

Example:
```  
coordinates = (22.2, 114.4)
```
---

## Set

A set is a collection that is unordered and unindexed. No duplicate members. In python, sets are written in curly brackets `{}`.

Example:
```  
fruit_set = {"apple", "banana", "cherry"}
```
---

## Dictionary

A dictionary is a collection of data which is unordered and can be changed by use of built in methods. Dictionaries in python are written as `key : value` pairs in curly brackets `{}`.
   
Example:
```  
person = {"name": "John Doe", "age": 30}
```
---

## Tree

A tree is a hierarchical data structure with a root value and subtrees of children with a parent node, represented as a set of linked nodes.

Example:

```
    Root
     /\
   Leaf Leaf
```
---

## Graph

A graph data structure consists of a finite (and possibly mutable) set of vertices (also called nodes or points), together with a set of unordered pairs of these vertices for an undirected graph or a set of ordered pairs for a directed graph.

Example:

```
   A------B\
   |\      |\  
   | \     | \
   |  \    |  C
   |   D---E /
   |/       |/
   F--------G
```
---

I hope this overview of data structures is helpful for you. 😄
