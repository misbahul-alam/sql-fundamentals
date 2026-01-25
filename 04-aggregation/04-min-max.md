# MIN & MAX

## Overview

`MIN` and `MAX` are aggregate functions in SQL that return the smallest and largest values in a column, respectively.

## Syntax

```sql
SELECT MIN(column_name) FROM table_name;
SELECT MAX(column_name) FROM table_name;
```

## Example

Suppose you have a table called `students`:

| id  | name    | score |
| --- | ------- | ----- |
| 1   | Alice   | 90    |
| 2   | Bob     | 85    |
| 3   | Charlie | 92    |
| 4   | Diana   | NULL  |

To get the minimum and maximum score:

```sql
SELECT MIN(score) AS min_score, MAX(score) AS max_score FROM students;
```

**Result:**

| min_score | max_score |
| --------- | --------- |
| 85        | 92        |

## Practice

Write a query to get the lowest and highest student scores, ignoring NULLs.
