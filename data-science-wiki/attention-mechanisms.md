Created by @jl33-ai 👦🏻

When training deep neural networks, there is a huge challenge pertaining to understanding different parts of a complicated structure. The "attention mechanism" is a technique that helps overcome this difficulty by picking out only the important parts for the problem at hand! 

## Table of Contents

- [Introduction](#Introduction)
- [Types of Attention Mechanisms](#Types-of-Attention-Mechanisms)
- [Applications in Model Architectures](#Applications-in-Model-Architectures)
- [Final Thoughts](#Final-Thoughts)

## Introduction
In the context of neural networks, the term "attention" indicates how different parts of the networks allocate computational resources. This is based on the data‘s different states at each step of the task, such as parts of an image or text sentence. 

## Types of Attention Mechanisms 

- **Soft Attention**: Determines the degree of 'attention‘ or importance of each step on a scale of between 0 and 1, and assigns a score through a softmax function. It’s called ‘soft’ because all parts are attended to some extent.

```python
    import numpy as np

    def softmax(x):
        return np.exp(x)/sum(np.exp(x))
```

- **Hard Attention**: Based on stochastic selection and reinforcement learning, 'hard attention’ is when the mechanism attends strictly to parts of the input and ignores everything else. Hard attention selects a subset and can entirely disregard the rest.

- **Scaled Dot-Product Attention**: Used in the Transformer architecture, it allows all positions to interact with each other in parallel using a simple dot-product, and then scales by square root of the dimension.

```python
    import torch

    def scaled_dot_product(q, k, v):
        d_k = q.size(-1)
        attn_logits = torch.matmul(q, k.transpose(-2, -1))
        attn_logits /= math.sqrt(d_k)
        attn = F.softmax(attn_logits, dim=-1)
        output = torch.matmul(attn, v)
        return output
```

## Applications in Model Architectures

- LSTM networks: Long Short-Term Memory (LSTM) networks utilize attention mechanisms to assist in remembering long dependencies of sequences.

- BERT: The BERT architecture uses transformer-based models, which employ attention mechanisms to understand the context of words in a sentence.

- Show, Attend and Tell: An attention-based model that automatically learns to describe the content of images.

## Final Thoughts

While attention mechanisms have significantly improved the state-of-the-arts across multiple domains, it is important to note they can contribute to model complexity and are not suitable for all kinds of tasks. 

---

*This tutorial is a brief introduction to attention mechanisms. For further information, see: [Attention in Long Short-Term Memory Recurrent Neural Networks](https://machinelearningmastery.com/attention-long-short-term-memory-recurrent-neural-networks/)*
