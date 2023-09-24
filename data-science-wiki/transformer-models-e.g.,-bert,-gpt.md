### Created by @jl33-ai 👦🏻

In this document, we will delve into the world of Transformer models, specifically, the BERT (Bidirectional Encoder Representations from Transformers) and GPT (Generative Pretrained Transformer) models. These models have revolutionized the NLP (Natural Language Processing) field and have been widely used in a variety of applications, such as sentiment analysis, question-answering, and language translation.

## Table of Contents
- [Introduction](#introduction)
- [BERT](#bert)
- [GPT](#gpt)

## Introduction
In layman's terms, Transformer models are neural models that use self-attention mechanisms to understand the context of words in a sentence. They have been very successful in a multitude of natural language processing tasks.

## BERT
BERT, which stands for Bidirectional Encoder Representations from Transformers, is designed to pretrain deep bidirectional representations from unlabeled text by jointly conditioning on both left and right context in all layers.
### Key Features of BERT
- **Bidirectional:** Traditional models like RNN and LSTM read the text input sequentially (either left-to-right or right-to-left), while BERT leverages Transformer's attention mechanism to directly connect all positions of a sentence.
- **Pretraining:** BERT is pretrained on a large corpus of text data (Wikipedia + BooksCorpus).
- **Fine-tuning:** The pretrained BERT model can be fine-tuned on a specific task with additional output layer to generate predictions.

### Getting Started
```bash
pip install transformers
```
### Example Code 📜
```python
from transformers import BertTokenizer, BertModel

tokenizer = BertTokenizer.from_pretrained('bert-base-uncased')
model = BertModel.from_pretrained("bert-base-uncased")

input_ids = tokenizer("Hello, my dog is cute", return_tensors="pt")["input_ids"]
outputs = model(input_ids)
```
## GPT
The Generative Pretrained Transformer (GPT) from OpenAI is yet another transformative model in the NLP landscape. It, however, focuses on generating human-like text.
### Key Features of GPT
- **Autoregressive:** It generates a sentence by predicting the next word in a given sequence of words.
- **Pretraining:** Like BERT, GPT also utilizes the benefits of pretraining on a large volume of text data.
- **Fine-tuning:** The pretrained GPT model needs to get fine-tuned for specific NLP tasks.

### Getting Started
```bash
pip install transformers
```
### Example Code 📜
```python
from transformers import GPT2LMHeadModel, GPT2Tokenizer

tokenizer = GPT2Tokenizer.from_pretrained("gpt2")
model = GPT2LMHeadModel.from_pretrained("gpt2")

inputs = tokenizer("Hello, I'm a model,", return_tensors="pt")
outputs = model(**inputs, labels=inputs["input_ids"])
```

## References
- [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/abs/1810.04805)
- [GPT: Improving Language Understanding by Generative Pre-Training](https://cdn.openai.com/research-covers/language-unsupervised/language_understanding_paper.pdf)

## Tags