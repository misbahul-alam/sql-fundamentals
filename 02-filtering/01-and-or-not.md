# AND, OR, NOT

## Overview

`AND`, `OR`, and `NOT` are logical operators used in SQL to combine or negate conditions in the `WHERE` clause.

## Syntax

```sql
SELECT column1, column2
FROM table_name
WHERE condition1 AND condition2;

SELECT column1, column2
FROM table_name
WHERE condition1 OR condition2;

SELECT column1, column2
FROM table_name
WHERE NOT condition;
```

## Example

Suppose you have a table called `students`:

| id  | name    | age | score |
| --- | ------- | --- | ----- |
| 1   | Alice   | 20  | 90    |
| 2   | Bob     | 21  | 85    |
| 3   | Charlie | 19  | 92    |
| 4   | Diana   | 22  | 88    |

To get students older than 20 with a score above 85:

```sql
SELECT name FROM students
WHERE age > 20 AND score > 85;
```

**Result:**

| name  |
| ----- |
| Diana |

To get students younger than 20 or with a score above 90:

```sql
SELECT name FROM students
WHERE age < 20 OR score > 90;
```

**Result:**

| name    |
| ------- |
| Charlie |

To get students who do not have a score of 90:

```sql
SELECT name FROM students
WHERE NOT score = 90;
```

**Result:**

| name    |
| ------- |
| Bob     |
| Charlie |
| Diana   |

## Practice

Write a `SELECT` statement to get the names of students who are older than 20 and have a score less than 90.
