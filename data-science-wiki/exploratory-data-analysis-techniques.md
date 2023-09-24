#### Created by @jl33-ai 👦🏻

## Table of Contents

1. [Introduction](#intro)
2. [Handling Missing Values](#missing-values)
3. [Handling Outliers](#outliers)
4. [Histograms](#histograms)
5. [Box Plots](#boxplots)
6. [Scatter Plots](#scatter-plots)
7. [Correlation Matrix](#correlation-matrix)
8. [Pairplots](#pairplots)
9. [Heat Maps](#heatmap)
10. [Summary Statistics](#summary-stats)
11. [Conclusion](#conclusion)

<a name="intro"></a>
## Introduction

Exploratory Data Analysis (EDA) is the initial step taken by data analysts and data scientists to understand the basic characteristics, structure, and relationships within a dataset.  Let's explore various techniques used in EDA. 🚀

<a name="missing-values"></a>
## Handling Missing Values

- Missing data is a common occurrence in data analysis, it's important to handle them correctly based on the nature of missing data.
- We can use the following strategies to handle missing values:
   - **Elimination:** Delete the rows/columns with missing data 🗑
   - **Imputation:** Fill the missing values with statistical measures like mean, median or mode 📚
   - **Prediction models:** Use prediction models to estimate the missing values 🧠

<a name="outliers"></a>
## Handling Outliers

- Outliers are extreme values that deviating from other observations in the data.
- We can handle outliers in the following ways:
  - Visualization methods (Box plot, Scatter plot etc.)
  - Z-Score, IQR Proximity rule
  - Trimming, Capping or Winsorization methods 

<a name="histograms"></a>
## Histograms 

- Histograms provide a visual interpretation of numerical data by indicating the number of data points that lie within a range of values.
- They divide the dataset into bins and show the frequency distribution of these bins.
- Example: Visualization of the distribution of ages or income range in a population.

<a name="boxplots"></a>
## Box Plots

- A box plot is a way of statistically representing the distribution of the data through five main dimensions: minimum, First Quartile, median, Third Quartile and maximum.
- Helps to quickly give an understanding of where the bulk of the data falls in the range and whether the distribution is skewed.

<a name="scatter-plots"></a>
## Scatter Plots

- Scatter plots are used for relationship checking or correlation between two numerical variables.
- A scatter plot can also display the correlation between two variables, the closer the data points are to a straight line, the higher the correlation.

<a name="correlation-matrix"></a>
## Correlation Matrix

- A correlation matrix is a table that shows the correlation coefficients between many variables.
- Each cell in the table shows the correlation between two variables.
- It is used to summarize data, as an input into a more advanced analysis, and as a diagnostic for complex analyses.

<a name="pairplots"></a>
## Pairplots

- Pairplots are a really simple (one-line-of-code simple!) way to visualize relationships between each variable. 
- It produces a matrix of relationships between each variable in your data for an instant examination of our data.
- It can also be a great jumping off point for determining types of regression analysis to use.

<a name="heatmap"></a>
## Heat Maps

- A heat map uses color to represent intensity and is perfect for visualizing correlation matrices, geographical data, and more.
- Heatmaps are visually appealing and make interpreting temporal data a breeze.

<a name="summary-stats"></a>
## Summary Statistics

- Summary statistics includes Mean, Median, Mode, Minimum Value, Maximum Value, Range, Standard Deviation, Count etc.
- These provide insights into the central tendency and variability within your dataset.

<a name="conclusion"></a>
## Conclusion

To wrap it up, Exploratory Data Analysis (EDA) facilitates us to understand the subtle patterns, spot anomalies, test hypothesis and check assumptions based on our dataset. It provides a critical bridge from raw data to insights and data driven decision making.
