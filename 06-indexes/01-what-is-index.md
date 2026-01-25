# What is an Index?

## Overview

An index is a database structure that improves the speed of data retrieval operations on a table at the cost of additional space and slower writes.

## Example

Suppose you have a table called `students` with thousands of rows. Creating an index on the `name` column:

```sql
CREATE INDEX idx_name ON students(name);
```

This allows the database to quickly find students by name.

## Notes

- Indexes speed up SELECT queries but can slow down INSERT, UPDATE, and DELETE operations.
- Primary keys automatically create a unique index.
- Use indexes on columns that are frequently searched or used in JOINs.

## Practice

Write a statement to create an index on the `score` column of the `students` table.
