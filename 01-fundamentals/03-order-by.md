# ORDER BY

## Overview

The `ORDER BY` clause in SQL is used to **sort the result set** of a query by one or more columns. By default, sorting is in ascending order.

## Basic Syntax

```sql
SELECT column1, column2
FROM table_name
ORDER BY column1 [ASC|DESC];
```

## Example

Suppose you have a table called `students`:

| id  | name    | age | score |
| --- | ------- | --- | ----- |
| 1   | Alice   | 20  | 90    |
| 2   | Bob     | 21  | 85    |
| 3   | Charlie | 19  | 92    |

To get all students sorted by score in descending order:

```sql
SELECT name, score FROM students
ORDER BY score DESC;
```

**Result:**

| name    | score |
| ------- | ----- |
| Charlie | 92    |
| Alice   | 90    |
| Bob     | 85    |

## Notes

- `ASC` means ascending order (default).
- `DESC` means descending order.
- You can sort by multiple columns: `ORDER BY score DESC, age ASC`.

## Practice

Write a `SELECT` statement to get all students' names and ages, sorted by age in ascending order from the `students` table.
