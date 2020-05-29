---
title: Data-Driven City Planning: We Made a Visualizer for Surrey's Electric Vehicle Strategy
layout: post
author: Eugenie Lai
date: 2019-10-29

---

# Data-Driven City Planning: We Made a Visualizer for Surrey's Electric Vehicle Strategy  
Date: 2019-10-29

Last summer, I teamed up with [Laura](https://github.com/lauragreenstreet) and developed this visualization tool as a part of the [UBC Data Science for Social Good (DSSG) program](https://dsi.ubc.ca/data-science-social-good), directed by [Dr. Raymond Ng](https://www.cs.ubc.ca/~rng/). A collaboration between the [UBC Data Science Institute](https://dsi.ubc.ca/) and the [City of Surry](https://www.surrey.ca/), our project openned my eyes on the influential role of data in city planning and sustainability.

## Background & Motivation

Surrey is the second-largest city in the Metro Vancouver area with around 550,000 residents. By 2050, Surrey is projected to be the biggest city in the Metro Van area with over 800,000 residents. Hence the decisions made by the city of Surrey today will have a big impact as the city grows in the next 30 years.

![alt text][surry]{: height="80%" width="80%" style="display: block; margin: 0 auto"}

The city also aims to **grow sustainably**, with the goal to lower per capita emissions to half of the levels in 2007 by 2040. Transportation will play an important role in this change, as 50% of Surrey's greenhouse gas emissions come from transportation, compared to only 28% across Canada. Surrey only plans to decrease per-capita driving distance by 9%, resulting in **low-emission vehicles** playing an important role in reaching the city’s emission goals.

## The Problem

Motivated by these factors, the city of Surrey is currently developing an electric vehicle (EV) transformation strategy to support EV adoption, and the goal is to reach 100% zero-emission vehicles by 2050.

![alt text][chicken_n_egg]{: height="50%" width="50%" style="display: block; margin: 0 auto"}

However, there are a number of challenges:
1. EV adoption faces **a chicken-and-egg problem**: People wouldn’t get EVs unless there are chargers, but the private sector wouldn’t build chargers unless there is a market. Second, it’s unknown to what extent the city should fund EV development until the private sector takes over.
2. Adopters are constrainted by the **high cost** of EVs.
3. There is a **lack of public awareness**.

![alt text][goal_vs_now]{: height="60%" width="60%" style="display: block; margin: 0 auto"}

There is also a big gap between the current state and the goal. 
* **Low EV adoption:** From the 2018 ICBC registration dataset, EV only takes up less than 1% of the total passenger vehicles in Surrey. 
* **Inadequate EV infrastructure:** There are only 70 public charging sites in and within a 5km radius of Surrey, representing around 180 chargers. 

![alt text][charging_sites]{: height="60%" width="60%" style="display: block; margin: 0 auto"}

Therefor, the EV transformation strategy is much needed.

The purpose of this project is to help Surry adopt EV faster by giving statistical insights to guide the EV strategy development. Specifically, the city wants to know how to strategically implement EV infrastructure in Surrey. Our **goal** was to help the city use their data to choose 20 sites for curbside chargers for a national funding proposal.

## Visualization Tool

Our visualizer aims to help the city planners explore 
* the spatial distribution of their vehicel stock and traffic flows.
* the categorical distribution.
* the time trends.

![alt text][app_vehcle_stock]

For example, on the vehicle stock tab, 
* the map on the left is showing the number of EVs per area in 2018.
* the plots on the right show the statistics specific to a selected area, Fraser Heights: 
    * the line graph on the top right shows the yearly changes of vehicle counts by class.
    * the bar chart on the bottom right shows the vehicle composition compared to the city average.

However, maps could be prone to subjectivity. For example, choosing different colour scales for a heat map can minimize or exaggerate the differences in EV density among areas. To mitigate subjectivity, we enabled the tool to visualize the data on several scales to give the user several perspectives. For example, on the vehicle stock tab, users are able to see where EVs are located in each area by either count or proportion. By count, Cloverdale Industrial does not even show up in the top quantile, while by proportion, it becomes an outlier with 4% EVs compared to 2% in the area with the next largest percentage. The tool also allows the user to zoom in and out between the Traffic Analysis Zone (TAZ) and area level for different spatial resolutions.

[Back to blog](../blog.html)

[surry]: /assets/posts/dssg/surry.png "surry.png"
[goal_vs_now]: /assets/posts/dssg/goal_vs_now.png "goal_vs_now.png"
[charging_sites]: /assets/posts/dssg/charging_sites.png "charging_sites.png"
[chicken_n_egg]: /assets/posts/dssg/chicken_n_egg.png "chicken_n_egg.png"
[app_vehcle_stock]: /assets/posts/dssg/app_vehcle_stock.png "app_vehcle_stock.png"
