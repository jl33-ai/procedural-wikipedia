Created by @jl33-ai 👦🏻

## Table of Contents

- [Introduction](#Introduction)
- [How to use RNNs for NLP?](#How-to-use-RNNs-for-NLP?)
- [Types of RNN](#Types-of-RNN)
- [Working Example of RNN for NLP](#Working-Example-of-RNN-for-NLP)
- [Summary](#Summary)
- [References](#References)

## Introduction 

Recurrent Neural Networks (RNNs) are a type of artificial neural network designed to recognize patterns in sequences of data, such as text, genomes, handwriting, or the spoken word. With the capacity to recognize patterns across time, RNNs are particularly effective for Natural Language Processing (NLP) tasks.

## How to use RNNs for NLP?

_RNNs and Words Representation_ 😊
1. Convert the words in your text to vectors using methods like One-Hot Encoding, Word2Vec or GloVe.
2. Feed these vectors into your RNN.

_RNNs Structure_ 😄
1. RNNs use sequential information by performing the same task for every element in the input sequence and passing the information along to the next step.
2. This chain-like nature reveals the 'recurrent' aspect of RNNs.

## Types of RNN

_RNN Variants_ 🧠
1. **Vanilla RNN**: The simplest form but fails to capture long-term dependencies because of 'vanishing gradient' problem.
2. **LSTM (Long Short Term Memory)**: A type of RNN that mitigates the vanishing gradient problem, making it great for learning from important experiences that have very long time lags.
3. **GRU (Gated Recurrent Unit)**: A simplification of LSTM, with performance like LSTM but with less complexity.

## Working Example of RNN for NLP 

Here's a concrete example where we employ PyTorch to create a simple RNN for text generation:

```python
import torch
from torch import nn

transform_texts = ["I feel happy", "I feel sad", "I feel amazed"] # suppose these are our input texts
map_words_to_one_hot = ... # a function to map words to vectors e.g. one-hot vectors

# let's define the dimensions
input_dim = len(vocabulary)
hidden_dim = 100
output_dim = len(vocabulary)
num_rnn_layers = 1

class SimpleRNN(nn.Module):
    def __init__(self, input_dim, hidden_dim, output_dim, num_rnn_layers):
        super(SimpleRNN, self).__init__()
        self.hidden_dim = hidden_dim
        self.rnn = nn.RNN(input_dim, hidden_dim, num_rnn_layers, batch_first=True)
        self.fc = nn.Linear(hidden_dim, output_with)
  
    def forward(self, x):
        out, _ = self.rnn(x)
        out = self.fc(out[:, -1, :])
        return out

# Instantiate the model with hyperparameters
model = SimpleRNN(input_dim, hidden_dim, output_dim, num_rnn_layers)
```

## Summary

Recurrent Neural Networks (RNNs) are incredibly powerful for NLP tasks due to their capacity to handle sequence data. By learning the relevant aspects of the input thanks to their design, they can accurately predict or classify outputs. Applications include text auto-completion, sentiment analysis, machine translation and much more.

## References 

1. Understanding LSTM Networks (http://colah.github.io/posts/2015-08-Understanding-LSTMs/)