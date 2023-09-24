# Exponential Smoothing Methods 📊🧮
Created by @jl33-ai 👦🏻

Exponential smoothing methods are time series forecasting methods for univariate data. These methods use weighted averages of past observations to forecast new points. 

## Table of Contents
1. [Simple Exponential Smoothing (SES)](#simple-exponential-smoothing) 🪜
2. [Holt's Linear Exponential Smoothing](#holts-linear-exponential-smoothing) 📉
3. [Holt-Winters' Exponential Smoothing](#holt-winters-exponential-smoothing) ❄️

## Simple Exponential Smoothing (SES) <a name="simple-exponential-smoothing"></a> 🪜
Simple Exponential Smoothing is suitable for forecasting data with no clear trend or seasonal pattern.  

- Forecast, level, and error are calculated with these formulas:  

    `Forecast = Level`
    
    `Level = alpha*Observation + (1-alpha)*Level`
    
    `Error = Observation - Forecast`
    
- Alpha is smoothing constant for level. 

## Example of SES:
```python
from statsmodels.tsa.holtwinters import SimpleExpSmoothing
train, test = data[:100], data[100:]
model = SimpleExpSmoothing(train)
model_fit = model.fit(smoothing_level=0.3,optimized=False)
forecast = model_fit.forecast(steps=len(test))
```

## Holt's Linear Exponential Smoothing <a name="holts-linear-exponential-smoothing"></a> 📉
Holt extended SES to allow the forecasting of data with trends. Uses two smoothing constants, one for level (alpha) and one for trend (beta).

- The level and trend equations are:
    
    `Level = alpha*Observation + (1-alpha)*(Level + Trend)`
    
    `Trend = beta*(Level - Level_prev) + (1-beta)*Trend`
    
- Alpha is smoothing constant for level, beta is smoothing constant for trend. The trend is a simple difference between the current level and the level of previous moment.

## Example of Holt's Exponential Smoothing:
```python
from statsmodels.tsa.holtwinters import Holt
model = Holt(train)
model_fit = model.fit(smoothing_level=0.3, smoothing_slope=0.1,optimized=False)
forecast = model_fit.forecast(steps=len(test))
```

## Holt-Winters' Exponential Smoothing <a name="holt-winters-exponential-smoothing"></a> ❄️
Holt-Winters' method is suitable for data with trends and seasonalities. It introduces a third smoothing equation for seasonality.

- Forecasts, level, trend, and seasonal are calculated with these equations:

```python
Forecast = (Level + Trend*M) * Seasonal

Level = alpha*Observation/Seasonal + (1-alpha)*(Level + Trend)

Trend = beta*(Level - Level_prev) + (1-beta)*Trend

Seasonal = gamma*Observation/Level + (1-gamma)*Seasonal
```

- Alpha is smoothing constant for level, beta is for trend, and gamma is for seasonality.

## Example of Holt-Winters' Exponential Smoothing:
```python
from statsmodels.tsa.holtwinters import ExponentialSmoothing
model = ExponentialSmoothing(train, trend='add', seasonal='add', seasonal_periods=12)
model_fit = model.fit(smoothing_level=0.3, smoothing_slope=0.1, smoothing_seasonal=0.1,optimized=False)
forecast = model_fit.forecast(steps=len(test))
```