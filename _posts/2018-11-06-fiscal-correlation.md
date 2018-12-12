---
title: Fiscal Correlation
image: /images/correlationmatrix.jpg
author: Michael Bottom
categories:
    - financial
    - correlation
layout: post
---

## Method
The yearly financial reports were scraped from internet financial databases. Once the data was collected, I calculated the aggregate or sum of the stats and created a column for that in MS Excel. Then I calculated a mean of the total stats and created a column for that also. The file was saved in csv format and imported into RStudio.

In RStudio I verified the calculations of the means column in the financial stats, for data quality checking. I transposed the data, switching the x and y axis. I needed the stock name as column names. AMZN1 through AMZN6 refer to the Amazon financial stats for years 2012 through 2017. Similarly for WMT(1-6) for Walmart, TGT(1-6) for Target, BBY(1-6) for Best Buy, and COST(1-6) for Costco. I performed data reduction by removing the column that contained the names of the financial stats using the NULL keyword because it was not numerical data. I performed some test plotting and correlation checking. Then I ran a normalization function on the data. I assigned the data frame to a variable, and then plotted another correlation matrix.

![R Correlation Matrix]({{site.baseurl}}/images/Correlation-matrix-six-years.jpg)



## Analysis    
Looking at the correlation matrix, it was useful to compare one year of a stock of with its correlation to other years of the same stock. For example, comparing COST1 (Costco 2012) to the other Costco years showed it was markedly different from the other years (.9973822 correlation with 2017). 2012 was the year that Costco’s sales increased the most compared to the other years. Looking at BBY2 (Best Buy 2013) also showed a noticeable difference in correlation with the other Best Buy years (.9971878 correlation with 2016). That is the year that Best Buy’s sales dropped the most compared to the other years.
The correlation matrix also showed that in 2017 both Amazon and Costco had lower correlation with the mean, (.9510914 correlation with the mean) (.9907068 correlation with the mean) respectively, than the other companies. And it matches up with both companies having the two largest increases in their liabilities of the group that year. 

It was also clear that Amazon, Walmart, and Target were the most correlated companies to each other out of the group of five online retailers when comparing intergroup correlation.  Overall the correlation matrix was mostly useful here for comparing a company to itself over time and looking for changes in the correlations. And it was also useful for looking at companies’ correlation with the group mean. It did not turn out to be useful for tracking stock value volatility in correlation to financial stats because yearly quarterly reports do not have the granularity needed that quarterly reports would have provided. Also, not being able to retrieve the 52-week high and 52-week low stats of the companies’ stocks from the deprecated Google or Yahoo Finance APIs meant that I had to use sales per share instead, which was not as useful for measuring stock value volatility.

## Github Link
https://github.com/MLBott/r-fiscal-correlation (with R files)




