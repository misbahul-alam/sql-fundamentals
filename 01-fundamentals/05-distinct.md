# DISTINCT

## Overview

The `DISTINCT` keyword in SQL is used to **remove duplicate rows** from the result set of a `SELECT` query. It ensures that each row returned is unique for the selected columns.

## Basic Syntax

```sql
SELECT DISTINCT column1, column2
FROM table_name;
```

## Example

Suppose you have a table called `students`:

| id  | name    | age | score |
| --- | ------- | --- | ----- |
| 1   | Alice   | 20  | 90    |
| 2   | Bob     | 21  | 85    |
| 3   | Charlie | 19  | 92    |
| 4   | Alice   | 20  | 90    |

To get all unique student names:

```sql
SELECT DISTINCT name FROM students;
```

**Result:**

| name    |
| ------- |
| Alice   |
| Bob     |
| Charlie |

To get unique combinations of name and age:

```sql
SELECT DISTINCT name, age FROM students;
```

**Result:**

| name    | age |
| ------- | --- |
| Alice   | 20  |
| Bob     | 21  |
| Charlie | 19  |

## Notes

- `DISTINCT` applies to all columns listed in the `SELECT` clause.
- If you use `DISTINCT` with multiple columns, only rows with unique combinations of those columns are returned.

## Practice

Write a `SELECT` statement to get all unique scores from the `students` table.
