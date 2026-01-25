# LIKE & ILIKE

## Overview

`LIKE` is used in SQL to search for a specified pattern in a column. `ILIKE` is a case-insensitive version (supported in PostgreSQL).

## Syntax

```sql
SELECT column1
FROM table_name
WHERE column1 LIKE 'pattern';
```

- `%` matches any sequence of characters
- `_` matches a single character

## Example

Suppose you have a table called `students`:

| id  | name    |
| --- | ------- |
| 1   | Alice   |
| 2   | Bob     |
| 3   | Charlie |
| 4   | Diana   |

To find names starting with 'A':

```sql
SELECT name FROM students
WHERE name LIKE 'A%';
```

**Result:**

| name  |
| ----- |
| Alice |

To find names ending with 'a':

```sql
SELECT name FROM students
WHERE name LIKE '%a';
```

**Result:**

| name  |
| ----- |
| Diana |

## Practice

Write a `SELECT` statement to find all students whose names contain the letter 'i'.
