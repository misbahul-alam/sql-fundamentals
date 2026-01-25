# LEFT JOIN

## Overview

`LEFT JOIN` returns all rows from the left table, and the matched rows from the right table. If there is no match, the result is NULL on the right side.

## Syntax

```sql
SELECT columns
FROM table1
LEFT JOIN table2 ON table1.column = table2.column;
```

## Example

Suppose you have two tables:

**students**
| id | name |
| --- | ------- |
| 1 | Alice |
| 2 | Bob |
| 3 | Charlie |
| 4 | Diana |

**scores**
| student_id | score |
| ---------- | ----- |
| 1 | 90 |
| 2 | 85 |
| 3 | 92 |

To get all students and their scores (if any):

```sql
SELECT s.name, sc.score
FROM students s
LEFT JOIN scores sc ON s.id = sc.student_id;
```

**Result:**

| name    | score |
| ------- | ----- |
| Alice   | 90    |
| Bob     | 85    |
| Charlie | 92    |
| Diana   | NULL  |

## Practice

Write a query to get all students and their scores, showing NULL for students without a score.
