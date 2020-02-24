---

firstPublishedAt: 2020-01-30
title: SaaS Metrics

tag: Project Management
---


This document is a review and breakdown of Metrics Definitions and formulas related to SaaS Metrics, particulary 16 SaaS Metrics critical for business growth

## Breaking Down Profit

Profit = Revenue - Cost

Where:
1. Revenue = Paying Users x amount paid by userrevenue is equal to 
2. Paying Users = New Users + Repeated Paying Users
3. New Users = Trial Users * Conversion Rate
4. Repeated Paying Users = Previous Paying Users x (1-Churn Rate)
5. Trial Users = (SEO Visitors + SEM Visitors + Viral Visitors)Trial Conversion Rate

> Note: Churn rate has a nonlinear improvement in revenue over time

## Metric Definitions and Formulas

### 1. Net MRR Growth Rate

Month over Month % increase in net MRR is an important metric

> Note: If a company is not able to reach a sustainable ratio of 3.5-4x or more than lost MRR, bussiness is not sustainable - Alexander Bruehl, Angel Investor

#### 1.1 Calculation

**Net MRR**

Net MRR = Existing MRR (\$) + New Business (\$) + Reactivation (\$) + Expansion (\$) - (Churn (\$) + Contractural (\$)) 

**Net MRR Growth Rate**

$\tfrac{\text{Net MRR Growth Rate Month B}-\text{Net MRR Growth Rate Month q}}{\text{Net MRR Growth Rate Month A}}$

### 2. Growth MRR Churn Rate

The measured % of MRR Churn Rate. That is, Percent of revenue lost due to cancellation or downgrades. It estimates the company, in contrast to Net MRR Churn Rate that calculates relative loss for company

#### 2.1 Calculation

$\tfrac{\text{Total MRR Churn this month}}{\text{Total MRR at the Start of this Month}}$ x 100

### 3. Expansion MRR Rate

### 4. Average Revenue Per Account (ARPA)

#### 4.1 Calculation

$\tfrac{\text{Total Monthly Recurring Revenue}}{\text{Total Number of Accounts}}$

### 5. LTV:CAC Ratio

Average Lifetime value of your customer is the average monthly revenue per adjusted for monthly churn and gross margin

#### 5.1 Calculation

$\tfrac{LTC}{CAC}$

### 6. Lifetime Value (LTV)
Average revenue a single customer is predicted to generate for an assumed duration of their account

Average Monthly Revenue per Customer X Number of Months for customer = $\tfrac{\text{Average Monthly Revenue Per Customer}}{\text{Monthly Churn}}$

### 7. Customer Acquisition Cost (CAC)

#### 7.1 Calculation

$\tfrac{\text{Total Sales and Marketing Expense}}{\text{Number of New Customers acquired}}$

Average expense of gaining a single customer

### 8. CAC Payback Period

CAC Payback Period is the number of months it takes to earn back money in acquiring customers.

$\tfrac{CAC}{\text{ARPA x Gross Margin (%)}}$

> Note: Two rules about CAC--LTV should be 3x of CaC and Recover CAC <12 months....else business would require too mich capital in future

### 9. Monthly Active Users (MAU)

Number of unique individuals visiting website each month

### 10. Qualified Lead Velocity Rate (LVR)

LVR is a great indicator of future sales attainment

$LVR = \tfrac{\text{Qualified Leads Current Month}-\text{Qualified Leads Previous Month}}{\text{Qualified Leads Previous Month}}$ x 100

### 11. Product Qualified Lead (PQL)

Potential Customers who have used product and reach pre-defined trigger to likely become paying customer

### Organic vs Paid Traffice Rate

### Viral Coefficient

Viral Coefficient = Invites X Conversion Percent

where invites is the number of invites a user sends

### Conversion Rate to Customer

Coversion Rate to Customer = $\tfrac{\text{Number of PQLs}}{\text{Total Number of New Cusotmers during same time period}}$

### Stickiness Ratio

$\tfrac{DAU}{MAU}$

### Net Promoter Score (NPS)

Metric used to gauge customer satisfaction and loyalty to your offering

#### Calculation

