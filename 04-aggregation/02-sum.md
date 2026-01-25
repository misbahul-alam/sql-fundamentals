# SUM

## Overview

`SUM` is an aggregate function in SQL that returns the total sum of a numeric column.

## Syntax

```sql
SELECT SUM(column_name) FROM table_name;
```

## Example

Suppose you have a table called `students`:

| id  | name    | score |
| --- | ------- | ----- |
| 1   | Alice   | 90    |
| 2   | Bob     | 85    |
| 3   | Charlie | 92    |
| 4   | Diana   | NULL  |

To get the total score of all students:

```sql
SELECT SUM(score) FROM students;
```

**Result:**

| sum |
| --- |
| 267 |

## Practice

Write a query to get the total score of students with a score above 85.
