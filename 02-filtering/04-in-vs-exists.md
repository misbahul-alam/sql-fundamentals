# IN vs EXISTS

## Overview

`IN` and `EXISTS` are used in SQL to test whether a value or set of values exists in a subquery or list.

## IN Syntax

```sql
SELECT column1
FROM table_name
WHERE column1 IN (value1, value2, ...);
```

## EXISTS Syntax

```sql
SELECT column1
FROM table_name
WHERE EXISTS (SELECT 1 FROM another_table WHERE ...);
```

## Example

Suppose you have two tables: `students` and `honor_roll`.

| id  | name    |
| --- | ------- |
| 1   | Alice   |
| 2   | Bob     |
| 3   | Charlie |
| 4   | Diana   |

| student_id |
| ---------- |
| 1          |
| 3          |

To get names of students on the honor roll using `IN`:

```sql
SELECT name FROM students
WHERE id IN (SELECT student_id FROM honor_roll);
```

To get the same result using `EXISTS`:

```sql
SELECT name FROM students s
WHERE EXISTS (
  SELECT 1 FROM honor_roll h WHERE h.student_id = s.id
);
```

## Notes

- `IN` is simpler for small lists or subqueries.
- `EXISTS` is often more efficient for correlated subqueries.

## Practice

Write a `SELECT` statement to get the names of students who are not on the honor roll using `NOT IN`.
