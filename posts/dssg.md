---
title: Data Science for Social Good: Data Visualizer for Surrey's Electric Vehicle Strategy
layout: post
author: Eugenie Lai
date: 2019-10-29

---

# Data Science for Social Good: Data Visualizer for Surrey's Electric Vehicle Strategy  
Date: 2019-10-29

This visualization tool is developed as a part of UBC Data Science for Social Good (DSSG) program, which is a collaboration between the UBC data science institute and the city of Surry.

## Background & Motivation

Surrey is the second-largest city in the Metro Vancouver area with around 550,000 residents. By 2050, Surrey is projected to be the biggest city in the Metro Van area with over 800,000 residents. Therefore, the decisions made by the city of Surrey today will have a big impact as the city grows in the next 30 years.

![alt text][surry]

The city also aims to grow sustainably, with the goal to lower per capita emissions to half of the levels in 2007 by 2040. Transportation will play an important role in this change, as 50% of Surrey's greenhouse gas emissions come from transportation, compared to only 28% across Canada. Surrey only plans to decrease per-capita driving distance by 9%, resulting in low-emission vehicles playing an important role in reaching the city’s emission goals.

## The Problem

Motivated by these factors, the city of Surrey is currently developing an EV transformation strategy to support EV adoption, and the goal is to reach 100% zero-emission vehicles by 2050.

![alt text][chicken_n_egg]

However, there are a number of challenges. First, EV adoption faces a chicken-and-egg problem. People wouldn’t get EVs unless there are chargers, but the private sector wouldn’t build chargers unless there is a market. Second, it’s unknown to what extent the city should fund EV development until the private sector takes over.

On top of that, there are other concerns regarding the high cost of EVs, public awareness, etc.

![alt text][goal_vs_now]

There is also a big gap between the current state and the goal. From the 2018 ICBC registration dataset, EV only takes up less than 1% of the total passenger vehicles in Surrey. In addition, there are only 70 public charging sites in and within a 5km radius of Surrey, representing around 180 chargers.

![alt text][charging_sites]

Therefore, the EV transformation strategy is much needed.

That being said, the purpose of this project is to help Surry adopt EV faster by giving statistical insights to guide the EV strategy development. To be more specific, the city wants to know how to strategically implement EV infrastructure in Surrey. Unlike private businesses, the city can invest in infrastructure in underserved areas that might not have an immediate payoff. Our goal was to help the city choose 20 sites for curbside chargers for a national funding proposal.

[surry]: /assets/posts/dssg/surry.png "surry.png"
[goal_vs_now]: /assets/posts/dssg/goal_vs_now.png "goal_vs_now.png"
[charging_sites]: /assets/posts/dssg/charging_sites.png "charging_sites.png"
[chicken_n_egg]: /assets/posts/dssg/chicken_n_egg.png "chicken_n_egg.png"
