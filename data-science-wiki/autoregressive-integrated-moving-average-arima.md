# Autoregressive Integrated Moving Average (ARIMA) 📈
> Created by @jl33-ai 👦🏻  

An Autoregressive Intergraded Moving Average (ARIMA) model is a class of statistical models that are widely used for time-series forecasting. In this document, we will explore what makes ARIMA model unique and how it is used in time-series analysis.

---

## Table of contents 📚

1. [Introduction to ARIMA](#introduction-to-arima)
2. [Components of ARIMA](#components-of-arima)
3. [Application of ARIMA](#application-of-arima)
4. [ARIMA in Python](#arima-in-python)

---

<a name="introduction-to-arima"></a>
## 1. Introduction to ARIMA 🚀

- ARIMA, which stands for AutoRegressive Integrated Moving Average, is a forecasting algorithm based on the idea that the information in the past values of the time series can be used to predict the future values.
- It is a generalization of the simpler AutoRegressive Moving Average and adds the notion of integration.
- An ARIMA model is characterized by 3 terms: p, d, q.

<a name="components-of-arima"></a>
## 2. Components of ARIMA 📊

- **p** or Autoregressive part: The number of lag observations in the model. (AR)
- **d** or Integrated part: The number of times that raw observations are differenced for stationarity. (I)
- **q** or Moving average part: The size of moving average window. (MA)

These three parameters are called the order of the ARIMA model.

<a name="application-of-arima"></a>
## 3. Applications of ARIMA 💻

ARIMA models are used for :

- Stock price forecasting
- Forecasting the number of viewers of a show
- Predicting the number of passengers in airlines
- And many other time series related forecasting.

<a name="arima-in-python"></a>
## 4. ARIMA in Python 🐍
Here's how you can use the ARIMA model in Python:

```python
# Importing the necessary libraries
from statsmodels.tsa.arima_model import ARIMA
import pandas as pd

# Loading the dataset
data = pd.read_csv('dataset.csv')

# Fitting the model
model = ARIMA(data, order=(1,1,1))
model_fit = model.fit(disp=0)

# Making predictions
forecast = model_fit.predict(start=2, end=10, typ = 'levels')

print(forecast)
```

Note: Modify the order=(1,1,1) based on your dataset and requirements.

---

And that's all about applying ARIMA to time-series forecasting! Let's keep exploring. 