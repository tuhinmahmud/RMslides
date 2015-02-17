---
title:  Regression Model Analysis using shiny App
subtitle: Coursera - Developing Data Products
author: Tuhin Mahmud
framework: io2012
widgets: [mathjax]
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---


Executive Summary
========================================================
<h3>Synopsis</h3>

The purpose of this project is to look at a data set of a collection of cars.We are interested in exploring the relationship between a set of variables and miles per gallon (MPG) (outcome). We want to answer following two questions:

-"Is an automatic or manual transmission better for MPG"
-"Quantify the MPG difference between automatic and manual transmissions"
<h3>Summary</h3>
Studying ther results of the linear regression and multi variable linear regression we find that automatic transmission is better for MPG but impact of transmission type on MPG is lowered when considered with other variables.

For linear regression the MPG increasses 7.245 MPG , whereas if we consider other important variables like cylinder type , weight and horse power the increase in MPG is about 1.809 MPG.


---

## Build and Analyze Linear Regression Models

Models for analyzing the mtcars dataset




```r
#7 modles for analysis
model1<-lm(mpg~am,data=data)
model2<-lm(mpg~cyl,data=data)
model3<-lm(mpg~cyl+wt,data=data)
model4<-lm(mpg~cyl+wt+hp,data=data)
model5<-lm(mpg~am+cyl+wt+hp,data=data)
model6<-lm(mpg~.,data=data)
model7<-lm(mpg~ wt + qsec + am,data=data)
```

---

## Regression analysis


```
## Warning: package 'ggplot2' was built under R version 3.1.2
```

![plot of chunk unnamed-chunk-3](assets/fig/unnamed-chunk-3-1.png) 

---

## Results
- We accept the alternative hypothesis that model5 is better choice for regression.
- From model5 and the Esitmate coefficient of "am manual" is 1.8092, which is the quantity of impact of transmission type on MPG.
Model 5 statistics is shown below

![plot of chunk unnamed-chunk-4](assets/fig/unnamed-chunk-4-1.png) 

---

## Shinny App and Source Code
- <h3>Shiny App hosted </h3>
    https://tuhinmahmud.shinyapps.io/regressionAnalysis/RM_project.Rmd
- <h3> Source code </h3>
    https://github.com/tuhinmahmud/RegressionModelApp
- <h3> Slidify Slides </h3>
    http://tuhinmahmud.github.io/RMslides
