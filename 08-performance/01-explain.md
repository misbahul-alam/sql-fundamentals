# EXPLAIN

## Overview

`EXPLAIN` is a SQL command that shows the execution plan of a query. It helps you understand how the database will execute your query and where performance bottlenecks may occur.

## Syntax

```sql
EXPLAIN SELECT * FROM table_name WHERE condition;
```

## Example

Suppose you have a query:

```sql
SELECT * FROM students WHERE score > 90;
```

Running `EXPLAIN` on this query will show whether an index is used and how the table is scanned.

## Practice

Write an `EXPLAIN` statement for a query that selects students with a score below 80.
