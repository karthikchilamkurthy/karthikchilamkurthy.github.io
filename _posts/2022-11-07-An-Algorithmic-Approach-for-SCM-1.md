---
title:  An Algorithmic Approach for Supply Chain Optimization - Container Recommendation Using Game Theory.
author: Karthik Chilamkurty
date: 2022-11-07 11:33:00 +0800
categories: [SCM,Forecasting,Statistics]
tags: [SCM]
math: true
image:
  src: https://cdn.jsdelivr.net/gh/karthikchilamkurthy/Machine_learning@main/Data%20Sources/images/ship1.jpeg
---

## **_About_**

I've Been Working as a Strategist Engineer in Digitalising Logistics of a Food Chain Industry, We try to drew Parametres of Supply chain Process and derive the holistic approch to improve Efficiency and Optimize costs.

## **_Abstract_**

Container Freight is a Ecosystem that organize the external suppliers, distributors, vessel management, disruptions, Port Management etc,.

There is always a need of scalable greedy algorithm for optimizing Supply Chain Design, Planning and Execution.

There are Number of Components that collate to derive Supply Chain Optimization Model.

Collaborative game theoretic approach ie., Shapley Value is used for Supply Chain Design and Planning.

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



