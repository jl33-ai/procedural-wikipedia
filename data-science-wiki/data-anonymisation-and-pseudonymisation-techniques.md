
*Created by @jl33-ai 👦🏻*

## Table of Contents

1. [Introduction](#introduction)
2. [Data Anonymisation Techniques](#data-anonymisation-techniques)
3. [Data Pseudonymisation Techniques](#data-pseudonymisation-techniques)
4. [Examples](#examples)
5. [Conclusion](#conclusion)

<a name="introduction"></a>
## Introduction 📑

This document addresses **Data Anonymisation** and **Pseudonymisation** techniques, which are critical practices for maintaining data privacy and meeting regulatory compliance, like GDPR and HIPAA. 

<a name="data-anonymisation-techniques"></a>
## Data Anonymisation Techniques🕵️‍♀️🔎

Data anonymisation involves modifying `personal data` to remove all identifiable information so the data subject can't be identified.

Here are some popular anonymisation techniques:

1. **Data Masking**: Replaces sensitive data with random characters or data 🎭.
2. **Perturbation**: Changes the original data slightly to stop identification 🌪️.
3. **Generalization**: Reduces the granularity of data by replacing it with more 'general' data 🌐.
4. **Data Swapping (Shuffling/Permutation)**: Changing the dataset order to break the link between individuals and their data 🔄.
5. **K-anonymity**: Adjusts and clusters the data in a way that re-identifying individuals becomes difficult 🏝️.

<a name="data-pseudonymisation-techniques"></a>
## Data Pseudonymisation Techniques🕵️‍♂️🔎

Data pseudonymisation transforms `personal data` to keep it usable but not lead back to original data subjects without extra info.

Here are some common pseudonymisation techniques:

1. **Encryption with secret key**: A cryptographic key that is used for both encryption and decryption 🗝️.
2. **Hash functions, possibly with salt**: A hash function transforms input of any length into a fixed-size string of text 🧂.
3. **Tokenization**: Replaces sensitive data with non-sensitive 'token' substitutes 🏷️.

<a name="examples"></a>
## Examples 🧪

**Anonymisation Example:**

Original data: John Doe, 36, Los Angeles, Heart Disease  
Anonymised data: Person, Age Range(30-40), Large City, Chronic Disease 

**Pseudonymisation Example:**

Original data: johndoe@email.com  
Pseudonymised data: 143nkjv42v6@example.com  

<a name="conclusion"></a>
## Conclusion 🕰️

Data Anonymisation and Pseudonymisation are crucial for data privacy. While anonymisation makes re-identification impossible, pseudonymisation allows it under certain circumstances. Choose the one fits best to your scenario.

Always remember that while anonymised/pseudonymised data can be used freely, it can lose its fidelity and originality, which might limit its usefulness for data analysis.
