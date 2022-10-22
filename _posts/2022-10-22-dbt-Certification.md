---
title: "How to become a dbt Certified Developer"
tag: Technical
author_profile: true
toc: true
header:
  teaser: https://yimbyaction.org/2021/wp-content/uploads/sites/5/2021/08/image_from_ios-6-scaled-e1628888786710-1536x1155.jpg
  og_image: https://yimbyaction.org/2021/wp-content/uploads/sites/5/2021/08/image_from_ios-6-scaled-e1628888786710-1536x1155.jpg
---

# Summary


The dbt (data build tool) Certification let's you show you're a reliable source for Analytics Engineering industry's development for (Operational) Analytics.

I would recommend [Paul Fry's article "Preparing for the dbt 'Analytics Engineering' Certification"](https://medium.com/geekculture/preparing-for-the-dbt-analytics-engineering-certification-5496c3ec6e15) as an introduction to what the dbt Certified Developer Certification is and resources.

This article will cover additional material & tips that would be helpful for folks, like myself
* About me: I have 2+years of dbt experience, 3+ years of Python development for Analytics and reporting. I am currently a Sr. Data Analyst @ Autodesk.

# The Exam

## The Scenario

### What would you do?

These questions are geared towards experienced model & development. Moreover, the question range from starting a dbt project to developing & testing (i.e Building) your first model. 

I would say this exam is more geared towards the following folks: 
* 3-6months of startup or full dbt project build
* 6+months in dbt experience

If you are a newcomer to the space, I recommend developing a dbt project using your preffered Database & BI tool. You can find trials for such tools on their available website.

My (personal) recommended tools w/free trials are the following:
* Snowflake`
* Mode Analytics
* Superset

You can see how I developed a dbt project, in my past (personal) training course [Analytic Engineering & dbt: 0-100](https://raulingaverage.dev/onboarding-2-dbt/)

### You can be technically correct in one sense, but wrong in the question's scenario

Imagine you are configuring a YAML file called `src_sfdc.yml`. The question you get calls for identifying a test configuration. You have 4 multiple choice questions. Two of them say "model" in their explanation, and sound right. REMEMBER, this is about a **Source, not a model**.



## Mitigating Non-dbt Exam issues

Learning about Discrete Option Multiple Choice (DOMC) questions...before you find out the hard way.

I didn't look into DOMC-style questions. When I first saw one, I was a bit confused on what to do. Moreover, what the interpretation of a Yes/No question meant. As a consequence, I wasted 1min-2min deciphering what to do. That time could have been ~1.8mins on re-evaluating another question (120mins / 65Q's).

As a summary:

> "DOMC represents a relatively simple but very useful change in the delivery of multiple choice question. Instead of showing all of the options at one time, as is usually done, options are randomly presented one at a time. For each presented option, the test taker chooses YES or NO indicating whether the he or she thinks it is the correct one." - [source](https://domc.caveon.com/about)

I should also note that DOMC-style questions are not necessarily 2+ Yes/No path questions. They could be 1 Yes/No or 3 Yes/No path questions.

## Types of Questions

Someone after the exam told me they had 2 Snapshot questions. However, I have none of those, and 3+ Incremental questions

* YAML file configurations

## Resources

* [dbt Analytics Engineering Certification Exam Study Guide](https://www.getdbt.com/assets/uploads/dbt_certificate_study_guide.pdf)

* dbt Fundamentals
    * Advanced Materialization
    * Jinja & Macro Statements
    * 

* Coalesce NOLA '22
    * Advanced Materialization
    * Advanced Testing
    * 