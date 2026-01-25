# SELECT

## Overview

The `SELECT` statement is the core of SQL. It is used to **retrieve data from one or more
tables** in a relational database. Every read operation in SQL begins with `SELECT`.

Understanding `SELECT` correctly is essential before learning filtering, joins,
aggregation, or optimization.

## Basic Syntax

```sql
SELECT column1, column2
FROM table_name;
```

## Selecting All Columns

To select all columns from a table, use the asterisk `*`:

```sql
SELECT * FROM table_name;
```

## Example

Suppose you have a table called `students`:

| id  | name    | age | score |
| --- | ------- | --- | ----- |
| 1   | Alice   | 20  | 90    |
| 2   | Bob     | 21  | 85    |
| 3   | Charlie | 19  | 92    |

To get all student names and scores:

```sql
SELECT name, score FROM students;
```

**Result:**

| name    | score |
| ------- | ----- |
| Alice   | 90    |
| Bob     | 85    |
| Charlie | 92    |

## Notes

- SQL keywords are not case-sensitive, but it is common to write them in uppercase.
- You can select as many columns as you need, separated by commas.
- The order of columns in the result matches the order in the `SELECT` clause.

## Practice

Try writing a `SELECT` statement to get the `id` and `age` of all students from the `students` table.
