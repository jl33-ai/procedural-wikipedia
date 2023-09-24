
Created by @jl33-ai 👦🏻

------------

# What is Markov Chain Monte Carlo (MCMC)? 

Markov Chain Monte Carlo (MCMC)methods are a class of algorithms for sampling from a probability distribution. These techniques are particularly useful when the distribution is complex and the desired result is difficult to obtain analytically.
The Markov Chain refers to the sequence of variables the algorithm steps through, with the 'Monte Carlo' aspect pertaining to the randomness incorporated in the process.

----------

# Understanding MCMC

## Basic Concepts:🧠

- **Markov Chain**: A sequence of random variables where a parameter depends only on the preceding value. It has the *Markov Property*, meaning the future state is independent of the past states given the present state.

- **Monte Carlo**: Refers to the repeated generation of random variables from a specified distribution to simulate complex mathematical problems.

- **Bayesian Statistics**: The branch of statistics where we use prior knowledge, along with evidence from incoming data to infer the future predictions. MCMC is a method used in Bayesian Statistics. 

## How does it work? 🛠️

1. Initialize a random solution 
2. Generate a random neighboring solution 
3. Acceptance or rejection of new solution based on a specific acceptance criterion.
4. If solution is accepted, it's added to the chain.
5. Repeat steps 2-4 for a substantial number of iterations.
6. A distribution is formed from the accepted solutions.

----------

# MCMC Algorithms 

Several classes of MCMC algorithms have been developed, including:

## 1. Metropolis-Hastings Algorithm🔎

- The first and simplest MCMC method. 
- It generates a random walk using a proposal density and probabilistic acceptance criterion.

## 2. Gibbs Sampling✍️

- Special case of Metropolis-Hastings algorithms.
- Useful when the joint distribution is complex, but the conditional distributions are simple.

## 3. Hamiltonian Monte Carlo🛸

- Uses information about the gradient of the log probability to propose future states.
- Significantly reduces the correlation between successive sampled states and achieves much faster convergence.

------

# Advantages of MCMC ☑️

- Most useful for dimensions of data sets that are greater than 2. 
- Can solve problems that have multiple or many parameters. 
- Capable of handling missing data.

# Limitations of MCMC ⚠️

- Can take a long time to run and converge to the target distribution.
- Can get stuck in high probability states, not exploring the full space of possible states.
- The distribution of interest must be known except for a constant of proportionality.

------

# MCMC in use📊

We use MCMC in numerous applied areas such as:

- Physics
- Finance 
- Computer Vision
- Artificial Intelligence
- Epidemiology

-------------

# MCMC Code example 

Here is an example of how to implement MCMC in python using the `pymc3` library:

```python
import pymc3 as pm
import numpy as np

# observed data
n = 100
h = 61
alpha = 2
beta = 2

with pm.Model() as model:
    # prior
    p = pm.Beta('p', alpha, beta)
    
    # likelihood
    y = pm.Binomial('y', n=n, p=p, observed=h)
    
    # inference
    trace = pm.sample(2000, tune=1000)
```

-------------
Use the `trace` variable to access the samples for the `p` variable: `trace['p']`.

I hope this notebook was helpful in understanding MCMC! ✌️🎉 

----------

# References 📚

- [Markov Chain Monte Carlo in Practice: A Roundtable Discussion](https://amstat.tandfonline.com/doi/pdf/10.1198/000313006X96962)
- [A Conceptual Introduction to Hamiltonian Monte Carlo](https://arxiv.org/abs/1701.02434)
- [pymc3 library](https://docs.pymc.io/)
