# Interactive Visualisation Tools :chart_with_upwards_trend: :bar_chart:
##### Created by @jl33-ai 👦🏻

Interactive visualization tools are software programs that allow users to create and manipulate digital visual content. In the world of Data Science, these provide an engaging way to present data by allowing viewers to interact with their results.

Here are some of the powerful and most commonly used interactive visualization tools by Data Scientists and ML practitioners:

## 1. Matplotlib :art:
Matplotlib is a standard graphing library that produces publication quality figures. One can generate plots, histograms, power spectra, bar charts, error charts, scatterplots, etc.

```python
import matplotlib.pyplot as plt
plt.plot([1, 2, 3, 4])
```

## 2. Seaborn :ocean:

Seaborn is a library in Python predominantly used for making statistical graphics. Seaborn is a superset of Matplotlib and to make a graph more attractive you can use seaborn functions.

```python
import seaborn as sns
penguins = sns.load_dataset("penguins")
sns.pairplot(penguins)
```

## 3. Plotly 🌌

Plotly is a modern platform for plotting static, animated, and interactive visualizations in Python. We can make plots using Plotly for data analysis and also to make visually attractive representations online.

```python
import plotly.graph_objects as go

fig = go.Figure(data=go.Bar(y=[2, 3, 1]))
fig.show()
```

## 4. Bokeh :bokeh:

Bokeh is a powerful library that allows for quick design and styling of plots, which can then be viewed in a browser. Because they are interacted with in a browser, the data visualization produced using Bokeh are very user-friendly.

```python
from bokeh.plotting import figure, show

p = figure(plot_width=500, plot_height=400)
p.circle([1, 2, 3, 4, 5], [6, 7, 2, 4, 5])
show(p)
```

## 5. GGplot :ggplot:

ggplot is a robust plotting package for creating complex, multi-layered visualizations. It’s based on R’s ggplot2 and the Grammar of Graphics by Leland Wilkinson.

```python
from ggplot import *

ggplot(aes(x='date', y='beef'), data=meat) +\
    geom_line() +\
    stat_smooth(colour='blue', span=0.2)
```   

What tool you choose will ultimately depend on how complex your visualization needs to be. Matplotlib is suitable for customized static plots, Seaborn and GGplot is for complex statistically oriented visualizations, Bokeh and Plotly can generate more user-friendly interactive plots.