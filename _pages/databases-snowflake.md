---
permalink: /notes/databases-snowflake
title: "Databases: Snowflake"
author_profile: false 
toc: true
---

# Parsing JSON with ANSCII SQL in Snowflake

* [How to Analyze JSON With Snowflake](https://www.snowflake.com/wp-content/uploads/2017/08/Snowflake-How-to-Analyze-JSON-with-SQL.pdf)

# LISTAGG Missing <delimiter>

If one were to use the LISTAGG operation like the following, and NULL values still exist in said list, they are included in the resulting operation

`LISTAGG( [ DISTINCT ] <expr1> [, <delimiter> ]`

However, if you add the resulting ORDER BY condition in the remainder of LISTAGG, it returns a list of non-NULL values with such delimiter


`LISTAGG( [ DISTINCT ] <expr1> [, <delimiter> ] ) [ WITHIN GROUP ( <orderby_clause> ) ]`

So, e.g. 

```
SELECT LISTAGG(o_orderkey, ', ')
    FROM orders WHERE o_totalprice > 450000;

------------------------------------------------------+
             LISTAGG(O_ORDERKEY, ' ')                 |
------------------------------------------------------+
 41445, 55937, 67781, 80550, 95808, 101700, 103136, ''|
------------------------------------------------------+
```

The additional value at the end is due to a NULL value. So, to exclude it, add the remaining `WITHIN GROUP` to remove it in th results.

```
```
SELECT LISTAGG(o_orderkey, ', ')  WITHIN GROUP (ORDER BY 1) AS orders
    FROM orders WHERE o_totalprice > 450000;
```

# Migrating from one query engine and/or database to Snowflake

* [Instacart and migrating from Redshift to Snowflake](https://community.snowflake.com/s/article/Migrating-from-Redshift-to-Snowflake)

* [dbt's take & hints on transitioning from Redshift to Snowflake, from Tristan Handy](https://medium.com/@jthandy/how-compatible-are-redshift-and-snowflakes-sql-syntaxes-c2103a43ae84)