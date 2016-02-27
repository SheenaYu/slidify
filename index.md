---
title       : Life Expectancy Prediction
subtitle    : Developing Data Products - Final Project
author      : Sheena
job         : Student
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides

---
## Introduction
* The purpose of this project is to make prediction for the life expectancy of people in a area given three predictors:
  Murder rate, Percent of High-school graduates and number of frost days


## Data Examination

* The data set I use is a built-in data set called state.x77. Let's take a brief look at the data set (first 6 observations):

```
##            Population Income Illiteracy Life Exp Murder HS Grad Frost   Area
## Alabama          3615   3624        2.1    69.05   15.1    41.3    20  50708
## Alaska            365   6315        1.5    69.31   11.3    66.7   152 566432
## Arizona          2212   4530        1.8    70.55    7.8    58.1    15 113417
## Arkansas         2110   3378        1.9    70.66   10.1    39.9    65  51945
## California      21198   5114        1.1    71.71   10.3    62.6    20 156361
## Colorado         2541   4884        0.7    72.06    6.8    63.9   166 103766
```

--- 

## Predictors Selection
After stepwise regression to reach the minimum adequate model, I choose Murder, HS Grad and Frost as the independent variables which are statistically significant at level of 0.05, to predict the life expectancy of a specified area.

```
## 
## Call:
## lm(formula = Life.Exp ~ Murder + HS.Grad + Frost, data = st)
## 
## Residuals:
##     Min      1Q  Median      3Q     Max 
## -1.5015 -0.5391  0.1014  0.5921  1.2268 
## 
## Coefficients:
##              Estimate Std. Error t value Pr(>|t|)    
## (Intercept) 71.036379   0.983262  72.246  < 2e-16 ***
## Murder      -0.283065   0.036731  -7.706 8.04e-10 ***
## HS.Grad      0.049949   0.015201   3.286  0.00195 ** 
## Frost       -0.006912   0.002447  -2.824  0.00699 ** 
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## Residual standard error: 0.7427 on 46 degrees of freedom
## Multiple R-squared:  0.7127,	Adjusted R-squared:  0.6939 
## F-statistic: 38.03 on 3 and 46 DF,  p-value: 1.634e-12
```

---
## Plot Fit

<img src="assets/fig/unnamed-chunk-3-1.png" title="plot of chunk unnamed-chunk-3" alt="plot of chunk unnamed-chunk-3" style="display: block; margin: auto;" />



---
## Model Prediction
* Murder rate and frost days have a negative relationship with life expectancy, while the percentage of high-school graduates has a positive relationship.


* UI: The left tab give users an interactive function to put in values they desire. The main panel on the right will display corresponding results.

* Now you can try to input the values and check the predictions. 

* The data app is hosted on https://sheenayu.shinyapps.io/coursera_project/

## Thank You !





