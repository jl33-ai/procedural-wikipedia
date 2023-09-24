
_**Created by @jl33-ai 👦🏻**_

This notebook provides a comprehensive overview of two primary types of generative models: Variational Autoencoders (VAEs) and Flow-Based Models. Our focus will be understanding their functionalities, strengths, and notable examples. Let's start exploring! 

---

## Contents: 

- [Introduction](#Introduction)
- [Variational Autoencoders (VAEs)](#VAEs)
- [Flow-Based Models](#FbM)
- [Summary](#Summary)
- [Reference/Resources](#References)

---

## <a name="Introduction"></a>Introduction 🎯

Generative models are a powerful subset of machine learning models that generate new data instances resembling your training data. Generative models capture the joint probability distribution of the input features and are widely used in:

* Image synthesis
* Anomaly detection
* Image denoising
* Data augmentation
* Imputation of missing data

Two effective generative models are:

1. [Variational Autoencoders (VAEs)](#VAEs)
2. [Flow-Based Models](#FbM)

Let's dive deeper into these models.

---

## <a name="VAEs"></a>Variational Autoencoders (VAEs) 🧮

VAEs are a kind of generative model that add capabilities to traditional autoencoders. Here's a quick overview:

### Understanding VAEs 🧩
* VAEs are probabilistic and assume that the data and the codes are random variables.

* It has the same architecture as an Autoencoder but with a twist in the middle. 

* The encoder takes a data point, sends it into a latent space, where it generates a set of parameters that are then used to generate a distribution.

* The decoder then takes random samples from these distributions and decodes them back to the original data, adding a layer of randomness to our model.

### Key Benefits of VAEs 🌟
* VAEs allow for complex, abstract representations.

* They model the underlying probability distribution of the data, so they can generate completely new data points.

* VAEs are flexible and relatively easy to implement. 

### Examples of VAE use-cases 🚀
* Generating faces (_CelebA dataset_).
* Creating artwork (_DeepArt_).

---

## <a name="FbM"></a>Flow-Based Models 🌊

Flow-Based models are another category of generative models that are especially useful for tasks requiring explicit likelihood evaluation.

### Understanding Flow-Based models 💡
* Flow-Based models are a family of deep generative models with highly desirable properties for modeling complex distributions.

* They use invertible neural networks to transform a simple base distribution (e.g., multivariate standard Gaussian) into a complex one, matching any data distribution given sufficient capacity.

* The models get their name because they allow probabilistic flow of information in both directions (from input to output and from output to input), enabling both efficient sampling and density estimation.

### Key Benefits of Flow-Based models 🥇
* They provide rich expressivity, enabling them to closely approximate complex, high-dimensional distributions.

* Explicit density: Flow-Based models provide an estimate of the data likelihood, unlike GANs and VAEs.

* Exact latent-variable inference and tractable likelihood: Flow-based models have tractable likelihoods and permit exact latent-variable inference, unlike GANs and VAEs.

### Examples of Flow-Based Models use-cases 🏹
* High-quality image synthesis (_Glow model_).
* Text-to-speech synthesis (_WaveGlow_).

---

## <a name="Summary"></a>Summary 📝

This notebook provides an overview of VAEs and Flow-Based Models, two primary types of generative models. We explored their basic understanding, benefits, and examples. Both offer unique advantages and can be used for various applications ranging from image synthesis to text-to-speech synthesis.

---

## <a name="References"></a>Reference/Resources 📚

1. ["Variational Autoencoder: An Unreasonably Deep Dive"](https://lilianweng.github.io/lil-log/2018/08/12/from-autoencoder-to-beta-vae.html)
2. ["Flow-based deep generative models"](https://lilianweng.github.io/lil-log/2018/10/13/flow-based-deep-generative-models.html)

---

**Disclaimer**: