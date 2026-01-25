# LIMIT & OFFSET

## Overview

The `LIMIT` and `OFFSET` clauses in SQL are used to **control the number of rows** returned by a query and to **skip a specified number of rows**. This is useful for pagination and sampling data.

## Basic Syntax

```sql
SELECT column1, column2
FROM table_name
LIMIT number_rows OFFSET number_skip;
```

You can also use just `LIMIT`:

```sql
SELECT * FROM table_name
LIMIT 5;
```

## Example

Suppose you have a table called `students`:

| id  | name    | age | score |
| --- | ------- | --- | ----- |
| 1   | Alice   | 20  | 90    |
| 2   | Bob     | 21  | 85    |
| 3   | Charlie | 19  | 92    |
| 4   | Diana   | 22  | 88    |
| 5   | Ethan   | 20  | 91    |
| 6   | Fiona   | 23  | 87    |

To get the first 3 students:

```sql
SELECT name, score FROM students
LIMIT 3;
```

**Result:**

| name    | score |
| ------- | ----- |
| Alice   | 90    |
| Bob     | 85    |
| Charlie | 92    |

To skip the first 2 students and get the next 3:

```sql
SELECT name, score FROM students
LIMIT 3 OFFSET 2;
```

**Result:**

| name    | score |
| ------- | ----- |
| Charlie | 92    |
| Diana   | 88    |
| Ethan   | 91    |

## Notes

- `LIMIT` is supported in most SQL databases (e.g., MySQL, PostgreSQL, SQLite). In SQL Server, use `TOP` instead.
- `OFFSET` is optional and is used for skipping rows.
- The order of rows is not guaranteed unless you use `ORDER BY`.

## Practice

Write a `SELECT` statement to get 2 students with the highest scores from the `students` table.
