# R
> **_Created by @jl33-ai 👦🏻_**

R is a powerful language used for statistical analysis and graphics. It's great for data analysis, data visualization and predictive modelling. R has a fantastic community of bloggers, mailing lists, forums, and is growing rapidly. This guide serves as a basic introduction and reference for R.

**_Table of Contents_**

1. [Installation](#installation)
2. [Data Types](#data-types)
3. [Data Structures](#data-structures)
4. [Control Structures](#control-structures)
5. [Functions](#functions)
6. [Packages and Libraries](#packages-and-libraries)
7. [Data Import and Export](#data-import-and-export)
8. [Data Manipulation and Analysis](#data-manipulation-and-analysis)
9. [Data Visualization](#data-visualization)

---

## 1. Installation <a name="installation"></a>

Download and Install R from the [Comprehensive R Archive Network (CRAN)](https://cran.r-project.org/mirrors.html)

For an Integrated Development Environment (IDE), you can use [RStudio](https://rstudio.com/products/rstudio/download/)

---

## 2. Data Types <a name="data-types"></a>

Basic data types in R include:
- numeric: `5`, `2.5` -> Numbers
- integer: `4L`, `6L` -> Integers
- complex: `3+2i` -> Complex numbers
- logical: `TRUE`, `FALSE` -> Boolean values
- character: `"Hello"`, `"World"` -> Text strings

Example: 

```r
x <- 7   # numeric
y <- 4L  # integer
z <- "R-Language"  # character
```

---

## 3. Data Structures <a name="data-structures"></a>

- Vector: A sequence of data elements of the same basic type. 
- Matrix: A two-dimensional array where each cell is of the same type.
- Array: Can store data in more than two dimensions.
- Data frame: A table where each column can be of a different type.
- List: An ordered collection of objects, can contain different types of elements.

Example:

```r
numbers <- c(1, 2, 3, 4, 5)
fruits <- c("apple", "banana", "cherry")
```

---

## 4. Control Structures <a name="control-structures"></a>

These include if, if else, for, while and repeat. 

Example:

```r
x <- 5
if(x > 0){
  print("Positive number")
}
```

---

## 5. Functions <a name="functions"></a>

Function is a set of statements organized together to perform a specific task. R has a wide variety of inbuilt functions and the user can create their own functions.

Example:

```r
hello_function <- function(name) {
  return(paste("Hello ", name))
}
```

---

## 6. Packages and Libraries <a name="packages-and-libraries"></a>

- `install.packages("package-name")` - To install a package.
- `library(package-name)` - To load a package into R session.

Example:

```r
install.packages("dplyr")
library(dplyr)
```

---

## 7. Data Import and Export <a name="data-import-and-export"></a>

Reading from csv file:

```r
data <- read.csv("data.csv")
```

Writing to csv file:

```r
write.csv(data,"data.csv")
```

---

## 8. Data Manipulation and Analysis <a name="data-manipulation-and-analysis"></a>

- Processing and transforming data.
- Analyzing for patterns or testing hypotheses.
- Reporting the results.

Example:

```r
library(dplyr)

# create a new column, calculate the mean 
data %>%
  mutate(new_col = var1/var2) %>%
  summarise(mean_new_col = mean(new_col, na.rm = TRUE))
```

---

## 9. Data Visualization <a name="data-visualization"></a>

With packages like ggplot2, plotly, and shiny, R can create highly interactive and customizable visuals.

Example:

```r
library(ggplot2)

ggplot(data, aes(x=var1, y=var2, color=var3))+
  geom_point()+
  theme_minimal()
```

---