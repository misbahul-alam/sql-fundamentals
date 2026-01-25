# EXISTS vs IN

## Overview

`EXISTS` and `IN` are both used to test for the existence of rows in a subquery, but they work differently and have different performance characteristics.

## Syntax

```sql
-- Using EXISTS
SELECT column1 FROM table1
WHERE EXISTS (SELECT 1 FROM table2 WHERE ...);

-- Using IN
SELECT column1 FROM table1
WHERE column1 IN (SELECT column2 FROM table2);
```

## Example

Suppose you have two tables:

**students**
| id | name |
| --- | ------- |
| 1 | Alice |
| 2 | Bob |
| 3 | Charlie |

**honor_roll**
| student_id |
| ---------- |
| 1 |
| 3 |

To get the names of students on the honor roll using EXISTS:

```sql
SELECT name FROM students s
WHERE EXISTS (
  SELECT 1 FROM honor_roll h WHERE h.student_id = s.id
);
```

To get the same result using IN:

```sql
SELECT name FROM students
WHERE id IN (SELECT student_id FROM honor_roll);
```

## Notes

- `EXISTS` is often more efficient for correlated subqueries.
- `IN` is simpler for small lists or subqueries.

## Practice

Write a query to get the names of students who are not on the honor roll using NOT EXISTS.
