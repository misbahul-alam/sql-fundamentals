# Composite Index

## Overview

A composite index is an index on two or more columns of a table. It is useful for queries that filter or sort on multiple columns.

## Example

Suppose you have a table called `students`:

| id  | name    | age | score |
| --- | ------- | --- | ----- |
| 1   | Alice   | 20  | 90    |
| 2   | Bob     | 21  | 85    |
| 3   | Charlie | 19  | 92    |

To create a composite index on `age` and `score`:

```sql
CREATE INDEX idx_age_score ON students(age, score);
```

## Notes

- The order of columns in a composite index matters.
- Composite indexes are useful for queries that filter or sort on both columns.

## Practice

Write a statement to create a composite index on the `name` and `score` columns of the `students` table.
