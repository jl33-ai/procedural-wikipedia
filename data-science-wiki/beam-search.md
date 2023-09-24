
Created by @jl33-ai 👦🏻 

## Table of contents 
1. [Introduction](#intro)
2. [How it works](#works)
3. [Example of Beam Search](#example)
4. [Applications of Beam Search](#applications)
5. [Advantages & Disadvantages](#advdisadv)
6. [Conclusion](#conclusion)

<a name="intro"></a>
## 🌟 Introduction:
Beam search is heuristic search algorithm that explores a graph by expanding the most promising node in a limited set. Beam search is an optimization of best-first search that reduces its memory requirements. In other words, beam search is a mix of breadth-first search and depth-first search.

<a name="works"></a>
## 🚀 How it Works:
* Beam search uses breadth-first search to build its search tree.
* At each level of the tree, it generates all successors of the current states and keeps only a predetermined number of best paths, called the "beam width".
* Less promising nodes, based on some heuristic, are dropped.

<a name="example"></a>
## 🎲 Example of Beam Search:
Consider a language model trying to predict the next word given a current word in a sequence. If the beam width is 3:

* The model predicts top 3 possible next words.
* For each of these 3 words, the model predicts top 3 successors again.
* So we have 9 paths now, but we keep only the top 3 according to their probabilities.
* We continue this process untill the end of the sequence.

<a name="applications"></a>
## 🌍 Applications of Beam Search:
1. Natural Language Processing: In machine translation, beam search can be used to generate a number of possible translations and then select the one with the highest probability.
2. Speech Recognition: Beam search can be used to recognize a possible proper sentence from speech input.
3. Travelling Salesman Problem: Beam search is some times used for finding an oatimal solution for TSP.

<a name="advdisadv"></a>
## 🍏 Advantages & 🍎 Disadvantages:
### Advantages:
* Beam search reduces memory requirements compared to best-first search and can find reasonably good solutions.
* It's faster than breadth-first search and depth-first search as it doesn't search all nodes.

### Disadvantages:
* Beam search is not guaranteed to find an optimal solution.
* It's sensitive to its beam width: a small beam width can cause the algorithm to converge to a local optima, while a larger beam width can be computationally expensive.

<a name="conclusion"></a>
## 💫 Conclusion: