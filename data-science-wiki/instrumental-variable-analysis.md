# Instrumental Variable Analysis ✨

*Created by @jl33-ai* 👦🏻

Instrumental Variable Analysis (IVA) is a statistical method which is used when the predictor variables (explanatory variables) in a statistical model are influenced by unobserved confounding factors. In these cases, the use of causal effects of predictor variables on outcome variables is recommended.

## Table of Contents

1. [Overview](#overview)
2. [Requirements for Instrumental Variables](#requirements)
3. [Example of an Instrumental Variable Analysis](#example)
4. [Advantages and Disadvantages](#advantages-disadvantages)

## Overview <a name="overview"></a> 👓

* The method aims to mimic the conditions of a randomized experiment by accounting for unobserved confounding variables that may bias causal inference.
* This technique is used when the standard assumption of econometric model, that the predictor variables are uncorrelated with the error term, is violated.

## Requirements for Instrumental Variables <a name="requirements"></a> 📝

#### There are three requirements to choose an instrumental variable: 
1. **Relevance:** The chosen instrument must be correlated with the predictor variable(s).
2. **Exogeneity:** The instrument cannot be correlated with the error term.
3. **Exclusion:** The instrument only affects the dependent variable through the predictor variable(s).

## Example of an Instrumental Variable Analysis <a name="example"></a> 📖
```python
# Python code for regression using Instrumental Variable Two Stage Least Squares
import numpy as np
import statsmodels.api as sm
from statsmodels.sandbox.regression.gmm import IV2SLS

# Generate some sample data
np.random.seed(12345)
instrument = np.random.normal(size=500)
endog = instrument + np.random.normal(size=500) / 2
exog = instrument + np.random.normal(size=500)
Z = np.column_stack((instrument, np.ones(500)))
X = np.column_stack((exog, np.ones(500)))

# Estimate model
model = IV2SLS(endog, X[:,-1], X[:,0], Z[:,0]).fit()
print(model.summary())
```
In this example, 'exog' is the predictor variable which we think might be influenced by unobserved factors, and 'instrument' is a variable which we expect to be correlated with 'exog' but not with the ‘endog’.

## Advantages and Disadvantages <a name="advantages-disadvantages"></a> 🎭

#### Advantages:
1. Can handle endogeneity problem where a predictor variable is correlated with the error term.
2. Allows for consistent estimation of causal effects.

#### Disadvantages:
1. Requires strong assumptions and an appropriate instrumental variable, which is not always available.
2. Not an efficient estimator if the errors are heteroskedastic or autocorrelated.