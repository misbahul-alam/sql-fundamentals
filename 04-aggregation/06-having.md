# HAVING

## Overview

`HAVING` is used in SQL to filter groups created by `GROUP BY` based on aggregate conditions.

## Syntax

```sql
SELECT column, AGG_FUNC(column)
FROM table_name
GROUP BY column
HAVING condition;
```

## Example

Suppose you have a table called `students`:

| id  | name    | age | score |
| --- | ------- | --- | ----- |
| 1   | Alice   | 20  | 90    |
| 2   | Bob     | 21  | 85    |
| 3   | Charlie | 20  | 92    |
| 4   | Diana   | 21  | 88    |

To get age groups with an average score above 90:

```sql
SELECT age, AVG(score) FROM students
GROUP BY age
HAVING AVG(score) > 90;
```

**Result:**

| age | avg |
| --- | --- |
| 20  | 91  |

## Practice

Write a query to get age groups with more than one student.
