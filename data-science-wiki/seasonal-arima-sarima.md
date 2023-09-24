> Created by @jl33-ai 👦🏻

---

SARIMA, short for **Seasonal AutoRegressive Integrated Moving Average**, is a type of ARIMA model that captures the seasonality in the data. 

## Table of Contents:

1. [ARIMA](#ARIMA)
2. [Seasonal ARIMA](#Seasonal-ARIMA)
3. [How to Choose Parameters for SARIMA](#How-to-Choose-Parameters-for-SARIMA)
4. [Building a SARIMA Model](#Building-a-SARIMA-Model)
5. [Critiques and Considerations](#Critiques-and-Considerations)

---

### ARIMA <a name="ARIMA"></a>

- ARIMA models are denoted by the notation ARIMA(p, d, q) where:
    - 🅿️ **p** is the order of the **AutoRegressive** part
    - 🅳️ **d** is the order of differencing necessary to make the time series stationary
    - 🅠️ **q** is the order of the **Moving AVerage** part

---

### Seasonal ARIMA <a name="Seasonal-ARIMA"></a>

- SARIMA models are an extension of ARIMA models that explicitly support univariate time series data with a seasonal component.
- They are denoted as SARIMA(p,d,q)(P,D,Q)m.
    - **P**: Seasonal autoregressive order.
    - **D**: Seasonal difference order.
    - **Q**: Seasonal moving average order.
    - **m**: The number of time steps for a single seasonal period.

---

### How to Choose Parameters for SARIMA <a name="How-to-Choose-Parameters-for-SARIMA"></a>

- There are several techniques to estimate the parameters `(p,d,q)` and `(P,D,Q)`.
    - **Identification**: Estimating the order of differencing and the order of the AR and MA process.
        * We look at the **ACF** and **PACF** plots to identify these orders.
    - **Estimation**: Estimate the nature of the AR and MA processes and the parameters.
    - **Diagnostic Checking**: Check the residuals of the identified model by plotting **ACF** of residuals, conducting the **Ljung-Box** test, etc.

---

### Building a SARIMA Model <a name="Building-a-SARIMA-Model"></a>

Below is a basic example of how to use the SARIMA model with the Python `statsmodels` library. 

```python
from statsmodels.tsa.statespace.sarimax import SARIMAX

# fit model
model = SARIMAX(data, order=(1, 1, 1), seasonal_order=(1,1,1,1))
model_fit = model.fit(disp=False)

# make prediction
yhat = model_fit.predict(len(data), len(data))
print(yhat)
```

---

### Critiques and Considerations <a name="Critiques-and-Considerations"></a>

- SARIMA models can be a very effective method for time series forecasting, but they are not without their limitations:
    - They assume that the time series is stationary, which is often not the case.
    - They can be sensitive to the choice of the order parameters.
    - They can be complex to interpret and tune. 

For these reasons, it's often a good idea to try a variety of forecasting strategies for any given problem, and not to rely exclusively on SARIMA.

---
