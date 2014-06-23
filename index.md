---
title       : Get company Information
subtitle    : 
author      : Anirban Basu
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Application Description

<b>Use of Crunchbase base API to retrive company information</b>




Input - Organization name ex organization/Microsoft using an dropdown selection method

Output-Table of company data

--- 

## Crunchbase API



<b>Example Call</b>





data=crunbaseinfo("organization/IBM")

Note-This slide might take time as there is a call to retrieve data from internet.

--- 

## Data Description for IBM


```r
head(data, 2)
```

```
##    id         type
## 1 IBM role_company
## 2 IBM  description
##                                                                                                                                                                                                                                                                                                                                                                                                                                                   value
## 1                                                                                                                                                                                                                                                                                                                                                                                                                                                  TRUE
## 2 IBM, acronym for International Business Machines, is a multinational computer technology and consulting corporation. The company is one of the few information technology companies with a continuous history dating back to the 19th century. IBM manufactures and sells computer hardware and software, and offers infrastructure services, hosting services, and consulting services in areas ranging from mainframe computers to nanotechnology..
##          cat
## 1 properties
## 2 properties
```


--- 

## Some characteristics of information 

Example total count of information per category

```r
table(data$cat)
```

```
## 
##    offices properties 
##          7         16
```


--- 
