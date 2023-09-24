Created by @jl33-ai 👦🏻

ggplot2 is one of the most widely used packages in R for data visualization. It is built under the Grammar of Graphics, a comprehensive and consistent framework for data visualization.

## Table of Contents

1. [Introduction](#introduction)
2. [Installation](#installation)
3. [Basics of ggplot](#basics_of_ggplot)
4. [Aesthetics](#aesthetics)
5. [Geometries](#geometries)
6. [Statistics](#statistics)
7. [Facets](#facets)
8. [Themes](#themes)

---
## Introduction<a name='introduction'></a>

ggplot2 offers a powerful graphics language for creating elegant and complex plots quickly. Its popularity in the R community has exploded in recent years.

---
## Installation<a name='installation'></a>

To install ggplot2, run the following command in an R console:

```R

install.packages("ggplot2")

```
After installation, you can load the ggplot2 package with:

```R

library(ggplot2)

```
---

## Basics of ggplot<a name='basics_of_ggplot'></a>

The most basic concept of ggplot is the idea of a code structure with different parts that define the plot. 

Here's a general structure of a ggplot command:

```R

ggplot(data = <DATA>) +
  <GEOM_FUNCTION>(mapping = aes(<MAPPINGS>))

```  
  
Here is an example:

```R

ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy))

```

---
## Aesthetics<a name='aesthetics'></a>

Aesthetics describes how your data will relate to your plot. Aesthetic properties include size, shape, color, fill, linetype, etc.

```R

ggplot(data = mpg) +
   geom_point(mapping = aes(x = displ, y = hwy, color = class))

```
---

## Geometries<a name='geometries'></a>

Geometric objects or geoms are the actual marks we put on a plot. Examples of geoms include:

1. Points (geom_point) - for scatter plots, dot plots, etc.
2. Lines (geom_line) - for trend lines, time-series, etc.
3. Boxplot (geom_boxplot) - for, well, boxplots!

```R

ggplot(data = mpg) +
  geom_smooth(mapping = aes(x = displ, y = hwy))

```
---

## Statistics<a name='statistics'></a>

To add a layer of summaries, we can use various stat functions. These functions will compute statistics on the fly for you.

```R

ggplot(data = diamonds) +
  geom_bar(mapping = aes(x = cut))

```
---
## Facets<a name='facets'></a>

With facets, you can create plots for different subsets of your data.

```R

ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy)) +
  facet_wrap(~ class, nrow = 2)

```

---
## Themes<a name='themes'></a>

ggplot2 comes with various themes that can be used to alter the presentation of the plot.

```R
ggplot(data = mpg) +
  geom_point(mapping = aes(x = displ, y = hwy)) +
  theme_bw()

```

Have fun plotting with ggplot2! 🎨 📈📊 
