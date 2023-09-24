# Data Scaling and Normalisation 📊

`Created by @jl33-ai 👦🏻`

Data Scaling and Normalisation are powerful techniques that can make your machine learning models 🤖 more accurate and easier to interpret. Let's dig deep into both concepts.

## Table of Contents
    - [Data Scaling](#data_scaling)
    - [Data Normalisation](#data_normalisation)
    - [Difference Between Data Scaling and Normalisation](#difference)
    - [When to use them](#when_to_use)
    - [Real-world Examples](#examples)

## Data Scaling <a name="data_scaling"></a>

Data Scaling involves changing the range of your data. In other words, scaling your data means that you're transforming your data so that it fits within a specific range. This technique is often used when we need to bring all features to the same level of magnitude.

For example, say you have a dataset with two features: age (ranges from 0 to 100) and income (income can range from 0 to very high values in the thousands or millions). This discrepancy in range can cause problems when we try to analyze the data.

**Key Points:**

- Data Scaling helps to bring all your values onto one scale 👌.
- It is often a necessary step when using Machine Learning Algorithms 🤖.
- Examples of data scaling are Min-Max scaling and Standardization.

## Data Normalisation <a name="data_normalisation"></a>

Data Normalisation is a scaling technique that assumes your data is normally distributed (has a bell curve shape) and scales them such that the distribution is now centred around 0, with a standard deviation of 1.

Data Normalisation is very important in the fields of statistics and probability theory.

**Key Points:**

- Data Normalisation helps to bring your values to a normal distribution 🎯.
- It is a critical step in data preprocessing when using Machine Learning Algorithms 🧮.
- Example of data normalisation is Z-transform normalisation.

## Difference Between Data Scaling and Normalisation <a name="difference"></a>

The Main difference between data scaling and data normalisation is that:

- In Scaling, you're changing the range of your data while in Normalisation you're changing the shape of the distribution of your data.
- Scaling is used when you're dealing with features of different scales. Normalisation, on the other hand, is used when your data is not normally distributed.

## When to use them <a name="when_to_use"></a>

Both of these techniques are especially useful when:

- Your dataset contains numerical features that have different scales 😨.
- Some of your features have outliers that you do not want to remove but would like to suppress when training your model.
- Your model assumes that your data is normally distributed (uses terms like mean, standard deviation, etc.),

## Real-world Examples <a name="examples"></a>

- Data scaling can be seen in weather applications where temperature is scaled from not only Fahrenheit to Celsuis 🌡️ but also times on different scales such as 12-hours or 24-hours.
- PCA(Principal Component Analysis) is a perfect example where both Normalisation and Scaling methods are used.
- Text Data in Natural Language Processing is also normalised or scaled for the pipeline in models such as Regression, Support Vector Machines etc.