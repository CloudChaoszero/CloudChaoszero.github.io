---
permalink: /consulting/modern-analytics/notebooks-and-analyses
title: "Modern Analytics: Notebooks and Analyses"
description: "Understanding Notebooks and Analyses, and it's pros and cons"
author_profile: true
toc: true
read_time: true
header:
  teaser: https://www.ezlytix.com/wp-content/uploads/2020/09/The-Modern-Approach-To-Enterprise-Analytics-Self-Service-Tools-And-A-Culture-Of-Analytics.png
  og_image: https://www.ezlytix.com/wp-content/uploads/2020/09/The-Modern-Approach-To-Enterprise-Analytics-Self-Service-Tools-And-A-Culture-Of-Analytics.png
---


# Summary

The following is an analysis and comparison of different Data Notebook tools for exploratory data analysis and data science.

| Tool Feature    | Hex | Mode | PopSQL | ZEPL |   |   |   |   |   |
|-----------------|-----|------|--------|------|---|---|---|---|---|
| Visualizations  |     | x    |        |      |   |   |   |   |   |
| Versioning      | x   |      |        |      |   |   |   |   |   |
| Data & Analysis | x   |      |        |      |   |   |   |   |   |
| Engine          | x   |      |        |      |   |   |   |   |   |
| Notebooks       | x   |      |        |      |   |   |   |   |   |
| Collaboration   | x   |      |        |      |   |   |   |   |   |
| Reports         |     | x    |        |      |   |   |   |   |   |
| Security        | x   | x    | x      |      |   |   |   |   |   |
| Data Science    | x   |      |        |      |   |   |   |   |   |
| Search          |     |      | x      |      |   |   |   |   |   |

# Tools 

## PopSQL

## ZEPL

It's going to be deprecated in March 2023, so let's just skip this product.

## Hex

Hex is a notebook style application that lend themselves more to a data story and explorations, than a traditional dashboard. Though, there is still a possiblility for dashboarding, but is not typically used as such. Some usefule features are writebacks, snapshots, and Hex comments. It also allows for collaboration between analysts in the same notebook.

## Mode

Mode feels a lot more like a traditional BI tool, but with python added on top of it. Mode has a sleek and content management that feels more mature on the  front-end.

The definitions feature could also be really useful as kind of a prototype for transformation/business logic. However, it's as is--a traditional BI tool. A workflow is  isn't common, and so therefore requires a lot of jumping around to different interfaces to do sql, python, or other types of visualizations.

### Hex vs Mode

All-in-all, Mode feels like it caters (or at least offers) a bit more towards a slightly less-technical Business Intelligence end users for reporting. Whereas Hex focuses on the data & analysis experience. Mode has been around for quite a while and has a lot features that you'd find in some of the other BI tools like Tableau, Power BI, or even Looker.   

Thought their charting & overall visuals are super polished, the overall experience with Mode can feel a bit disjointed sometimes. Their notebook experience isn't great. The SQL query editor is super easy to use and save to collections for re-use throughout your organization. This kind of reusability wasn't really available in Hex until they recently launched their Components feature, which has been amazing for re-use throughout our organization.

With Mode, it feels like you're jumping around from place to place to build up reports and analyses, whereas with Hex, you live solely within the notebook you're working on, which is something I've come to greatly appreciate. 

The notebook experience with Hex is hands-down better, allowing you to combine SQL, Python, and even Jinja (e.g. dbt)! Hex also has some great built-in charting capabilities, though they do fall short in direct comparison to what Mode has to offer. 

That being said, the Hex charts are certainly "good enough" and they continue to make improvements to the experience. 
* And for instances where Hex may not support something, it's super easy to pull in any python plotting/charting package like plotly and matplotlib.

# My recommendation

If you are interested in a recommendation, [feel free to reach out/](https://www.linkedin.com/in/raulm8/).