NPS = % of Promoters - % of detractors, where

* % of promoters = number of respondents who ranked 9 or 10 divided by total number of respondents

* % of detractors, number or respondents who ranked $\leq 6$, divided by total number of respondents


## Tips

### Lean Product Analytics Cycle
1. Identify your metrics
2. Measure Metrics Baseline Values
3. Evaluate Metrics Upside Potential
4. Select Top Metric

    a. Iterate
    

*   If your product feature is being released, for testing, please have a **counterfactual**  to really gage wether product feature launch provided significant improvement in product 

    a. (i.e. with product feature launch, have control and treatment groups)

## Notes

* What is Product Analytics?
    * Pull Data from SQL database
    * BI Tool for visualization
    * Pageview Analytics
    * Behavioral Analytics
    
* Distinguish between Bookings and Revenue

* Upsell vs cross sell

* KPIs

    * Reasonable number of KPIs between 3 and 7 (5 $\pm$ 2)
        * More KPIs create distractions as opposed to focus (for a team)
        
        * Warren Buffet: Write down top 25 goals. Then, choose top 5 goals. Focus on those, and ignore other 20 until you achieved first 5.
        
    * Quantifiable piece of objectives and goals
    
    * Needs 4 attributes: 
    
        * Measure
        
        * Target
        
        * Source
        
        * Frequency
    
    * Having Raw #'s, Progress, and Change % is important
    
    * Leading and Lagging Indicator
        
        * Lagging (occurred/outcome)
            
            * Example; Margin, profit, revenue--results
            
            * Note: Can't control lag, because we experienced it
        
        * Leading (soon to-be occuring) 
            
            *  Example: Number of contacts, actions, marketing
        
            *  Note: It's predictable and influential for future business results

## Resources
[How to improve your product analytics](https://www.youtube.com/watch?v=dwL97n06HFs)

[Lean Product Playbook](https://www.youtube.com/watch?v=Bb8DfkBSL_A)

[Negative Churn](http://tomtunguz.com/negative-churn/?_ga=2.19068216.1033635996.1542876886-1344136856.1541905224)

[Examples of Net MRR Churn Rate](https://www.geckoboard.com/learn/kpi-examples/saas-kpis/net-mrr-churn-rate/)

[Moving Average](https://blogs.sas.com/content/iml/2016/01/25/moving-average.html)

[SaaS Metrics Companies should track](https://databox.com/metrics-every-saas-company-should-track)

[Optional Video: AirBnB Product Insights](https://www.youtube.com/watch?v=EPji2e2XwDk)

[16 More SaaS Metrics](https://a16z.com/2015/09/23/16-more-metrics/)

Product Enagement: the most important metric you aren't tracking for your SaaS business

* General QUestions for manager about metrics
    * Are you, as a manager, tired of trying to gauge how your accounts performing or engagement this month is? 
    * As a customer success manager, do you want an easier want to get a gauge of user adoption and usabuluty wuthout having to check emails or communicate with teams about calls or check-ins?
    * As an AE, how many times did you wish you could see those deeper in funnel of prospect would be a converted customer?

* 4 steps to creating engagement score for your SaaS product
    * Define Activity or Engagement for Product
        * Event Tracking
            * tasks completed
            * team members added
            * comments left
            * team members added
            * projects completed
        * Start tracking product events/activities
            * Segmentation and analytics
                * User Engagement Score
                * NPS Score analytics
        * Advanced Analytics
            * Normalizing Engagement Scores
        * Apply Scores to make them actionable
* Rank Users
    * Discover Power Users
    * Prioritize Customer success efforts through driving solutions and growth for customers
    * Identify business strategy implementations for customers

*  Score and Rank Accounts
    * Understand engagement metrics in aggregation at account level, and other available levels thereafter
    * Understand health of biz
    * Prioritize CS efforts by focusing on accounts that are ripe for expansion or upgrade
*  Calculate overall score for product
* Compare populations or cohorts
* Correlate with other business metrics and teams

Evaluation for adoption and engagement with other business metrics (e.g. Sales, Retention, Churn, LTV, etc.) then more quality in CS improves over time

> Test and Learn



```python

```
