---
firstPublishedAt: 2020-03-01
title: SQL Readability and your Team (2020)
tag: Coding
author_profile: true 
toc: true
---


You're writing an advanced and sophisticated contribution, and ready to push the Pull Request (PR) to production

![Far Out](https://media2.giphy.com/media/FV8YUdZ88fNLi/source.gif)

**but then a code reviewer does not approve your query.**

Your query works, so what's the matter? 

It may turn out that you're writing style may not be up to par with team's query standards--and that's not your fault,something you should not be ashamed about.


# What is Readability?

Readability is the style, standarization, and practice of producing readable code. Similar to writing, it's like correcting for punctuation.

The enforcement of readability practices, typically by teams, are tied to code reviewing between peers to push code to production.

## Why should I encourage readability best practices for my team?

In the hook to the introduction, I want to emphasize that coding practices enforce general team contributions and standards to better alignment readability, abstract readability to focus more on core logic, and minimize errors

# Why am I writing about this?

I contracted with a top 10 tech company in 2018, and I was learning so much from an engineering team, as an onboarding analyst with them. 

I submitted PR's (Change Lists[CL]) to the code production, and I learned the impact of readability for teams, and the long-term benefits from it.

> I had some idea of readability before joining the company, but holy cow I didn't know it's true value until working their. I learned readability for SQL, some Javascript and Python, but never had the chance to get approved/certified. :/

Now that I have been away with that company for some time, and onboarded with another great company, Autodesk, I wanted to teach others about the impact of

<b><center>SQL Readability</center></b>

![Reading Vision](https://thumbs.gfycat.com/SandyHelpfulAmazondolphin-max-1mb.gif)


# SQL Readability

Let's say we want to have the total amount of logins for the past 7 days of [Myspace](https://en.wikipedia.org/wiki/Myspace) data per user, and some attributes along with that.

We create a workable query using [ASCII SQL syntax](https://docs.snowflake.com/en/sql-reference/functions/ascii.html).


```sql
select 

id, createdDate, login.login_id, geoState, firstName, lastName, sum(login.logIn) total_logins

from mySpace_events as events
LEFT JOIN mySpace_users users
on users.id = events.user_id
WHERE login.date >= login.date - CURRENT_DATE

group by 1,2,3,4,5,6
```


## Reserve Words

## Spacing

## Subqueries and WITH statements

## Aliases

## 80 Characters

# Resources

1. [Vicki Boykis' take on readable SQL](http://veekaybee.github.io/2015/06/02/good-sql/)

2. [SQL Style Guide](https://www.sqlstyle.guide/)

3. [Craig Kersteins' take on Legible SQL](http://www.craigkerstiens.com/2016/01/08/writing-better-sql/)

4. Unofficial: Past experience on SQL Readability at a top 10 tech company