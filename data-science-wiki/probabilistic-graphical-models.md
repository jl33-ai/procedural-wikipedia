# Probabilistic Graphical Models
`Created by @jl33-ai 👦🏻`

Probabilistic Graphical Models (PGMs) provide a structured representation of the joint probability distributions in machine learning-complex systems. They aim to capture dependence amongst the random variables in the model. PGMs are extensively utilized in fields such as artificial intelligence, statistics and information theory.

## Contents:

- [What is PGM?](#what_is_PGM)
- [Types of PGMs](#Types_of_PGMs)
    - [Bayesian Networks](#Bayesian_Networks)
    - [Markov Networks](#Markov_Networks)
- [Applications of PGMs](#Applications_of_PGMs)
- [Conclusion](#Conclusion)

<a name="what_is_PGM"/>

## What is PGM?
PGM is a rich framework for encoding probability distributions over complex domains. With a PGM, we can represent complex correlations between different features in a more simplified form rather than considering all possibilities.

- PGMs allow us to break complex systems down into simpler parts. :+1:
- They are useful to compactly describe the joint probability distribution over random variables.

<a name="Types_of_PGMs"/>

## Types of PGMs
There are primarily two types of PGMs.

<a name="Bayesian_Networks"/>

## Bayesian Networks
Bayesian Networks, also known as Belief Networks or Directed Acyclic Graphical Models, are a kind of PGM that represents the conditional dependencies of random variables through a directed acyclic graph (DAG).

- A Bayesian network is represented as: _BN = (G, P)_

    - Where `G` is a DAG and the nodes correspond to `n` number of variables, and the edges represent direct dependencies between them.
    - `P` stands for a set of conditional probability distributions.

<a name="Markov_Networks"/>

## Markov Networks
Markov Networks, also known as Markov Random Fields or Undirected Graphical Models, are another class of PGM that represents the joint distribution of random variables through an undirected graph.

- A Markov network is represented as: _MN = (H, Φ)_

    - Where `H` is an undirected graph and the nodes correspond to `n` number of random variables.
    - `Φ` stands for the set of potential functions. 

<a name="Applications_of_PGMs"/>

## Applications of PGMs
- In robotics, these models are used for mapping and localization.
- In social network analysis, PGMs are used to model the behavior of large communities of people.
- PGMs facilitate spam filtering by determining if an email is a Spam or Not a Spam.
- In genetic studies, PGMs can model genetic networks and infer gene-activity levels.

<a name="Conclusion"/>

## Conclusion
By compactly encoding the joint probability distribution of large, complex systems, Probabilistic Graphical Models greatly simplify the process of building and using probabilistic models. They are an integral part of various fields and continue to bring in more efficiency and accuracy to the processes.
