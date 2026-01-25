# Subquery Basics

## Overview

A subquery is a query nested inside another SQL query. It can be used in SELECT, INSERT, UPDATE, or DELETE statements.

## Syntax

```sql
SELECT column1
FROM table_name
WHERE column2 = (SELECT ...);
```

## Example

Suppose you have a table called `students`:

| id  | name    | score |
| --- | ------- | ----- |
| 1   | Alice   | 90    |
| 2   | Bob     | 85    |
| 3   | Charlie | 92    |

To get the name of the student with the highest score:

```sql
SELECT name FROM students
WHERE score = (SELECT MAX(score) FROM students);
```

**Result:**

| name    |
| ------- |
| Charlie |

## Practice

Write a query to get the names of students with a score above the average score.
