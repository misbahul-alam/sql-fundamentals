# WHERE

## Overview

The `WHERE` clause in SQL is used to **filter rows** returned by a `SELECT` statement. It allows you to specify conditions that each row must satisfy to be included in the result set.

## Basic Syntax

```sql
SELECT column1, column2
FROM table_name
WHERE condition;
```

## Example

Suppose you have a table called `students`:

| id  | name    | age | score |
| --- | ------- | --- | ----- |
| 1   | Alice   | 20  | 90    |
| 2   | Bob     | 21  | 85    |
| 3   | Charlie | 19  | 92    |

To get all students with a score greater than 90:

```sql
SELECT name, score FROM students
WHERE score > 90;
```

**Result:**

| name    | score |
| ------- | ----- |
| Charlie | 92    |

## Common Operators

- `=` : Equal to
- `!=` or `<>` : Not equal to
- `>` : Greater than
- `<` : Less than
- `>=` : Greater than or equal to
- `<=` : Less than or equal to
- `AND`, `OR`, `NOT` : Combine multiple conditions

## Notes

- The `WHERE` clause can be used with `SELECT`, `UPDATE`, and `DELETE` statements.
- String values in conditions should be enclosed in single quotes: `'Alice'`.
- Multiple conditions can be combined using `AND` and `OR`.

## Practice

Write a `SELECT` statement to get the names of students who are older than 20 from the `students` table.
