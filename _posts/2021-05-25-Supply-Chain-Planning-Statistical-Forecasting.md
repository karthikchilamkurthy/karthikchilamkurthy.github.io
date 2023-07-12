---
title:  Supply Chain Planning - Statistical Forecasting
author: Karthik Chilamkurty
date: 2022-06-07 11:33:00 +0800
categories: [Supply Chain Management]
tags: [Supply Chain Management]
image:
  src: https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__DWgAqRhrUqqzYSJtV8zYgg.jpeg
---

**_Supply chain planning_** is the process of anticipating demand and planning materials and components to supply that demand.**_Demand planning_** is a process of forecasting, or predicting, the demand for products to ensure they can be delivered without surplus.

#### Forecasting Models

Forecasting is an essential part of every business.
- **_prediction_**, guess what demand will do.
- **_Estimation_**, guess what level it will be at.
- **_projection_**, carrying it into the future of demand. 
There are several types of forecasting approaches, we’re going to use time series and time series relies on historical data.

We have demand recorded over time from past until the future.  
we’re sitting here at point t, and this demand data is going to be recorded in equal size intervals of time. So that maybe a day, it maybe week, it maybe a month or even a year.

So, we have this equal size periods of time and we are going to forecast in those same intervals into the future.

## Naive Forecast

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__DtN____gFhwjepXv7fuEmbzA.png){: width="150" .normal}

Dt-1: Demand at the previous time period  
Ft: Forecast at the current time

The naive forecast, It’s naive because all we’re doing is, we’re saying what we sold yesterday, that’s how much we’re going to sell today. What we sell today is the number we’re going to project for tomorrow.

The naive forecast works very well in certain situations, it sometimes works even better than other more complicated methods.

it’s more applicable to use the same month last year(t-12), would be an example of a seasonal naive method.

Now the naive forecast is very noisy because it doesn’t filter out any noise whatsoever. That makes it very nervous but also responsive to changes in demand. Nervous means we have a very volatile forecast.


![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__t0exc0cbvpB1IEXwLa2BVQ.png){: width="600" .normal}



## Cumulative Mean


![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__2nz6HyEFzZnc2__2tZ9O4Cg.png){: width="150" .normal}

Dt: Demand at the time period t  
Ft: Forecast at the current time

In the naive method, we assumed that only the last piece of information is useful in predicting the future, if we think that all prior data is useful in our forecast, That is the idea behind the cumulative mean. We take all of the data that we have, average it, and that is going to represent our forecast.

This forecast is very stable and averages out all the noise, so it really filters it out.


![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__OSomw0FEoKypfmOKDRRgrA.png){: width="600" .normal}

## Forecast Accuracy Measures

you have to measure it’s accuracy, and you can measure how far away it is from the actual demand, which is defined as accuracy, but you also have to consider bias, and bias means is, do you have a tendency to over forecast or under forecast? You don’t want to be too biased in either direction because that degrades the ability to properly forecast the future just as much as accuracy does

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__4ydClKTyKqBPjD__wf5b8cA.png){: width="150" .normal}

Mean Error

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__1lK882WXcHgK4sOt7OvAMg.png){: width="150" .normal}

Mean Absolute Error

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__wED9qi1KV__A88Xppt6lfew.png){: width="150" .normal}

Mean Squared Error

**_Mean Error_** :The simplest form of a forecast accuracy measure is the mean error.Both over forecasting and under forecasting are bad. If you over forecast, that means you have more product than you really needed, so you’re going to have stuff left over. If you under forecast, you’re not going to have enough product, and customers are going to come to your store, not have anything to buy.

**_Mean Absolute Percent Error :_** Unlike the mean error, which was more of a measure of bias, we are going to actually get that accuracy. So we have our demand, minus our forecast.

**_Mean Squared Error :_** what happens when we have a large error, Because we’re squaring the error terms, it becomes much larger because we multiply it by itself. Small errors remain small, but large errors become huge and those huge errors are going to significantly affect our mean squared error, therefore we will be much more sensitive to those large errors.

## Moving Average

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__JanyuQ1U6kQn4eMgwJ6tyQ.png){: width="150" .normal}



Dt: Demand at the current time period  
Ft: Forecast at the current time period  
Dt-1: Take the demand from the previous period  
N: number of data points in the moving average

In the Cumulative Mean method, we think that all prior data is useful in our forecast, If want to look at a moving average that takes a subset of data, averages it, and as we move through time, that average will move with us, we often consider 50 and 200 day moving averages as a comparison for the stock price that we currently have.

The average, as you saw, is a fairly straight forward mathematical function. But in the moving average, we have one big unknown, and that’s called N.

A small N will make the forecast very reactive versus a large N, which makes the forecast very stable, Moving average is a tremendously adaptable forecasting method. You can make it very reactive, you can make it very stable.

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__VywDxI2LePUyLm7br0Bbyg.png){: width="600" .normal}



## Exponential Smoothing

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__6FgDSiiVjKJWmwDtc9jAlQ.png){: width="150" .normal}

Dt: Demand at the time period t  
Ft: Forecast at the current time

For moving average, you have to do trial and error. And this is slightly true for exponential smoothing as well. However, rather than redoing the forecast over and over, all we need to do is change the value of alpha from larger to smaller. And it makes the forecast either more reactive or more stable.  
Now, when you change these different values for alpha, you have to keep looking at your accuracy. If your accuracy is improving, then you’re going in the right direction. If your accuracy’s getting worse, you’re going in the wrong direction.

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__Zsra0y0Bj2XvJfUO15YuPw.png){: width="600" .normal}