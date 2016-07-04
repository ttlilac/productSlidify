---
title       : Iris K-mean Clustering Application
subtitle    : Shinny web application
author      : Ding Lei
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Introduction

1. Iris Data Exploring
2. Clustering
3. Shiny Application
4. Reference

--- .class #id 

## Iris Data Exploring

```r
library(datasets)
head(iris)
```

```
##   Sepal.Length Sepal.Width Petal.Length Petal.Width Species
## 1          5.1         3.5          1.4         0.2  setosa
## 2          4.9         3.0          1.4         0.2  setosa
## 3          4.7         3.2          1.3         0.2  setosa
## 4          4.6         3.1          1.5         0.2  setosa
## 5          5.0         3.6          1.4         0.2  setosa
## 6          5.4         3.9          1.7         0.4  setosa
```

--- .class #id 

## Clustering

```r
library(ggplot2)
irisCluster <- kmeans(iris[, 3:4], 3, nstart = 20)
irisCluster$cluster <- as.factor(irisCluster$cluster)
ggplot(iris, aes(Petal.Length, Petal.Width, color = irisCluster$cluster)) + geom_point()
```

![plot of chunk unnamed-chunk-2](figure/unnamed-chunk-2-1.png)

--- .class #id 

## Shiny Application

![width](assets/img/kmeans.png)

--- .class #id 

## Reference



--- .class #id 




