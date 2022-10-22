---
title: "How to become a dbt Certified Developer"
tag: Technical
author_profile: true
toc: true
header:
  teaser: https://miro.medium.com/max/1272/0*2JgVQB9iEB1cvp0Y.
  og_image: https://miro.medium.com/max/1272/0*2JgVQB9iEB1cvp0Y.
---

# Summary


The dbt (data build tool) Certification let's you show you're a reliable source for Analytics Engineering industry's development for (Operational) Analytics.

I would recommend [Paul Fry's article "Preparing for the dbt 'Analytics Engineering' Certification"](https://medium.com/geekculture/preparing-for-the-dbt-analytics-engineering-certification-5496c3ec6e15) as an introduction to what the dbt Certified Developer Certification is and resources.

This article will cover additional material & tips that would be helpful for folks, like myself
* About me: I have 2+years of dbt experience, 3+ years of Python development for Analytics and reporting. I am currently a Sr. Data Analyst @ Autodesk.


# The Exam

![Testing](https://tenor.com/view/test-gif-20712302)

## The Scenario

![Scenario by Tribe called Quest w/Busta Rhymes](https://miro.medium.com/max/1272/0*2JgVQB9iEB1cvp0Y.)

### What would you do?

These questions are geared towards experienced model & development. Moreover, the question range from starting a dbt project to developing & testing (i.e Building) your first model. 

I would say this exam is more geared towards the following folks: 
* 3-6months of startup or full dbt project build
* 6+months in dbt experience

If you are a newcomer to the space, I recommend developing a dbt project using your preffered Database & BI tool. You can find trials for such tools on their available website.
* NOTE: If you work with a company, even better! Try out local dbt development!

My (personal) recommended tools w/free trials are the following:
* Database - [Snowflake](https://signup.snowflake.com/)
* BI - [Mode Analytics](https://mode.com/)
* BI - [Preset](https://preset.io/)

You can see how I developed a dbt project, in my past (personal) training course [Analytic Engineering & dbt: 0-100](https://raulingaverage.dev/onboarding-2-dbt/)


### You can be technically correct in one sense, but wrong in the question's scenario

There are certain pieces of terminology you have to certainly know. The scenario for each question sets you up to solve a problem in the context of one part of the Analytic Engineering practice, but proposed answers can be part of another part.

Example:

Imagine you are configuring a YAML file called `src_sfdc.yml`. The question you get calls for identifying a test configuration. You have 4 multiple choice questions. Two of them say "model" in their explanation, and sound right. REMEMBER, this is about a **Source, not a model**.


## Mitigating Non-dbt Exam issues

Learning about Discrete Option Multiple Choice (DOMC) questions...before you find out the hard way.

I didn't look into DOMC-style questions. When I first saw one, I was a bit confused on what to do. Moreover, what the interpretation of a Yes/No question meant. As a consequence, I wasted 1min-2min deciphering what to do. That time could have been ~1.8mins on re-evaluating another question (120mins / 65 Q's).

As a summary:

> "DOMC represents a relatively simple but very useful change in the delivery of multiple choice question. Instead of showing all of the options at one time, as is usually done, options are randomly presented one at a time. For each presented option, the test taker chooses YES or NO indicating whether the he or she thinks it is the correct one." - [source](https://domc.caveon.com/about)

I should also note that DOMC-style questions are not necessarily 2+ Yes/No path questions. They could be 1 Yes/No or 3 Yes/No path questions.

## Types of Questions

* Developing dbt models
* Debugging data modelling errors
* Monitoring data pipelines
* Implementing dbt tests
* Deploying dbt jobs
* Creating and maintaining dbt documentation
* Promoting code through version control
* Establishing environments in a data warehouse for dbt

### Questions can vary

After I passed the exam at Coalesce'22, I was headed back to the main conference floor. Approaching the staircase, I found someone else that passed the exam. 
* Note: You can tell because they we got special swag for being one of the many few becoming dbt Certified Developers

We got to talking, and he mentioned some of the Snapshot-related scenario questions he had. I told him "WHAT Snapshot questions?" I got 3+ Incremental materialization questions, but I didn't get any Snapshot questions...

Another theory to the test is that questions can vary on what is served up on the test. 

This makes sense because the person who developed the Exam provides high standard exams that minimize cheating, compared to other tool/software certifications.

![Thinking](https://tenor.com/view/pooh-think-winnie-the-pooh-gif-14107893)


Hope you enjoyed this article, and good luck on your upcoming exam!

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Last day at <a href="https://twitter.com/hashtag/dbtCoalesce?src=hash&amp;ref_src=twsrc%5Etfw">#dbtCoalesce</a> 😭♥️<br><br>Became a dbt Certified Developer &amp; had some fun! <a href="https://t.co/iMnVkSptXy">pic.twitter.com/iMnVkSptXy</a></p>&mdash; ℝaul ∈ 🥑 (YIMBY) 🚲 ❤ (@RaulingAverage) <a href="https://twitter.com/RaulingAverage/status/1583279335750107136?ref_src=twsrc%5Etfw">October 21, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## Resources

* [dbt Analytics Engineering Certification Exam Study Guide](https://www.getdbt.com/assets/uploads/dbt_certificate_study_guide.pdf)

* dbt Fundamentals
    * [Advanced Materialization](https://courses.getdbt.com/courses/advanced-materializations)
        * Mainly focus on Snapshot & Incremental Materialization methods
    * [Jinja & Macro Statements](https://courses.getdbt.com/courses/jinja-macros-packages)


* Coalesce NOLA '22
    * [Advanced Materialization](https://attendees.bizzabo.com/396530/agenda/activity/967466)
    * [Advanced Testing](https://attendees.bizzabo.com/396530/agenda/activity/967474)