---
title:  Supply Chain Operations - Optimising Inventory
author: Karthik Chilamkurty
date: 2022-05-27 11:33:00 +0800
categories: [SCM, Inventory Management, statistics]
tags: [SCM, Statistics]
image:
  src: https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__hM4uxJvw3V35dirbpbktvA.jpeg
---

In supply chain, operation refers to the process of transformation. We transform input, raw material, machinery, and labor into outputs, our finished products

When we look at how to make operations better, we focus on four primary goals. Cost, quality, speed, and flexibility.

Now how do companies make their operations better?  
**_optimisation_**, you have to define your objective. It may be to minimize cost, increase speed, achieve perfect quality or more flexibility, nevertheless, you have certain parameters that you can change. You change the way you use machinery.  
But, you cannot change them too much. There are certain constraints placed on your operations.

### Lean Inventory

If you have well planned production, why should you hold lots and lots inventory  
Holding costs are often wrongly accounted for. In other words, most companies underestimate the amount of money it takes to hold inventory. And this really causes them to hold too much inventory. Because they don’t think it costs them a lot.

EOQ model **_Economic order quantity_** (**_EOQ_**) is the ideal order quantity a company should purchase to minimize inventory costs such as holding costs, shortage costs, and order costs

## Holding Cost

*   Capital costs:which is we take into account the cost of money.
*   Inventory operational cost: If we take into account the service costs which are taxes and insurance on inventory.
*   Risks costs: Things may go out of style, they break, or they expire.

If holding costs are higher, your optimal inventory levels are going to go down. Because you will hold less inventory and order more often. We can lower the level of inventory also by looking at our order cost

### Storage costs

All the warehouses, equipment, and labor to maintain that level of inventory.

Order Costs

*   Order submission : we can look at automation and using technology to generate automatic orders that don’t require human intervention, which is expensive
*   Order Receipt : we can use automation, better technology, and better management methods, to make unloading trucks and putting away the inventory more efficient. Therefore, overall reducing the order cost.

if we have lower cost of placing orders, we will place them more often, therefore reducing the average level of inventory.

### Economic Order Quantity Calculation  
calculate the order quantity and the total cost resulting from that order quantity.


![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__Ql8dOvCM__9IjzZ__kEtiCFg.jpeg){: width="150" .normal}

<br>

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__3twyd0xdGwPmlcUjXSkgpA.jpeg){: width="150" .normal}

TC = Total Cost of Ordering and Holding Inventory  
Q = Order Quantity :how much we order each time  
D = Demand : how much we sell in a given period Annually)  
V = Value of the item : purchase cost or production cost  
O = Order Cost : on-time cost of placing and receiving an order  
C = Inventory Carrying Cost :expressed as a percentage of the value of the item

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__Sr__QQjZYxCYZ4fvd__SSYrg.png){: width="600" .normal}

<br>


![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__KAU0cedQs__eqFxLKnOBIkQ.png){: width="500" .normal}


### The Safety Stock Calculation

SS = safety stock  
k = service factor  
Sc = combined standard deviation of lead time and demand  
t = average replenishment lead time  
Sd = standard deviation of daily sales  
d = average daily sales  
St = standard deviation of replenishment cycle

Step 1: Calculate the Combined Standard Deviation of Lead Time and Demand

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__rZ5xhbX__ZzyP7M7If84irg.png){: width="150" .normal}

Step 2: Pick your desired Service Level  
This step depends on how much inventory you can carry to prevent a stockout. The higher the service level the more inventory you need to carry. Most companies pick a service level between 90% and 99%

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__QgDCBtRHrK1Tcvx1LZunQw.png){: width="350" .normal}

Step 3: Calculate the Safety Stock

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__fqlieLYunHNN__c__eqttKQQ.png){: width="150
" .normal}

<br>

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__O55i8LDzLdt3sKZW6ZaFZA.png){: width="500" .normal}