Created by @jl33-ai 👦🏻

`Prophet` is a procedure for forecasting time series data. It is based on an additive model where non-linear trends are fit with yearly and weekly seasonality, plus holidays. It works best with time series that have strong seasonal effects and several seasons of historical data. 

## Table of Contents 📚

- [Installation](#Installation)
- [How It Works](#How-It-Works)
- [Prophet Forecasting Model](#Prophet-Forecasting-Model)
- [Using Prophet](#Using-Prophet)
- [Final Words](#Final-Words)

### Installation

```bash
pip install fbprophet
```
It is important to note that `pystan` is a prerequisite for `prophet`.

### How It Works

* Prophet uses an additive regression model with four main components:
   * A piecewise linear or logistic growth curve trend. 
   * A yearly seasonal component modeled using Fourier series.
   * A weekly seasonal component using dummy variables.
   * A user-provided list of important holidays.

### Prophet Forecasting Model

```python
from fbprophet import Prophet

# Creating instance of Prophet
model = Prophet()

# Fit the model with the time series data
model.fit(df)  
```

### Using Prophet

* Use Prophet to make future predictions:

```python
# Create a future dataframe for 2 years
future = model.make_future_dataframe(periods=730)

# Make prediction
forecast = model.predict(future)
```
* Visualize the forecast:

```python
model.plot(forecast);
```
### Final Words

Prophet shines when it comes to forecasting data that contains trends and seasonality. The fact that it accounts for holidays gives it an advantage, especially for retail and sales forecasting. 

For more detailed information, visit Prophet’s official documentation [here](https://facebook.github.io/prophet/docs/quick_start.html#python-api).

