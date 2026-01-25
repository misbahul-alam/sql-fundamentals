# NULL Handling

## Overview

`NULL` in SQL represents a missing or unknown value. It is not the same as zero or an empty string. Special care is needed when working with `NULL` values in queries.

## Checking for NULL

Use `IS NULL` and `IS NOT NULL` to test for `NULL` values:

```sql
SELECT * FROM table_name
WHERE column_name IS NULL;
```

```sql
SELECT * FROM table_name
WHERE column_name IS NOT NULL;
```

## Example

Suppose you have a table called `students`:

| id  | name    | age | score |
| --- | ------- | --- | ----- |
| 1   | Alice   | 20  | 90    |
| 2   | Bob     | 21  | NULL  |
| 3   | Charlie | 19  | 92    |
| 4   | Diana   | 22  | NULL  |

To get all students with missing scores:

```sql
SELECT name FROM students
WHERE score IS NULL;
```

**Result:**

| name  |
| ----- |
| Bob   |
| Diana |

To get all students with a known score:

```sql
SELECT name, score FROM students
WHERE score IS NOT NULL;
```

**Result:**

| name    | score |
| ------- | ----- |
| Alice   | 90    |
| Charlie | 92    |

## Notes

- Comparisons with `NULL` using `=`, `!=`, `<`, or `>` do not work as expected. Always use `IS NULL` or `IS NOT NULL`.
- Functions like `COUNT(column)` ignore `NULL` values, but `COUNT(*)` counts all rows.
- Use `COALESCE(column, value)` to replace `NULL` with a default value in results.

## Practice

Write a `SELECT` statement to get the names of students whose score is not known (i.e., is `NULL`).
