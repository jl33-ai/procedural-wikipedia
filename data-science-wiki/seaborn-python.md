
## Created by @jl33-ai 👦🏻

---

**Seaborn** is a powerful Python library used to create beautiful and informative statistical graphics. Built over Matplotlib, it is often used for visualizing complex data in a simpler form.

#### Table of Contents:

1. [Installation guide](#installation-guide-⚙️)
2. [Introduction to Seaborn](#introduction-to-seaborn-🌈)
3. [Seaborn Functions](#seaborn-functions-🔨)
4. [Plotting with Seaborn](#plotting-with-seaborn-📈)
5. [Exploring Datasets with Seaborn](#exploring-datasets-with-seaborn-🔍)
6. [Visualizing Statistical Relationships](#visualizing-statistical-relationships-🧪)
7. [Multi-Plot Grids](#multi-plot-grids-🔳)
8. [Conclusion](#conclusion-🏁)

---

### Installation guide ⚙️
Installation is straightforward using pip:

```
pip install seaborn
```
Or via conda:

```
conda install seaborn
```
---
### Introduction to Seaborn 🌈
```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```
You can always set themes via set_theme function:
```python
sns.set_theme()
```
---

### Seaborn Functions 🔨
- `sns.lineplot`: Line plot
- `sns.barplot`: Bar chart
- `sns.scatterplot`: Scatter plot
- `sns.histplot`: Histogram
- `sns.boxplot`: Box plot
- `sns.violinplot`: Violin plot
- `sns.heatmap`: Heatmap
- `sns.pairplot`: Pair plot
- `sns.countplot`: Count plot

---

### Plotting with Seaborn 📈

```python
# simple line plot
sns.lineplot(x = 'variable_x', y = 'variable_y', data = dataset)
```

```python
# bar graph
sns.barplot(x = 'variable_x', y = 'variable_y', data = dataset)
```

```python
# histogram
sns.histplot(data = dataset, x = 'variable')
```

---

### Exploring Datasets with Seaborn 🔍
Seaborn provides built-in datasets for exploration:

```python
# Load dataset
tips = sns.load_dataset("tips")

# Print first 5 rows
print(tips.head())
```

---

### Visualizing Statistical Relationships 🧪
Create a relational plot scattering data points between two variables using `relplot()`
```python
sns.relplot(x="total_bill", y="tip", data=tips)
```

---

### Multi-Plot Grids 🔳
Seaborn simplifies the creation of multi-plot grids:

```python
g = sns.FacetGrid(tips, col="time")
g.map(sns.histplot, "tip")
```

---

### Conclusion 🏁
Seaborn offers a high-level, flexible interface for creating statistical graphics that are both informative and attractive. It’s a must-learn library for data artists due to the power and simplicity it provides. 

For detailed information and tutorial, visit the [Seaborn official documentation](http://seaborn.pydata.org/)
