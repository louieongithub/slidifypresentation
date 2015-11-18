---
title       : Data Products
subtitle    : Orange Tree Growth Prediction 
author      : Louie Sakellaris
job         : Coursera Assignment
framework   : io2012       # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Tree hugging is great
### Ever wanted to know how big that baby orange tree at the nursery will grow?  

### Now you can with this latest app.  

---

## How this app works



This app was developed using shinyapps and R's Orange data set.   

```r
data(Orange)
head(Orange)
```

```
##   Tree  age circumference
## 1    1  118            30
## 2    1  484            58
## 3    1  664            87
## 4    1 1004           115
## 5    1 1231           120
## 6    1 1372           142
```

---
## The prediction model

This app uses a mathematical model that can predict how big your orange tree will grow.  


```r
fit1<-lm(circumference~age,data=Orange)
summary(fit1)$call
```

```
## lm(formula = circumference ~ age, data = Orange)
```

```r
summary(fit1)$coefficients
```

```
##               Estimate  Std. Error   t value     Pr(>|t|)
## (Intercept) 17.3996502 8.622659801  2.017898 5.179267e-02
## age          0.1067703 0.008276623 12.900228 1.930596e-14
```

--- 

## Try it now

Try out the app at https://louieonshinyapps.shinyapps.io/orangeapp  

## Find out if Orange Trees are great hugging trees!
 ![alt text][id]
 [id]: orangetree.png
 
