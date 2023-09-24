# MapReduce 🌍🔍

> Created by @jl33-ai 👦🏻

MapReduce is a programming model and an associated implementation for processing and generating big data sets with a parallel, distributed algorithm on a cluster.

---

### Content

- [Objective 🎯](#objective)
- [Architecture 🏗️](#architecture)
- [Working 🔄](#working)
- [MapReduce Example 🌍](#example)
- [Conclusion 🏁](#conclusion)

---

## Objective 🎯

The main objective of MapReduce is to divide the application into small parts of work, each of which could be executed on any nodes in the cluster.

- **Map:** The map task is performed using a map() function, which performs filtering and sorting. 💾
- **Reduce:** The reduce task is performed using a reduce() function, performs a summary operation.🔄

---

## Architecture 🏗️

MapReduce has two important stages:

1. **Map Stage:** The main task of the Map() function is to map the input data set into a final set of outputs.✨
2. **Reduce Stage:** The Reducer’s task is to take the output from the Mapper as an input and combine those data tuples into a smaller set of tuples.💫

---

## Working 🔄

The MapReduce algorithm contains several important tasks each of which are executed systematically:

1. **Splitting:** The input file or files are split into runs of approximately equal sizes.
2. **Mapping:** Each split data is passed to the mapping phase. Each mapper now processes the lines in its run, emitting one intermediate key-value pair each time it processes a line.
3. **Shuffling:** The MapReduce framework collects the key-value pairs from all the mappers, sorts them by the key, and passes them on to the reducers. This is the shuffle phase.
4. **Reducing:** Each reducer takes the intermediate keys and their list of associated values and processes them one key at a time.

---

## MapReduce Example 🌍

Here is a simple example of a MapReduce algorithm, which counts the occurrence of words in a text file.

**Mapper**

The mapper scans through the text file line by line, it splits each line into words and for every word, it sends a key-value pair where the word is the key and the value is ‘1’ to represent one occurrence of the word.

```
Line 1: apple orange apple pear
Mapper Output: (‘apple’, 1), (‘orange’, 1), (‘apple’, 1), (‘pear’, 1)
```

**Reducer**

The reducer sums up all the values for each word and outputs the word and its total count.

```
Reducer Output: (‘apple’, 2), (‘orange’, 1), (‘pear’, 1)
```
---

## Conclusion 🏁

The MapReduce algorithm is a blessing for big data as it makes complex computations and processing a lot easier. It further enhances an organization’s capabilities and decision making. 

This algorithm has served as a tool for organizing and structuring huge amounts of data and will continue to be a primary go-to solution for handling big data.

---
