# Indexes Basics

An index is a database object that speeds up data retrieval on a table column.

## Why Use Indexes?

- Makes SELECT queries faster, especially on large tables
- Used automatically by the database when searching, filtering, or joining

## Creating an Index

```sql
CREATE INDEX idx_department ON employees(department);
```

_Creates an index on the department column._

## Example Table

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 2   | Karim    | IT         |
| 3   | Nasrin   | HR         |

## How Indexes Work

Indexes are like a book's table of contents—helping the database find rows quickly.

## Dropping an Index

```sql
DROP INDEX idx_department;
```

## Common Mistakes

- Creating too many indexes (slows down INSERT/UPDATE/DELETE)
- Forgetting to drop unused indexes

## Best Practices

- Index columns used in WHERE, JOIN, or ORDER BY
- Avoid indexing columns with lots of duplicate values

## Practice Challenge

1. Create an index on the name column.
2. Drop the index after testing query speed.
