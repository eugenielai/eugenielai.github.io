---
title: My Take on Causal Inference: Assessing Online Platform’s Policy Impact on Review Manipulation
layout: post
author: Eugenie Lai
date: 2020-04-12

---

# My Take on Causal Inference: Assessing Online Platform’s Policy Impact on Review Manipulation  
Date: 2020-04-12

Out of pure curiosity, I did a PhD-level business course this term on causal inference. This post is a light-hearted version of [my course project](/docs/work/policy.pdf), advised by [Dr. Arslan Aziz](https://www.sauder.ubc.ca/people/arslan-aziz). This work is my first exposure to research in social science and a preliminary application of causal inference techniques in online policy. Although comparing to research in CS, this experience felt very different for me, I appreciated the opportunity to explore a variety of topics and techniques in economics and learned that I am most motivated by the quatifiable impact of my work on a real-world problem.

## The Problem
Online retailing is one of the fastest-growing sectors in the past decade. However, studies have shown that unnatural reviews take up nearly a third of total online reviews, and review manipulation is shown to have substantial impacts on consumer’s buying decisions. Hence there is a growing need to monitor, assess, and control the quantity and impact of unnatural reviews on online platforms.

The three main types of unnatural reviews are negative reviews by competitors, positive reviews by producers, and incentivized reviews by customers. As a method of review manipulation, incentivized reviews are posted by consumers who received incentives from the product seller for the purchased product. Some common incentives include free products, product discounts, promotion coupons, and cash backs.

Historically, Amazon has prohibited compensation for reviews but allowed businesses to incentivize their customers to share their “honest” opinion as long as the reviewers disclosed their affiliation with the business in their review text. Although, in theory, these reviewers could write their unbiased opinion on the product, studies have shown that these incentivized reviews have tended to be overwhelmingly biased in favour of the product being rated. 

In an effort to keep bias out of the review process, *on October 6, 2016, Amazon announced to ban all incentivized reviews across the platform*, which provides a natural shock as an exogenous variation that only directly affects incentivized reviews. Here I aim to examine whether review policy bans can reduce review manipulation on online platforms by answering:  
* **Question:** Did the ban on incentivized reviews have an impact on review manipulation? Specifically, did the ban change the nature and number of incentivized reviews?
* **Hypothesis:** After the policy ban, there are more incentivized reviews. In addition, the characteristics of incentivized reviews also become more similar to natural reviews'.

I will be using a difference-in-difference approach with fixed effects to capture the impact of the policy ban on incentivized reviews.

## Data
[ReviewMeta](https://reviewmeta.com/) is an independent site that helps consumers get a better understanding of Amazon reviews. By affiliating with ReviewMeta, I collected a small dataset of reviews on two categories of top-selling products: *tablets* and *charging cables*. The dataset was collected based on lists of top-selling products in charging cables and tablets in September 2019. The dataset consists of reviews for Amazon and non-Amazon products six months before and after the policy ban. ReviewMeta labelled each review record either incentivized or non-incentivized based on the review text using their NLP methods.

![alt text][descriptive_reviews]

I analyzed the review sentiment using [Amazon Web Service (AWS) Comprehend](https://aws.amazon.com/comprehend/), which gives a sentiment score for positive, negative, neutral, and mixed sentiment for every review. I added the positive sentiment score to the dataset and used along with the rating as another measurement of reviews.  

## Methodology
The causal question is *whether Amazon's incentivized review ban had an impact on the nature and quantity of the incentivized reviews on Amazon*. 

### Model
Here I take a *difference-in-difference* approach: for each product category, I examine the difference in the nature of reviews across Amazon and non-Amazon products and across time periods before and after the policy ban. 
* **First difference:** Reviews for Amazon products are in the control group as Amazon itself would not incentivize its customers to post reviews. 
* **Second difference:** Reviews posted prior to the ban are in the control group.
* I used *fixed effects* to control the differences between product categories across the platform.
* I used a one-year time frame, including six months before and after the ban.

Furthermore, I need to check if the assumptions of using the difference-in-difference approach are satisfied. The pre-treatment parallel trend assumption is checked as the following.
* The interaction term of the weeks before the ban are tested.
* I created a dummy (i.e., 26 levels) for each week and then take the interaction of the non-Amazon dummy with this variable.
* The pre-treatment parallel assumption is satisfied if all the coefficients are statistically zero.

### Key Measures
![alt text][exploratory_analysis]

Using the stated incentivized review label identified by ReviewMeta's NLP methods, I found that review word count, image count, and helpfulness upvotes are sensitive to incentivized reviews: incentivized reviews are longer, with a higher image count, and more helpful than non-incentivized reviews. In addition, there is a strong correlation between reviews’ helpfulness and word count and image count. I validate this observation in the data using regression tests with fixed effects on product categories and brands and find that those characteristics are statistically significant for incentivized reviews, which is shown in the figure below. Along with review rating and sentiment, these five observables are the dependent variables in the difference-in-difference analysis.

![alt text][dv_brand]

## Results & Discussion

### Main Effects
The results align with the hypothesis. Based on the difference-in-difference analysis without fixed effects, there is a statistically significant decrease in review length, image count, and helpfulness for non-Amazon products after the ban. This means that after the ban, reviews became shorter, have fewer images, and are less helpful. Hence the policy ban had an impact on the nature of reviews. Notably, the coefficient of review rating and sentiment is positive but not significant. 

![alt text][did_avg]

In my difference-in-difference analysis with category-level fixed effects, besides the treatment effects being consistent for all dependent variables, review rating and sentiment also become statistically significant. The impact of the policy ban on incentivized reviews becomes more pronounced since I control the time-invariant characteristics of the product categories. In the previous analysis, I find that incentivized reviews inherently have higher ratings and sentiment. Therefore, the statistically significant increase in review rating and sentiment after the ban signals an increase in incentivized reviews. And instead of reducing the number of incentivized reviews on the platform, the policy ban led to more natural-looking incentivized reviews. 

![alt text][did_category_FE]

Lastly, the result of the difference-in-difference analysis with brand-level fixed effects is consistent with the previous findings. It is expected that I lose the statistical significance of the dependent variables as I further break down the data. 

![alt text][did_brand_FE]

The key findings are summarized as the following. First, the review policy ban changed the nature of reviews. Reviews become shorter with fewer images attached. Second, the policy ban increased review rating and sentiment across product categories. Third, the evidence shows that the ban may have heterogeneous effects on different product categories due to their individual characteristics.

### Robustness Check
![alt text][coef]

Following the steps described in the model section, the estimated coefficients of the 26 weeks prior to the policy ban are all statistically zero, which tells us that their trends are parallel before the ban.

## Conclusion

In summary, the results align with the hypothesis. After the ban, **the nature of reviews changed:** reviews became shorter with fewer images attached. However, there is an **increase** in both average review rating and sentiment, which indicates that the number of incentivized reviews increased after the ban for the top-selling phone cables and tablets.

Although this study only shows the possible repercussions of this particular online platform policy, 
* it openned my eyes on the complexity of policy impact evaluation, specifically the variety of confounders and unobservables.
* it showed me the potential of leveraging consumer-generated data in policy formulation.
* it made me have the urge to make data-driven policy formulation more accessible to benefit a wider range of governments and businesses.

[Back to blog](../blog.html)

[descriptive_reviews]: /assets/posts/descriptive_reviews.png "descriptive_reviews.png"
[exploratory_analysis]: /assets/posts/exploratory_analysis.png "exploratory_analysis.png"
[dv_brand]: /assets/posts/dv_brand.png "dv_brand.png"
[did_avg]: /assets/posts/did_avg.png "did_avg.png"
[did_category_FE]: /assets/posts/did_category_FE.png "did_category_FE.png"
[did_brand_FE]: /assets/posts/did_brand_FE.png "did_brand_FE.png"
[coef]: /assets/posts/coef.png "coef.png"

