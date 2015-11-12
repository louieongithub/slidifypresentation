---
title       : Data Products
subtitle    : Orange Tree Growth Prediction 
author      : Louie Sakellaris
job         : Coursera Assignment
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
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
summary(fit1)
```

```
## 
## Call:
## lm(formula = circumference ~ age, data = Orange)
## 
## Residuals:
##     Min      1Q  Median      3Q     Max 
## -46.310 -14.946  -0.076  19.697  45.111 
## 
## Coefficients:
##              Estimate Std. Error t value Pr(>|t|)    
## (Intercept) 17.399650   8.622660   2.018   0.0518 .  
## age          0.106770   0.008277  12.900 1.93e-14 ***
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## Residual standard error: 23.74 on 33 degrees of freedom
## Multiple R-squared:  0.8345,	Adjusted R-squared:  0.8295 
## F-statistic: 166.4 on 1 and 33 DF,  p-value: 1.931e-14
```

--- 

## Try it now

Try out the app at https://louieonshinyapps.shinyapps.io/orangeapp  

## Find out if Orange Trees are great hugging trees!
