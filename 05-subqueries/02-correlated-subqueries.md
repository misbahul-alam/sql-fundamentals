# Correlated Subqueries

## Overview

A correlated subquery is a subquery that references columns from the outer query. It is evaluated once for each row processed by the outer query.

## Syntax

```sql
SELECT column1
FROM table1 t1
WHERE EXISTS (
  SELECT 1 FROM table2 t2 WHERE t2.column = t1.column
);
```

## Example

Suppose you have two tables:

**students**
| id | name |
| --- | ------- |
| 1 | Alice |
| 2 | Bob |
| 3 | Charlie |

**scores**
| student_id | score |
| ---------- | ----- |
| 1 | 90 |
| 2 | 85 |
| 3 | 92 |

To get the names of students who have a score above 90:

```sql
SELECT name FROM students s
WHERE EXISTS (
  SELECT 1 FROM scores sc WHERE sc.student_id = s.id AND sc.score > 90
);
```

**Result:**

| name    |
| ------- |
| Charlie |

## Practice

Write a query to get the names of students who do not have a score recorded in the scores table.
