# COUNT

## Overview

`COUNT` is an aggregate function in SQL that returns the number of rows that match a specified condition.

## Syntax

```sql
SELECT COUNT(*) FROM table_name;
SELECT COUNT(column_name) FROM table_name WHERE condition;
```

## Example

Suppose you have a table called `students`:

| id  | name    | score |
| --- | ------- | ----- |
| 1   | Alice   | 90    |
| 2   | Bob     | 85    |
| 3   | Charlie | 92    |
| 4   | Diana   | NULL  |

To count all students:

```sql
SELECT COUNT(*) FROM students;
```

**Result:**

| count |
| ----- |
| 4     |

To count students with a known score:

```sql
SELECT COUNT(score) FROM students;
```

**Result:**

| count |
| ----- |
| 3     |

## Practice

Write a query to count the number of students with a score above 90.
