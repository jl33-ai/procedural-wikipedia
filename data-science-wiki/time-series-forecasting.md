
_An in-depth guide to predicting future values based on previously observed values._

Created by @jl33-ai 👦🏻

## Table Of Contents
- [Introduction](#introduction)
- [Important Concepts](#important-concepts)
- [Types of Models](#types-of-models)
- [Evaluation Metrics](#evaluation-metrics)
- [Conclusion](#conclusion)

---

## Introduction 🚀

_Time series forecasting_ is the process of using a statistical model to predict future values based on previously observed values. It is essential in many fields, including finance, economics, sociology, and even meteorology!

---

## Important Concepts 📚

1. **Trend**: A pattern of change in the time series over time.
2. **Seasonality**: A pattern of change that repeats over regular intervals.
3. **Cyclic**: A pattern of change that repeats, but not at fixed intervals.
4. **Stationary**: A time-series is called stationary if its statistical properties do not change over time. Most of the time-series models work on the assumption that the time-series are stationary. We might have to convert a series into a stationary series.
5. **Autocorrelation**: The correlation of the time-series with a lagged version of itself.

---

## Types of Models 🛠

There are several types of models that are widely used for time-series prediction. These include:

1. **Autoregressive Integrated Moving Average (ARIMA)**
2. **Seasonal ARIMA (SARIMA)**
3. **Vector Autoregression (VAR)**
4. **Prophet**
5. **Long Short-Term Memory (LSTM)**

###### Example 📝

```python
from statsmodels.tsa.arima_model import ARIMA

model = ARIMA(series, order=(5,1,0))
model_fit = model.fit(disp=0)
print(model_fit.summary())

# plot residual errors
residuals = DataFrame(model_fit.resid)
residuals.plot()
pyplot.show()
residuals.plot(kind='kde')
pyplot.show()
print(residuals.describe())
```

---

## Evaluation Metrics 📏

The accuracy of the forecasts can be determined using several metrics. These include:

1. **Mean Squared Error (MSE)**.
2. **Root Mean Squared Error (RMSE)**.
3. **Mean Absolute Error (MAE)**.

###### Example 📝

```python
from sklearn.metrics import mean_squared_error

X = series.values
size = int(len(X) * 0.66)
train, test = X[0:size], X[size:len(X)]
history = [x for x in train]
predictions = []

for t in range(len(test)):
	model = ARIMA(history, order=(5,1,0))
	model_fit = model.fit(disp=0)
	output = model_fit.forecast()
	yhat = output[0]
	predictions.append(yhat)
	obs = test[t]
	history.append(obs)
	print('predicted=%f, expected=%f' % (yhat, obs))
error = mean_squared_error(test, predictions)
print('Test MSE: %.3f' % error)
```

---

## Conclusion 🏁

_Time-series forecasting_ is a valuable technique for predicting future values based on past values. While there are many types of models available for these predictions, selecting the appropriate one depends on the particular dataset at hand.
