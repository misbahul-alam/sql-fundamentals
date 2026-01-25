# AVG

## Overview

`AVG` is an aggregate function in SQL that returns the average value of a numeric column.

## Syntax

```sql
SELECT AVG(column_name) FROM table_name;
```

## Example

Suppose you have a table called `students`:

| id  | name    | score |
| --- | ------- | ----- |
| 1   | Alice   | 90    |
| 2   | Bob     | 85    |
| 3   | Charlie | 92    |
| 4   | Diana   | NULL  |

To get the average score of all students:

```sql
SELECT AVG(score) FROM students;
```

**Result:**

| avg |
| --- |
| 89  |

## Practice

Write a query to get the average score of students with a known score.
