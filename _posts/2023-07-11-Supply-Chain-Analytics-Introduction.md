---
title:  Supply Chain Analytics - Introduction.
author: Karthik Chilamkurty
date: 2023-07-11 11:33:00 +0800
categories: [Analytics]
tags: [Supply Chain Management]
math: true
image:
  src: https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/ship1.jpeg
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

With huge amount of data generated from different parties of Supply Chain(ref: <https://karthikchilamkurthy.github.io/categories/scm/>), it is bedrock to modern supply chain to analyze manually.

Supply chain analytics allow companies to gain insights and extract value from large amount of data throughout various supply chain disciplines to increase efficiency, responsiveness. Supply chain analytics is an essential element of Supply Chain Management(SCM).

## **_Data Flow_**

let's take the example of a Shoe making Group that has stores all around the world,

Pro



## **_Contianer Optimization_**

Many Models have been developed in Supply Chain ecosystem, Large number of algorithms where found applying heuristics to Supply Chain Network Design, Inventory Management, Distribution etc.

Solving Real life Supply Chain Problems using Mathematical Decomposition were not found in this Feild, Cloud Computing is found to be appropriate tool for hosting data, Algorithms etc.

For optimizing any Supply Chain, There are many players that commonly make up to final decision such as predections, Recommendation.

Taking Example of NZ Container Recommendation, 

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/serviceflyermap.jpeg){: width="450" .normal}

- The Current Maritime Network between AUS and NZ remains Market centre for many industries for shipping their Goods.

- Dialy there are number of container Ships hop between these ports and parameters of this transportation paradigm are modeled using greedy algorithms to depict a monumental opportunity to rationalize costs, improve efficiency

- There are many Components arrive at various activites interlinking at a   same time.



#### **_Real World Scenario_** 

Considering Maritime Network between Australia and Newzeland, 

**_ShipSchedule_** is taken from orginization with Data Such as,

- **_Item_**: Item Requested for shipping.
- **_Source_**: Source Port.
- **_Destination_**: Destination Port.
- **_Orders_**: Number of Orders requested.
- **_Waitingtime_**: Number of days order is being requested.
- **_HoldingCosts_**: Cost incurred for holding the Order in Warehouse. 
- **_pallets_**: Number of pallets Available. 
- **_VesselType_**: Type of vessel that Material can fit.

**_Ship Information_** is taken from Shipping companies, 

- **_NumberOfVessels_**: Number of Vessels Available for shipping goods betweens AUS ports and NZ Ports.
- **_TypeOfVessels_**: Type of Vessel Available ex: Dry, Refrigerated etc.
- **_PortCongestionPeriod_**: Delay information in case of Disruptions, Congestions etc.


**_Customs Information_**, Priority shipping Goods etc information is taken from the Audit team (which are typically a outliers!).

The Model should Recommend the Priority of items that needs to be shipped over Network from one port to another.

Recommendation Should Optimize, (Please refer SCM Blogs for more understanding)

- **_Cost_**: Costs incured related to orders and their payments, storage of raw material or Products, Transportation, and waste.
- **_Inventory_**: Model should Optimize least quantity of inventory needed across the whole Supply Chain Network.
- **_Network_**: Model should be able to execute supply chain strategies at reduced cost and risk.


#### **_Solution_**

_Game theory_ studies interactive decision-making, where the outcome for each participant or Variable depends on the actions of other Variables.

In this Scenario, Game Theroy is A greedy algorithm adopts a solution path and interpretable Model, Can scale exponentially to arrive Optimal Model across various Interlinking activities.

## **_Game Theroy_**

From Game Theory, A proven methodology adopted for this Model and illustrates the incremental gains that are related to each participant in the Scenario. 

_Shapley value_ is a mono variate outcome in cooperative games, as postulated by Shapley S Lloyd way back-in 1953, is a method for assigning payouts to players depending on their contribution to the total payout. Players cooperate in a coalition and receive a certain profit from this cooperation

The “players” are the feature values of the Ship Data _Orders_, _Waitingtime_ etc . that collaborate to receive the gain (= predict Priority of item to sent).

Our Scenario, we evaluate the contribution of the _Orders_ feature value when it is added to a coalition of _WaitingPeriod_ and _HoldingCosts_. We simulate that only _WaitingPeriod_, _Orders_ and _HoldingCosts_ are in a coalition by randomly drawing another _Item_ from the data and using its value for the _pallets_ feature. The value 100 pallets was replaced by the randomly drawn 350 pallets. Then we predict the Priority of the _Item_ with this combination. In a second step, we remove _Orders_ from the coalition by replacing it with a random value of the _Volume_ feature from the randomly drawn _Item_(200). In the example it was 50M3, but it could have been _Orders_ again. We predict the _Item_ price for the coalition of _WaitingPeriod_ and _HoldingCosts_(100). The contribution of _Orders_ was 200-100 = 100. This estimate depends on the values of the randomly drawn _Item_ that served as a “donor” for the _Orders_ and _WaitingPeriod_ feature values. We will get better estimates if we repeat this sampling step and average the contributions.

_Shapley value_ is the average marginal contribution of a feature value across all possible coalitions, We repeat this computation for all possible coalitions, The Shapley value is the average of all the marginal contributions to all possible coalitions. The computation time increases exponentially with the number of features.

The Shapley value is defined via a value function _val_ of players in S.

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/sc1.png){: width="300" .normal}

where S is a subset of the features used in the model, x is the vector of feature values of the instance to be explained and p the number of features.

All possible coalitions (sets) of feature values have to be evaluated with and without the j-th feature to calculate the exact Shapley value

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/sc2.png){: width="250" .normal}

All these differences are averaged and result in:

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/sc3.png){: width="250" .normal}

Averaging implicitly weighs samples by the probability distribution of X.

The procedure has to be repeated for each of the features to get all Shapley values.

## **_Execution_**

For example, We have 2 contianers from AUS to NZ: One 20 foot, one 40 food Container. Our model needs to decide the priority of items needs to sendm keeping many players in Consideraion.

Following is the model:

![Desktop View](https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/gif-created.gif){: width="1000" .normal}



