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
select listagg(o_orderkey, ' ')
    from orders where o_totalprice > 450000;

---------------------------------------------+
          LISTAGG(O_ORDERKEY, ' ')           |
---------------------------------------------+
 41445 55937 67781 80550 95808 101700 103136 |
---------------------------------------------+
```