# Data Manipulation with dplyr-r :computer:

Manipulating datasets to extract meaningful information has always been a core component of data analysis. The dplyr package in R programming is a powerful tool that helps achieve this elegantly and efficiently. Here's a guide to get you started with dplyr in R.

> Created by @jl33-ai :boy:

## Table of Contents

- [1. Introduction](#1-introduction)
- [2. Verb Functions of dplyr](#2-verb-functions-of-dplyr)
- [3. Examples](#3-examples)

### 1. Introduction  :open_book:

dplyr is a part of the tidyverse, an ecosystem of packages designed with common APIs and a shared philosophy. The philosophy of dplyr is to ensure simplicity and flexibility when following common data manipulation tasks. Here, we will discuss some of the most commonly used functions in the dplyr package:
- Selecting specific columns with `select()`
- Filtering rows with `filter()`
- Arranging rows with `arrange()`
- Creating new columns with `mutate()`
- Summarizing data with `summarise()`
- Grouping data with `group_by()`
- Piping `%>%`

### 2. Verb Functions of dplyr :pencil2:

**select()** 

Use this function to choose specific columns in a dataset.

```r
select(data, column1, column2)
```
**filter()**  

This function helps to filter rows based on a certain condition.

```r
filter(data, condition)
```
**arrange()**

This is used to sort data in either ascending or descending order.

```r
arrange(data, column)
```
**mutate()**  

This function allows us to add new variables into the dataset that are functions of existing ones.

```r
mutate(data, new_column = existing_column * operation)
```
**summarise()**  

It's used to summarize multiple values to a single value.

```r
summarise(data, summaryName = summariseFunc(column))
```
**group_by()**  

This is a helper function to group data by one or more variables.

```r
group_by(data, column1, column2)
```
**Piping (`%>%`)**  

This is a powerful operator which helps to transform and manipulate the data in a clean and clear way.

```r
data %>% verbFunction
```
### 3. Examples :mag:

Let's visualize how these functions work using a sample dataset. We are going to use the built-in `mtcars` dataset.

```r
# Load the dplyr package
library(dplyr)

# Use the mtcars dataset
data(mtcars)

# Select mpg and hp columns
mtcars %>%
select(mpg, hp)

# Filter cars with 6 cylinders
mtcars %>%
filter(cyl == 6)

# Arrange by mpg in descending order
mtcars %>%
arrange(desc(mpg))

# Add a new column "total", sum of hp and cyl
mtcars %>%
mutate(total = hp + cyl)

# Summarise the average mpg
mtcars %>%
summarise(avg_mpg = mean(mpg))

# Group by number of gears and cylinders
mtcars %>%
group_by(gear, cyl)
```
As seen through this notebook, dplyr is a versatile package for data manipulation in R and is a vital skill to have in your data science toolkit. Happy coding! :computer::tada::
```