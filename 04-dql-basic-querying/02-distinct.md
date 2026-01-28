# DISTINCT

The `DISTINCT` keyword removes duplicate values from your query results.

## Basic Usage

```sql
SELECT DISTINCT department FROM employees;
```

_This returns each department only once, even if it appears in many rows._

## Example Table

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 2   | Nasrin   | IT         |
| 3   | Sumon    | HR         |

## Example Output

| department |
| ---------- |
| HR         |
| IT         |

## Multiple Columns

```sql
SELECT DISTINCT department, name FROM employees;
```

_This returns unique combinations of department and name._

## Common Mistakes

- Using DISTINCT when you only need a count of unique values (use `COUNT(DISTINCT column)` instead).
- Forgetting that DISTINCT applies to all selected columns together.

## Best Practices

- Use DISTINCT only when necessary, as it can slow down queries on large tables.

## Practice Challenge

1. List all unique departments from the `employees` table.
2. Find the number of unique names in the table.
