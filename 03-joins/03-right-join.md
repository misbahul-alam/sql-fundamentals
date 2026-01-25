# RIGHT JOIN

## Overview

`RIGHT JOIN` returns all rows from the right table, and the matched rows from the left table. If there is no match, the result is NULL on the left side.

## Syntax

```sql
SELECT columns
FROM table1
RIGHT JOIN table2 ON table1.column = table2.column;
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
| 4 | 88 |

To get all scores and the corresponding student names (if any):

```sql
SELECT s.name, sc.score
FROM students s
RIGHT JOIN scores sc ON s.id = sc.student_id;
```

**Result:**

| name    | score |
| ------- | ----- |
| Alice   | 90    |
| Bob     | 85    |
| Charlie | 92    |
| NULL    | 88    |

## Practice

Write a query to get all scores and the corresponding student names, showing NULL for scores without a matching student.
