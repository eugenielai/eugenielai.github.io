---
title: My Take on Causal Inference: Assessing Online Platform’s Policy Impact on Review Manipulation
layout: post
author: Eugenie Lai
date: 2020-04-12

---

# My Take on Causal Inference: Assessing Online Platform’s Policy Impact on Review Manipulation  
Date: 2020-04-12

Out of pure curiosity, I did a PhD-level business course this term on causal inference. This post is a light-hearted version of [my course project](/docs/work/policy.pdf), advised by [Dr. Arslan Aziz](https://www.sauder.ubc.ca/people/arslan-aziz). This is my first exposure to research in social science. Although everything felt very different, I learned that I get motivated by the quatifiable impact of my work on a real-world problem.

## The Problem
Online retailing is one of the fastest-growing sectors in the past decade. However, studies have shown that unnatural reviews take up nearly a third of total online reviews, and review manipulation is shown to have substantial impacts on consumer’s buying decisions. Hence there is a growing need to monitor, assess, and control the quantity and impact of unnatural reviews on online platforms.

The three main types of unnatural reviews are negative reviews by competitors, positive reviews by producers, and incentivized reviews by customers. As a method of review manipulation, incentivized reviews are posted by consumers who received incentives from the product seller for the purchased product. Some common incentives include free products, product discounts, promotion coupons, and cash backs.

Historically, Amazon has prohibited compensation for reviews but allowed businesses to incentivize their customers to share their “honest” opinion as long as the reviewers disclosed their affiliation with the business in their review text. Although, in theory, these reviewers could write their unbiased opinion on the product, studies have shown that these incentivized reviews have tended to be overwhelmingly biased in favour of the product being rated. 

In an effort to keep bias out of the review process, on October 6, 2016, Amazon announced to ban all incentivized reviews across the platform, which provides a natural shock as an exogenous variation that only directly affects incentivized reviews. Here I aim to examine whether review policy bans can reduce review manipulation on online platforms by answering:  
* **Question:** Did the ban on incentivized reviews have an impact on review manipulation? Specifically, did the ban change the nature and number of incentivized reviews?
* **Hypothesis:** After the policy ban, there are more incentivized reviews. In addition, the characteristics of incentivized reviews also become more similar to natural reviews'.

I will be using a difference-in-difference approach with fixed effects to capture the impact of the policy ban on incentivized reviews.

## Data
[ReviewMeta](https://reviewmeta.com/) is an independent site that helps consumers get a better understanding of Amazon reviews. By affiliating with ReviewMeta, I collected a small dataset of reviews on 2 categories of top-selling products: tablets and charging cables. The dataset was collected based on lists of top-selling products in charging cables and tablets in September 2019. The dataset consists of reviews for Amazon and non-Amazon products six months before and after the policy ban. ReviewMeta labelled each review record either incentivized or non-incentivized based on the review text using their NLP methods.  
![alt text][descriptive_reviews]

I analyzed the review sentiment using [Amazon Web Service (AWS) Comprehend](https://aws.amazon.com/comprehend/), which gives a sentiment score for positive, negative, neutral, and mixed sentiment for every review. I added the positive sentiment score to the dataset and used along with the rating as another measurement of reviews.  

## Methodology
The causal question is *whether Amazon's incentivized review ban had an impact on the nature and quantity of the incentivized reviews on Amazon*. 

### Models
Here I take a difference-in-difference approach: for each product category, I examine the difference in the nature of reviews across Amazon and non-Amazon products and across time periods before and after the policy ban. 
* The first difference: Reviews for Amazon products are in the control group as Amazon itself would not incentivize its customers to post reviews. 
* The second difference: Reviews posted prior to the ban are in the control group.
* I used a one-year time frame, including six months before and after the ban.
* I used fixed effects to control the differences between product categories across the platform.

Furthermore, I need to check if the assumptions of using the difference-in-difference approach are satisfied. The pre-treatment parallel trend assumption is checked as the following.
* The interaction term of the weeks before the ban are tested.
* I created a dummy (i.e., 26 levels) for each week and then take the interaction of the non-Amazon dummy with this variable.
* The pre-treatment parallel assumption is satisfied if all the coefficients are statistically zero.

### Key Measures
![alt text][exploratory_analysis]

## Results & Discussion

## Conclusion

[Back to blog](../blog.html)

[descriptive_reviews]: /assets/posts/descriptive_reviews.PNG "descriptive_reviews.png"
[exploratory_analysis]: /assets/posts/exploratory_analysis.PNG "exploratory_analysis.png"
