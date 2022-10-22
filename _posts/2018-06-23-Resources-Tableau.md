---

firstPublishedAt: 1529784517706
latestPublishedAt: 1532106756890
slug: resources-for-creating-tableau-visualizations-through-python
title: Resources for creating Tableau Visualizations through Python
tag: Technical
---

I have not personally tried to create Tableau visualizations through Python, but there does exist a python library called **TabPy**.

This library is currently being developed by the Tableau team, and is under Beta/development.

> [**tableau/TabPy**](https://github.com/tableau/TabPy)
>
> <small>Execute Python code on the fly and display results in Tableau visualizations - tableau/TabPy</small>

![“Man wearing headphones at desk with window view of sunset in background” by [Simon Abrams](https://unsplash.com/@flysi3000?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral)](https://cdn-images-1.medium.com/max/8860/0*VTIRgg3CTQ_2Ysib)

# TabPy Documentation

1. [https://community.tableau.com/thread/236479](https://community.tableau.com/thread/236479)

2. [https://www.tableau.com/about/blog/2017/1/building-advanced-analytics-applications-tabpy-64916](https://www.tableau.com/about/blog/2017/1/building-advanced-analytics-applications-tabpy-64916)

3. `How to get Started` [https://github.com/tableau/TabPy/blob/master/client.md](https://github.com/tableau/TabPy/blob/master/client.md)

# Security Considerations

The following security issues should be kept in mind as you use TabPy with Tableau:

The data channel between Tableau and TabPy is currently not encrypted.

TabPy currently does not use authentication.

Python scripts can contain code which can harm security on the server where the TabPy is running. For example:

Access file system (read/write)

Install new Python packages which can contain binary code

Execute operating system commands

Open network connections to other servers and download files

# Unofficial Python and Tableau Library(ies)

1. [http://tableau.github.io/document-api-python/docs/](http://tableau.github.io/document-api-python/docs/)
