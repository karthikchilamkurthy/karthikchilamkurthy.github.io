---
title:  Supply Chain Analytics - Introduction.
author: Karthik Chilamkurty
date: 2023-07-11 11:33:00 +0800
categories: [Supply Chain Analytics]
tags: [Supply Chain Management]
math: true
image:
  src: 
---

## **_What is Supply Chain Analytics?_**

Let's take an example of buying a product, In our case let's take the pair of shoes!

We rarely consider the origin of its materials, how they were manufactured, modes they were transported.

Each of above question have answers and each answer can be written or extracted in a form of data.

For example as a store manager, when you request stock of particular shoe model from factory, there are many factors to be considered, following are few factors need to be analyzed for your request.

- **_Warehouse_**: Is Stock available at factory warehouse?, if available, How much stock is needed considering forecast?
- **_Production_**: If there is spike in demand for that particular model, How many shoes needs to manufacture?
- **_Transportation_**: What is the best mode to transport considering amount of orders?

Huge amount of data is generated when we consider from production of raw materials followed by manufacturing, warehousing, transporting to sales, discounts, marketing of a product.

With huge amount of data generated from different parties of Supply Chain(ref: <https://karthikchilamkurthy.github.io/categories/supply-chain-management/>), it is bedrock to modern supply chain to analyze manually.

Supply chain analytics allow companies to gain insights and extract value from large amount of data throughout various supply chain disciplines to increase efficiency, responsiveness. Supply chain analytics is an essential element of Supply Chain Management(SCM).

## **_Information Flow_**

Let's take the example of a Shoe making Group that has stores all around the world, From Manufacturing Unit to Customer the flow of product as below

- Factories manufacture product and replenish them to warehouses
  + Planning teams to provide the Forecasts to support Production
  + Transportation Planners Create the Schedules to Ship the orders
  + Data generated from Third Party Vendors

- Warehouse Load, pack and Distribute the orders to store
  + Supply Planners send orders to the manufacturing units using ERP 
  + External Data sources were used if Third Party Vendors are used as part of warehousing and packing

- Retail Stores receives the orders
  + Distribution Planners Create orders
  + Sales team Collect sales and marketing data from stores

With the data available, An important goal is to optimize flow of goods by improving forecasting, efficiency and more responsive to customer needs, 

## **_Types of Supply chain Analytics_**

Supply chain Analytics is involving Different set of methods and tools that use supply chain information to identify, react and plan the flow of goods.

## ***_Descriptive Analytics_***

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/descriptvie.png
){: width="450" .normal)

A set of tools, mostly visualization tools are used in Descriptive Analytics, The Final deliverable is usually a set of dashboards

It helps in interpret what has happened, detect incidents and measure operational performance

Variety of statistical methods are involved in understanding the Distribution of data

Taking example of shoe making group, The company gathers millions of data points from Transportation Vendors, including information about location, Fuel charge, back haul charge, Km's driven, Truck type, Shipments, origin, destination etc.

- Transportation Control tower to analyze fuel, back haul metrics for all deliveries across globe

## ***_Diagnostic Analytics_***

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/diagnostoc.png){: width="450" .normal)

It is crucial to figure out what's behind if something happened, for example Sudden spike in demand, Change in transportation expenses. Company can acquire insights from the pattern of core cause trends they have noticed in their data by applying diagnostic analytics.

Diagnostic analytics is also termed as "Root Cause Analysis", it requires previous data, It makes use of variety of methods, including probability theory, Regression analysis, time-series analysis and more.

When performing Diagnostic analytics, with the assistance of technology analysts go deep into the data in search of patterns, trends, hidden correlation between variables, detect and explain outliers.

- Sales team identify a spike in amount charged in particular route by insights provided by Descriptive Analytics team, After Exploratory data analysis, they find the attributes most highly correlated with store orders, region and timing living in Northern states

- From there, The Team could conduct research with the specific transportation route and learn about demand in sales, causes of demand etc

## ***_Predictive Analytics_***

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/predective.png){: width="450" .normal}

The Idea behind Predictive Analytics is to make use of past data to predict future events or behaviors, It is one of the most popular branches of the statistics within the data analytics field.

By Leveraging Predictive Analytics, Companies can anticipate customer demand, optimize inventory, and reduce costs, it utilizes data and advanced algorithms like regression, classification techniques, etc. to optimize the network.

- Considering the hindsight from Diagnostic Analytics team, Predictive Analytics team modeled a Machine learning algorithm using feature engineering, Statistical modeling and fine-tuned the model.

- This model optimizes the back haul that reduces the fuel expenses on that particular Route

## ***_Prescriptive Analytics_***

Prescriptive Analytics is a type of Advanced analytics that optimizes decision-making by providing a recommended action, it works on the results given by Predictive Analytics.

Predictive Analytics help in understanding what future demands are likely to be, while Prescriptive Analytics analyzes the likely impact based on decisions, Prescriptive Analytics identifies and advices on possible outcomes before decisions are made.

Prescriptive Analytics evaluate the potential risks and change their course of action accordingly, this lowers the chances for human bias or error.

Specific techniques used in prescriptive analytics include simulation, game theory, decision analysis methods.

- Considering the foresight provided by Predictive Analytics, Prescriptive Analytics team made an efficient route planning based on likely changes in traffic, blockers and other factors

- This model optimizes the route that foreseeing the impact that may have potential risks in future

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/types.png){: width="450" .normal}


The ultimate goal of Supply chain analytics is to create an efficient supply network!