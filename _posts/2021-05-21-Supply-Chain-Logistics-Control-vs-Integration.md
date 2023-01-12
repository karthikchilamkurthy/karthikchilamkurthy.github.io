---
title:  Supply Chain Logistics - Control vs Integration
author: Karthik Chilamkurty
date: 2022-05-21 11:33:00 +0800
categories: [SCM, Inventory Management]
tags: [SCM]
image:
  src: https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__hM4uxJvw3V35dirbpbktvA.jpeg
---

Every modern company, lives, thrives by their ability to match supply with demand.

Supply chain makes it affordable for consumers, profitable for companies in a global economy.

Logistics is defined as the movement and storage of goods, services, and related information.

logistics is very essential in today’s global interconnected supply chains, where we can bring companies together through transportation, warehousing, and inventory management.

## Warehousing Management  
We need warehouses in a variety of different situations. One of them is to consolidate our raw material supply. So, let’s imagine a company that has two plants and three raw materials suppliers. Now we could shift from those raw material suppliers directly into both of our plants and it’ll be fine, but there is a better way and that is to use a warehouse in between them that receives raw materials from the three suppliers and then ships out, assembled assortments as needed

Example: You could ship out from those two plans to the five customers individually, but the customer wants an assortment of products produced by both plans. So you instead should use three warehouses to consolidate your output from the two plans, create assortment and then ship them out to your five final customers. This has the same advantages that we had before. It’s more efficient. It reduces the risk and it provides the customer with better service.

Advantages

*   **_Efficiencies in Transportation_** : we focus on each link specifically and make it really good. We can achieve efficiencies in inventory, because we can hold our inventory where it’s needed and just as much as is needed. And then finally, in production, because our production facilities get the resupplies they need when they need them.
*   **_risk pooling_**  : we hold inventories just in one location rather than scattered across this network of companies.

Technology

Implement Warehouse Management Software (WMS) to sequence orders and organize the workflow inside the warehouse,

## Inventory Management 

Inventory is typically made up of two different pieces. One is **_Cycle Stock_**, the other one is **_Safety Stock_**. **_Cycle Stock_**  has to do with the inventory that goes up and down during regular sales and replenishment. **_Safety Stock_** we hold it just in case something we did not anticipate happens. So we don’t really expect it to be used, but it’s there if we need it.

The future is not always certain, that’s why we cannot rely on stock alone and we need something called Safety Stock. Now, uncertainty can come in two forms. One, our **_demand_** is not what we expected it to be. Two, our **_replenishment_** may not arrive when we want it to arrive. And for those reasons, we need to hold Safety Stock.

Example :

Case 1 : without any uncertainty  
selling 20 items per day, replenishment arrives every 10 days

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__ykDtgw4c8cs09QRmFiBRAg.png){: width="350" .normal}

Case 2: Increased Demand  
Let’s assume our products are flying off the shelf rather than selling 20 units worth of product everyday, we sell 25  
We still get our 200 units every 10 days. We also are selling 25 units per day. That means after eight days, we have nothing left.  
**_Safety Stock_** do we needed :25 units per day over 2 days means 50 units worth of Safety Stock

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__p1k9TCbYMNbxt__pA8__7IIQ.png){: width="350" .normal}

Case 3 : Delay in replenishment  
The replenishment did not arrive when we expected to arrive.  
We got our 200 units worth of inventory. We expect it to last for 10 days, but the shipment does not arrive on day 10, it arrives on day 12.  
We need to bridge two days with inventory. We sell 20 units a day. We need 40 units of **_Safety Stock_**

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__jLpjR0__6xd6ajdjOEps8Eg.png){: width="350" .normal}

Case 4 : Both _Increased Demand and_ Delay in replenishment  
we need to hold **_safety stock_** to bridge those 4 days with 25 per day. That means we need 100 units worth of Safety Stock.

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/1__lWMW5qUgE6DPaVd9F6mrnQ.png){: width="350" .normal}

companies are scrutinising that decision very heavily and there are numerous, really thousands, of approaches of how you can determine how much inventory to order each time.

Predicting Inventory (s.Q vs s.S) 
s stands for reorder point  
Q stands for a fixed quantity that is determined ahead of time  
S stands for a variable quantity that depends on the current inventory level as you place the order

The s.Q system is a continuous review method, where we monitor our inventory at all times, and then once we hit the reorder point, we place an order of the same quantity

s.S system, it’s also a continuous review system, however, when we place an order, we are going to place it depending on where we are currently in the inventory. So if we have a lower inventory, the order will be larger, because we order up to a certain level. So the order will be the difference between our current inventory and where we would like to be.

Advantages

Advantages of the s.Q system, is that it’s simple, it’s very predictable for our supplier. However, in certain cases, it may not be as precise and proficient. The s.S method, may make it harder for a supplier, but it is a very precise system of inventory

## Logistics Network

When you have fewer warehouses the advantages are that you locate your inventory in fewer locations, you pool your risk, and therefore are able to hold less inventory. When you have many facilities, you will carry more inventory, but your access to your customer is going to be much quicker, so the decision is a tradeoff. Do you want to save money building facilities and holding inventory, or do you want quicker access to your customers?

Because you can spread your safety stock over a larger area. The risk of stocking out is less with fewer locations. If you have more locations, each location needs their own safety stock, thus we have more safety stock overall in the system

Another interesting way to think about it is that you can use your transportation network as a storage device

It is a nice rule of thumb for estimating the changes in overall inventory as a result of changing the number of warehouses. These calculations are assuming that nothing else changes.

X2 = (X1) \* √ (n2/n1)

n1 = number of existing warehouses n2 = number of future warehouses X1 = existing inventory X2 = future inventory
