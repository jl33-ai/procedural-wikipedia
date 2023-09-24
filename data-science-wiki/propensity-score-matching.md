# Propensity Score Matching (PSM) 💡

**Created by @jl33-ai 👦🏻**

_Propensity Score Matching_ or PSM is a statistical technique that attempts to estimate the effect of a treatment by comparing the treated and the non-treated units in an observational study. 

## Table of contents: 
* [Introduction 👋](#introduction-👋)
* [What is PSM? 🧐](#what-is-psm-🧐)
* [Applications 📚](#applications-📚)
* [Step-by-step procedure 📘](#step-by-step-procedure-📘)
* [Advantages and Disadvantages 🏁](#advantages-and-disadvantages-🏁)
* [References 🖋](#references-🖋)

### Introduction 👋

In experimental research, we often have the luxury of controlled experiments where researchers can assign treatments randomly, making sure that the effect of confounding variables is mitigated. But in many practical scenarios doing a randomized experiment is not possible.

This is where _Propensity Score Matching_ (PSM) comes in handy.

### What is PSM? 🧐

PSM is used to create “pseudo-controls” 🎭, in observational data — making the data look like a randomized experimental data. It estimates the effect of a treatment, policy, or other intervention on an outcome by comparing the average outcome of treated to untreated units with the same propensity score.

### Applications 📚

One of the greatest applications of PSM is in the field of program evaluation, economics, public health, and medical research. 

### Step-by-step Procedure 📘

1. **Choosing covariates:** Begin by selecting covariates that you believe may influence the treatment assignment or outcome.

2. **Estimating propensity scores:** Use logistic regression to estimate the propensity score.

3. **Matching:** Once you have the propensity scores, match each treated unit to one or many untreated units using nearest-neighbor matching, radius matching or kernel matching.

4. **Assessing the overlap and balance:** Diagnose and check if your matching is adequately removing the bias in the covariate(s).

5. **Estimate treatment effect:** The last step in the PSM procedure is to estimate the treatment effect.

### Examples of PSM in Python:

```python
# Importing necessary libraries
from sklearn.linear_model import LogisticRegression

# Defining logistic regression model
model = LogisticRegression()

# Fitting the model with data
model.fit(X, treated)

# Getting propensity scores
propensity_scores = model.predict_proba(X)[:, 1]
```

### Advantages and Disadvantages 🏁

**Advantages**
* Allows a way of pretending to do a randomized trial using observational data. 
* Reducing bias due to confounding variables.

**Disadvantages**
* Dependant on the choice and quality of covariates.
* Doesn’t take into account unknown confounders.

### References 🖋
* [“Propensity score methods for bias reduction in the comparison of a treatment to a non-randomized control group” by D'Agostino](https://pubmed.ncbi.nlm.nih.gov/11019996/)
* [“Practical Propensity Score Methods Using R” by Walter](https://journals.sagepub.com/doi/abs/10.1177/1536867x0800800114)
