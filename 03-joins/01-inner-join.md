# INNER JOIN

## Overview

`INNER JOIN` returns rows when there is a match in both tables being joined.

## Syntax

```sql
SELECT columns
FROM table1
INNER JOIN table2 ON table1.column = table2.column;
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

To get each student's name and score:

```sql
SELECT s.name, sc.score
FROM students s
INNER JOIN scores sc ON s.id = sc.student_id;
```

**Result:**

| name    | score |
| ------- | ----- |
| Alice   | 90    |
| Bob     | 85    |
| Charlie | 92    |

## Practice

Write a query to get the names of students and their scores using an INNER JOIN.
