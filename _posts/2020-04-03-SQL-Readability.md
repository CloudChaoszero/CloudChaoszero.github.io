---
firstPublishedAt: 2020-04-03
title: SQL Readability and your Team (2020)
tag: Coding
author_profile: true 
toc: true
mathjax: true
header:
  teaser: /assets/images/sql-query-worked.jpg
  og_image: /assets/images/sql-query-worked.jpg
---

Scenario: You're going to submit a Pull Request (PR) for an advanced and sophisticated contribution to production, that you spent hours on.

**Kudos to you!** 

![Far Out--Hackers](https://media2.giphy.com/media/FV8YUdZ88fNLi/source.gif)

**But then a code reviewer does not approve your PR.**

![Crying--10 Things I hate about you](https://media1.giphy.com/media/6tSHBDVDyOF3O/source.gif)

Your query works, so what happened? 

It may turn out that you're writing style may not be up-to-par with the team's standards.

And that's not your fault! It's something you should not be ashamed about, but understanding about.

But why? First...

# What is Readability?

Readability is the style, standarization, and practice for "readable" code. An analogy, it's like correcting for punctuation in a writing practice.

The enforcement of readability practices, typically by teams, are tied to code reviewing between peers to push code to production.

## Why should I encourage readability best practices?

From the introduction, I emphasized that coding practices are enforced by teams in agreement for better practices, standards, and alignment to contribute value to a product or organization. But what's in it for the team? What's in it for you

Let's look at a scenario.

### A Scenario

When a developer initially writes the code their knowledge of the system is very detailed and complex. And in this writing, they've spent a substantial amount of time to know every logical condition or output from the results--well hopefully.

1 year later, another person decides to change this code due to updated business logic needed w.r.t to the code. However, that past developer's work was written poorly. 


Recall the logic being complex? Well, this developer added another layer of complexity as well, which can actually disastisfy the current developer on fixing the code.

![Sleepy](https://i.pinimg.com/originals/17/7e/29/177e297fa5b9b5e5c889ef0b7da3abe3.gif)

This new developer may experence:
* Difficult to understand logic and ouuts
* Longer to debug
* Maintenance issues
* The complexity of reading code

With readabilit practices, we alleviate the complexity of reading the code for the developer. 

This can enable:
* Increased Productivity 
* More time to focus on the core logic.
* Quicker turnover of implementations

<b><center>That seems like it's worth it, right?</b></center>

![](https://media.giphy.com/media/69jvP3VXUYhr3YUYu9/giphy.gif)

# Why am I writing about this?

Being an upcoming analyst, I didn't mind code readability along with the content I produced.

However, one job I submitted SQL, Python, and Javascript PR's (Change Lists[CL]) to code production, and I learned the impact of readability for teams, and the long-term benefits from it.

Being with Autodesk, I wanted to drive impact to both colleagues and individuals that should be encouraged to enforce these same practices, as we evolve in analytics and (soft) engineering.

Now,
<b><center>SQL Readability</center></b>

![Reading Vision](https://thumbs.gfycat.com/SandyHelpfulAmazondolphin-max-1mb.gif)


# SQL Readability

## The Scenario

Let's say we want to have the total amount of logins for the past 7 days of [Myspace](https://en.wikipedia.org/wiki/Myspace) data per user, and some attributes along with that.

We create a workable query using [ASCII SQL syntax](https://docs.snowflake.com/en/sql-reference/functions/ascii.html).



```sql
select 

id, createdDate, events.login_id, geoState, firstName, lastName, sum(login.logIn) total_logins

from mySpace_events as events
LEFT OUTER JOIN mySpace_users users
on users.id = events.user_id
WHERE login.date >= current_date - (select min(createdDate) from mySpace_users where profile  = 'Musician')
group by 1,2,3,4,5,6
```


## Statement Syntax

1. `Upper case` declarative statements withing your SQL queries. This allows for another dimension to mentally filter out non-essential information when going to your main target--the logic.

2. Have the statements be on `Seperate Lines` 

3. Ensure particular words are [reserved](https://docs.microsoft.com/en-us/sql/t-sql/language-elements/reserved-keywords-transact-sql?view=sql-server-ver15) in your SQL queries.
    * For example, some reserve words are `SELECT`, `INNER`, `JOIN`--so don't use those words as columns.



Here, we modified the query to have declarative statements be on seperate lines and capitalize said statements.


```sql
SELECT 

id, createdDate, events.login_id, geoState, firstName, lastName, SUM(login.logIn) total_logins

FROM mySpace_events AS events
LEFT OUTER JOIN mySpace_users users ON users.id = events.user_id
WHERE login.date >= CURRENT_DATE - (SELECT MIN(createdDate) FROM mySpace_users WHERE profile  = 'Musician')
GROUP BY 1,2,3,4,5,6
```

## Spacing

"Do not optimize for a smaller number of lines of code. newlines are cheap, brain time is expensive" - [Source](https://github.com/fishtown-analytics/corp/blob/master/dbt_coding_conventions.md)

![Space](https://thumbs.gfycat.com/ElaborateEsteemedJackal-max-1mb.gif)





```sql
SELECT 

    id, 
    createdDate, 
    events.login_id, 
    geoState, 
    firstName, 
    lastName, 
    SUM(login.logIn) total_logins

FROM mySpace_events AS events

LEFT OUTER JOIN mySpace_users users ON
     users.id = events.user_id

WHERE login.date >= CURRENT_DATE - (SELECT MIN(createdDate) FROM mySpace_users WHERE profile  = 'Musician')

GROUP BY 1,2,3,4,5,6
```

## 80 Characters

Here, I am abiding to past enforcement of reading ergonomics that I learned from the engineering community. However, I think there is something more, historical to this[...seen here](https://softwareengineering.stackexchange.com/questions/148677/why-is-80-characters-the-standard-limit-for-code-width).

Here, the long-winded sub-query went from one line, to multiple lines, within an 80 character limit.



```sql
SELECT 

    id, 
    createdDate, 
    events.login_id, 
    geoState, 
    firstName, 
    lastName, 
    SUM(login.logIn) total_logins

FROM mySpace_events AS events

LEFT OUTER JOIN mySpace_users users

ON users.id = events.user_id

WHERE login.date >= CURRENT_DATE - (
    SELECT 
    
        MIN(createdDate) 
    
    FROM mySpace_users 
    
    WHERE profile  = 'Musician'
    )

GROUP BY 1,2,3,4,5,6
```

## Subqueries and WITH statements



```sql

WITH earliest_musician_user_date AS ( 

    SELECT 
    
        MIN(createdDate) 
    
    FROM mySpace_users 
    
    WHERE profile  = 'Musician'

)

SELECT 

    id, 
    createdDate, 
    events.login_id, 
    geoState, 
    firstName, 
    lastName, 
    SUM(login.logIn) total_logins

FROM mySpace_events AS events

LEFT OUTER JOIN mySpace_users users

ON users.id = events.user_id

WHERE login.date >= CURRENT_DATE - earliest_musician_user_date

GROUP BY 1,2,3,4,5,6
```



## Aliases

Don't pass on the `AS` statement. With adding the alias, we are ensuring we are explicit with defining nick-names of ingested information, to what we can expect for output information.




Here, we move the subqueries from the bottom of the list to the top, and then call the reference in the same location.

```sql

WITH earliest_musician_user_date AS ( 

    SELECT 
    
        MIN(createdDate)
    
    FROM mySpace_users 
    
    WHERE profile  = 'Musician'

)

SELECT 

    id, 
    createdDate, 
    events.login_id, 
    geoState, 
    firstName, 
    lastName, 
    SUM(login.logIn) AS total_logins

FROM mySpace_events AS events

LEFT OUTER JOIN AS mySpace_users users ON 
    users.id = events.user_id

WHERE login.date >= CURRENT_DATE - earliest_musician_user_date

GROUP BY 1,2,3,4,5,6
```

## Camel Case or Snake?

In other coding language readability guidelines, there is an enforcement of code readability. Particularly, in Python [PEP 8](https://www.python.org/dev/peps/pep-0008/) variable names are set to `camelCase` and file names are set to `snake_case`.

[![Camel Snake](https://4.bp.blogspot.com/-c4o1jtkNXoM/TZyVEvHZTwI/AAAAAAAAAW4/XlD0PjNQdBM/s1600/Slithering-Camel.jpg)](https://www.python.org/dev/peps/pep-0008/)

with SQL, we have our naming conventions be 'Snake" conventions. 



Here, we have all variable names be snake case (e.g. `createdDate` $\rightarrow$ `created_date`), along with other columns.

```sql

WITH earliest_musician_user_date AS ( 

    SELECT 
    
        MIN(created_date)
    
    FROM mySpace_users 
    
    WHERE profile  = 'Musician'

)

SELECT 

    id, 
    created_date, 
    events.login_id, 
    geo_state, 
    first_name, 
    last_name, 
    SUM(login.logIn) AS total_logins

FROM mySpace_events AS events

LEFT OUTER JOIN AS myspace_users users

ON users.id = events.user_id

WHERE login.date >= CURRENT_DATE - earliest_musician_user_date

GROUP BY 1,2,3,4,5,6
```
## Comments

Both in the beginning of the code snippet to say what data the snippet pulls, the business logic it includes, and throughout, as much as possible, to reference subqueries. SQL makes it hard to read through an entire piece of code without running specific pieces one by one to get where you’re going and comments will help jog the memory. Include them at the end of lines in code, or in blocks at the beginning of code.




Here, we add a block-quote comment `/* */` and single-line comments `--` to clarify logic

```sql

/*
Querying the Myspace Events table with user information for the time after the first Musician profile-user was created.
*/

WITH earliest_musician_user_date AS ( 

    SELECT 
    
        MIN(created_date)
    
    FROM mySpace_users 
    
    WHERE profile  = 'Musician'

)

SELECT 

    id, 
    created_date, 
    events.login_id, 
    geo_state, 
    first_name, 
    last_name, 
    SUM(login.logIn) AS total_logins -- Obtaining total logins

FROM mySpace_events AS events

LEFT OUTER JOIN AS myspace_users users

ON users.id = events.user_id

WHERE login.date >= CURRENT_DATE - earliest_musician_user_date

GROUP BY 1,2,3,4,5,6
```

There are other things to refine here, but let's stop here. 
> e.g. GROUP BY names should be actual names of columns, when code is in production

Now, take a look at the query above compared to the original one?

```sql
select 

id, createdDate, events.login_id, geoState, firstName, lastName, sum(login.logIn) total_logins

from mySpace_events as events
LEFT OUTER JOIN mySpace_users users
on users.id = events.user_id
WHERE login.date >= current_date - (select min(createdDate) from mySpace_users where profile  = 'Musician')
group by 1,2,3,4,5,6
```

Isn't that better?! 

![We can read!](https://media1.giphy.com/media/xT5LMWbDQuncMUJTmU/source.gif)

# Recap

We learned by encouraging a readability practice for submitting code to a team's repository, production, developers do not have to face:

* Difficult to understand logic and ouuts
* Longer to debug
* Maintenance issues
* The complexity of reading code

And possible enable:

* Increased Productivity 
* More time to focus on the core logic.
* Quicker turnover of fixes or tasks


Now, 
> Never RIGHT, move it to the LEFT..and **SQL ON**...

![You do you](https://i.kym-cdn.com/photos/images/original/001/175/473/0c3.gif)


# Resources

1. [Vicki Boykis' take on readable SQL](http://veekaybee.github.io/2015/06/02/good-sql/)

2. [SQL Style Guide](https://www.sqlstyle.guide/)

3. [Craig Kersteins' take on Legible SQL](http://www.craigkerstiens.com/2016/01/08/writing-better-sql/)

4. [Quora: Why do we need to improve readability of our code?](https://www.quora.com/Why-do-we-need-to-improve-the-readability-of-our-code)

5. Unofficial: My own past experience on SQL Readability form 2018 learnings
> Note: Company never open-sourced Readability standards for SQL, [but has for others]((http://google.github.io/styleguide/))

6. [Code Project; Writing SQL](https://www.codeproject.com/Articles/126380/Writing-Readable-SQL)

7. [PEP 8](https://www.python.org/dev/peps/pep-0008/)