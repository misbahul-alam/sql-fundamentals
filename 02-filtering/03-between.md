# BETWEEN

## Overview

`BETWEEN` is used in SQL to filter the result set within a certain range. The range is inclusive.

## Syntax

```sql
SELECT column1, column2
FROM table_name
WHERE column_name BETWEEN value1 AND value2;
```

## Example

Suppose you have a table called `students`:

| id  | name    | age | score |
| --- | ------- | --- | ----- |
| 1   | Alice   | 20  | 90    |
| 2   | Bob     | 21  | 85    |
| 3   | Charlie | 19  | 92    |
| 4   | Diana   | 22  | 88    |

To get students with scores between 85 and 90:

```sql
SELECT name, score FROM students
WHERE score BETWEEN 85 AND 90;
```

**Result:**

| name  | score |
| ----- | ----- |
| Alice | 90    |
| Bob   | 85    |
| Diana | 88    |

## Practice

Write a `SELECT` statement to get the names of students whose age is between 20 and 22.
