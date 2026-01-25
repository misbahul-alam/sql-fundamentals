# GROUP BY

## Overview

`GROUP BY` is used in SQL to arrange identical data into groups. It is often used with aggregate functions.

## Syntax

```sql
SELECT column, AGG_FUNC(column)
FROM table_name
GROUP BY column;
```

## Example

Suppose you have a table called `students`:

| id  | name    | age | score |
| --- | ------- | --- | ----- |
| 1   | Alice   | 20  | 90    |
| 2   | Bob     | 21  | 85    |
| 3   | Charlie | 20  | 92    |
| 4   | Diana   | 21  | 88    |

To get the average score by age:

```sql
SELECT age, AVG(score) FROM students
GROUP BY age;
```

**Result:**

| age | avg  |
| --- | ---- |
| 20  | 91   |
| 21  | 86.5 |

## Practice

Write a query to count the number of students in each age group.
