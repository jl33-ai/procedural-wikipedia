# Time-Series Decomposition 📈 

### Created by @jl33-ai 👦🏻

This document explains time-series decomposition, a fundamental process in time-series analysis that breaks a series down into separate components.

## Contents
1. [What is Time-Series Decomposition?](#decomposition)
2. [Components of Time-Series Decomposition](#components)
3. [Types of Time-Series Decomposition](#types)
4. [Applications of Time-Series Decomposition](#applications)
5. [Examples](#examples)

<a name="decomposition"></a>
## 🤔 What is Time-Series Decomposition?

Time-Series Decomposition involves separating a time-series into distinct components, each representing an underlying pattern category. The main goal is to simplify the series and make it easier to analyze and understand.

<a name="components"></a>
## 👓 Components of Time-Series Decomposition

A time-series data can generally be decomposed into three components:

- **Trend**: 📈 These are patterns that happen in the long-term (annual/seasonal).
- **Seasonality**: 🔄 Patterns that repeat at regular intervals (hourly, daily, weekly, monthly, etc.)
- **Random (Irregular or Remainder)**: 🎲 The unpredictable part which can't be attributed to the trend or seasonality.

<a name="types"></a>
## 🛠 Types of Time-Series Decomposition

There are two main types of time-series decomposition:

1. **Additive Decomposition**: The components are added to form the original time-series. 

    `Original series = Trend + Seasonality + Random`

2. **Multiplicative Decomposition**: The components are multiplied together to form the original time-series. 

    `Original series = Trend * Seasonality * Random`

The type of decomposition used depends on the nature of the time-series.

<a name="applications"></a>
## 🎯 Applications of Time-Series Decomposition

Time-series decomposition is primarily used in:

- Forecasting
- Anomaly detection
- Understand underlying patterns and trends

<a name="examples"></a>
## 📖 Examples

Let's look at a simple example using Python:

```python
import pandas as pd
from statsmodels.tsa.seasonal import seasonal_decompose

# Load dataset
df = pd.read_csv('AirPassengers.csv', index_col='Month', parse_dates=True)

# Apply decompose method 
result = seasonal_decompose(df['#Passengers'], model='multiplicative')

# Plot the original data, the trend, the seasonality, and the residuals 
result.plot()
```

In the above script, we first import the necessary libraries. We then load the 'AirPassengers' dataset and create a decomposition object, 'result', using the `seasonal_decompose` function from the `statsmodels` library. The `model='multiplicative'` argument specifies the type of decomposition. Lastly, we plot the decomposed time series.

## Conclusion

Time-series decomposition is a preliminary and crucial step in analyzing a time series data. It provides us with useful insights into the data's underlying structures and patterns which can be used in forecasting, outlier detection, and other analyses.