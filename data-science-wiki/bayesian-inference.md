# Bayesian Inference 🎲
##### Created by @jl33-ai 👦🏻

Bayesian inference is a method of statistical inference in which Bayes' theorem is used to evaluate the probability of a hypothesis. It involves updating the odds of our hypotheses being true as new data/Evidence becomes available.

### Contents

- [Introduction](#introduction-to-bayesian-inference-%EF%B8%8F)
- [Bayes Theorem](#bayes-theorem-%EF%B8%8F)
- [Example](#example-%EF%B8%8F)
- [Advantages and Limitations](advantages-and-limitations)

## Introduction to Bayesian Inference ➗
The name 'Bayesian' comes from the Bayesian interpretation of probability, named after Thomas Bayes, in contrast to the frequentist interpretation.

Unlike in frequentist inference, probability in Bayesian inference is often assigned to hypotheses, and statistical models are usually treated as fixed.

Bayesian inference blends the likelihood calculated from observed data with prior knowledge or beliefs. It allows us to combine what we know from data with what we knew before we saw the data. 

## Bayes Theorem ➕
Bayes’ Theorem comes into play in Bayesian Inference. The theorem is a simple formula that determines the probability of event B happening, given that event A has occurred.

The equation is as follows:
```
P(A|B) = [P(B|A) * P(A)] / P(B)
```
Where:
- `P(A|B)` is the conditional probability that event A occurs given event B has already occurred.
- `P(B|A)` is the conditional probability that event B occurs given event A has already occurred.
- `P(A)` and `P(B)` are the probabilities of observing A and B independently of each other.

## Example 👀
Let's consider a classic example - testing for a disease.
- Probability of having the disease `P(D)` = 0.01 (1% of the population has the disease).
- Probability of testing positive if you have the disease `P(T+|D)` = 0.99 (the test is 99% accurate).
- Probability of testing positive if you do not have the disease `P(T+|~D)` = 0.05 (the false positive rate is 5%).

If a person tests positive, what is the probability they actually have the disease?

- Here, our goal is to find `P(D|T+)`.
- Using Bayes Theorem, we can find that `P(D|T+)` is approximately 0.16, or 16%.

## Advantages and Limitations 🔄
Advantages:
- Modelling flexibility: Bayesian models can handle many different kinds of data and patterns.
- Results are intuitive: The Bayesian estimate comes out as a probability, which is close to how humans naturally think about problems.
- The theory is conceptually simpler: Bayesian theory has a solid philosophical foundation.

Limitations:
- Computationally intensive: Bayesian analysis often requires complex mathematical software and may be slow.
- Subjective prior: Bayesian analysis requires the analyst to make subjective choices about the prior. This could lead to different results as it might differ from person to person.

## Conclusion 🏁
Bayesian inference, stemming from Bayes' theorem, is a powerful tool for probability estimation. By combining novel observation results with established knowledge, we can continuously improve our hypotheses.