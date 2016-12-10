---
title: "README_parking_prediction"
author: "likk"
output: html_document
---

## Introduction
The following project challenge is provided by Smarking. Smarking is a driven group of MIT PhDs, engineers, and business professionals who set out on a journey to bring cutting edge solutions to the parking world. In our current 11-person team, there are 5 people from MIT, 6 with PhD background, and two serial entrepreneurs. In the past year, our business grew at an average pace of over 40% month-over-month, and we are post-revenue.

This challenge is part of the application for their software engineering position. You are also welcome to complete it for your own practice, it's a great analytics exercise.

## Project Description
The given data set (transations.csv) consists of more than three years of parking transaction data (from Jan 1, 2013 to Jan 31, 2016). There are two columns: entry time and exit time. Each row represents one transaction. Times are represented in ISO format.

Data Set: https://www.dropbox.com/s/g0ucylnjz375nhv/trans.csv?dl=0

For example:
```{r, eval=FALSE, message=FALSE}
entry time, exit time
2015-01-01 01:32:25, 2015-01-01 03:02:52
2015-01-01 01:58:11, 2015-01-01 06:39:03
```
We would like to provide one-month occupancy (number of cars in the garage) prediction to our clients. To be more specific, we would like to provide estimated occupancy for each of the following hours:
```{r, eval=FALSE, message=FALSE}
[2016-02-01 00:00:00, 2016-02-01 01:00:00, ..., 2016-02-29 23:00:00]
```
Requirements:

Provide hourly predicted occupancy numbers for all the hours above in a csv file.
Provide an interactive prediction chart on a web page. It should at least allow users to hover and see the number of each data point.
Provide an interface to allow users to upload csv files with actual occupancy numbers. Visualize the actual numbers with the predicted numbers in the same chart after the upload completes. The csv file is in the following format:
```{r, eval=FALSE, message=FALSE}
 hour, occupancy
 2016-02-01 00:00:00, 100
 2016-02-01 01:00:00, 125
...
```
 If actual occupancy numbers are provided, calculate the accuracy of your prediction and show the number on the web page. The measurement could be of your choice. Explain why you make that choice.
 
## Result Demonstration
Step1: Transform raw entry and exit time data into hourly occupancy data

Step2: Develop linear regression model using above data and improved model accuracy to above 0.9 of R-square value by tuning hyper parameters

Step3: Setup Website using Flask as backend and bootstrap as frontend to provide interactive hourly occupancy prediction

Step4: Add daily parking calendar, monthly heatmap, daily linechart, prediction chart and actual occupancy chart

 
### Daily Parking Calendar

<img src="http://ogx7uv5qv.bkt.clouddn.com/calendar.png" >
 
### Monthly Heatmap
<img src="http://ogx7uv5qv.bkt.clouddn.com/heatmap.png" >

### Daily Linechart
<img src="http://ogx7uv5qv.bkt.clouddn.com/linechart.png" >

### Prediction Chart
<img src="http://ogx7uv5qv.bkt.clouddn.com/prediction.png" >

### Actual Occupancy Chart
<img src="http://ogx7uv5qv.bkt.clouddn.com/actual_compare2.png" >
 
