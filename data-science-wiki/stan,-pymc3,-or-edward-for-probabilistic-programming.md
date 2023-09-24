#### Created by @jl33-ai 👦🏻  

This is a brief comparison guide for three of the most popular open-source libraries for probabilistic programming: Stan, PyMC3 and Edward. These libraries are used to estimate the probabilities of objects or events. 

## Table of Contents

- [Introduction](#introduction)
- [Stan](#stan)
- [PyMC3](#pymc3)
- [Edward](#edward)
- [Conclusion](#conclusion)

<a name="introduction"></a>
### :point_right: Introduction

Probabilistic programming allows you to design probabilistic models and then solve them automatically. The three most commonly used libraries are‌ Stan, PyMC3, and Edward.

<a name="stan"></a>
### :point_right: Stan

![Stan](https://mc-stan.org/docs/2_27/_static/img/logo.png)

[Stan](https://mc-stan.org/) is a robust and flexible tool for modeling and high-performance statistical analysis.

1. #### Features:
    - Built-in language for creating custom probabilistic models
    - MCMC sampling provided (like Hamiltonian Monte Carlo)
    - Can handle complex models with ease
    - Has excellent scalability, with multi-core processing capabilities

2. #### Example:

    Here is how you could perform simple linear regression in Stan.
    ```stan
    data {
      int<lower=0> N;
      vector[N] x;
      vector[N] y;
    }
    parameters {
      real alpha;
      real beta;
      real<lower=0> sigma;
    }
    model {
      y ~ normal(alpha + beta * x, sigma);
    }
    ```

<a name="pymc3"></a>
### :point_right: PyMC3

![PyMc3](https://docs.pymc.io/_images/pymc3_logo.png)

[PyMC3](https://docs.pymc.io/) is a Python library for Bayesian statistical modeling and Probabilistic Machine Learning.

1. #### Features:
    - Allows model specifications directly in Python code
    - Has a wide variety of pre-programmed statistical models
    - Also supports MCMC and variational inference
    - Harnesses the power of Theano for computation
    
2. #### Example:
   
   Here is how you could perform simple linear regression with PyMC3.
    
    ```python
    import pymc3 as pm

    basic_model = pm.Model()

    with basic_model:
        # Priors for unknown model parameters
        alpha = pm.Normal('alpha', mu=0, sigma=10)
        beta = pm.Normal('beta', mu=0, sigma=10, shape=2)
        sigma = pm.HalfNormal('sigma', sigma=1)

        # Expected value of outcome
        mu = alpha + beta[0]*x1 + beta[1]*x2 

        # Likelihood (sampling distribution) of observations
        Y_obs = pm.Normal('Y_obs', mu=mu, sigma=sigma, observed=Y)
    ```

<a name="edward"></a>
### :point_right: Edward

![Edward](http://edwardlib.org/images/edward-logo.png)

[Edward](http://edwardlib.org/) is a Python library built to be fast and flexible. Its aim is to enable complex probabilistic modeling, including both training and inference. 

1. #### Features:
    - Supports a wide range of architectures, like deep probabilistic models
    - Provides interfaces to easily plug-and-play with other TensorFlow libraries
    - It provides both classes of inference: Monte Carlo and variational inference

2. #### Example:
    We'll demonstrate Edward with simple model, a Beta-Bernoulli.

    ```python
    from edward.models import Beta, Bernoulli, Empirical

    # Prior on probability of success (use a conjugate prior)
    p = Beta(1.0, 1.0)

    # Likelihood
    data = Bernoulli(probs=p, dtype=tf.int32, sample_shape=10)

    # Posterior (we'll use Empirical to allow for greatest flexibility in modeling)
    q = Empirical(params=tf.Variable(tf.zeros(500)))

    # Inference (use Metropolis Hastings MCMC method)
    inference = ed.MetropolisHastings({p: q}, {p: data})
    inference.run(n_iter=500)
    ```

<a name="conclusion"></a>
### :point_right: Conclusion 

Before choosing between Stan, PyMC3, and Edward, you must consider the specifics of your project. Stan performs very sophisticated statistical and mathematical operations, PyMC3 has an advantage for being purely Python, and Edward functions well with TensorFlow. A noteworthy aspect is that they all support Bayesian statistical modelling, which is the backbone of probabilistic programming. 

## :sparkles: Happy Coding! :sparkles:

<table>
<tr>
<td valign="top"><sub><a href="#top">:arrow_up: back to top</a></sub></td>
</tr>