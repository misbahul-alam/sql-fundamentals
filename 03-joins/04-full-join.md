# FULL JOIN

## Overview

`FULL JOIN` (or `FULL OUTER JOIN`) returns all rows when there is a match in either left or right table. Rows without a match in one of the tables will have NULLs for the missing side.

## Syntax

```sql
SELECT columns
FROM table1
FULL JOIN table2 ON table1.column = table2.column;
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
| 5 | 80 |

To get all students and all scores, matching where possible:

```sql
SELECT s.name, sc.score
FROM students s
FULL JOIN scores sc ON s.id = sc.student_id;
```

**Result:**

| name    | score |
| ------- | ----- |
| Alice   | 90    |
| Bob     | 85    |
| Charlie | 92    |
| Diana   | NULL  |
| NULL    | 80    |

## Practice

Write a query to get all students and all scores, showing NULL where there is no match.
