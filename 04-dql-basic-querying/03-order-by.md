# ORDER BY

The `ORDER BY` clause sorts your query results by one or more columns.

## Basic Usage

```sql
SELECT * FROM employees
ORDER BY name ASC;
```

_This sorts the results alphabetically by name (A-Z)._

## Descending Order

```sql
SELECT * FROM employees
ORDER BY id DESC;
```

_This sorts the results by id from highest to lowest._

## Multiple Columns

```sql
SELECT * FROM employees
ORDER BY department ASC, name DESC;
```

_Sorts first by department (A-Z), then by name (Z-A) within each department._

## Example Table

| id  | name     | department |
| --- | -------- | ---------- |
| 2   | Nasrin   | IT         |
| 1   | Misbahul | HR         |
| 3   | Sumon    | HR         |

## Example Output (ORDER BY name ASC)

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 2   | Nasrin   | IT         |
| 3   | Sumon    | HR         |

## Common Mistakes

- Forgetting to specify ASC or DESC (ASC is default).
- Sorting by columns not in the SELECT list (allowed, but can be confusing).

## Best Practices

- Always specify the sort direction for clarity.
- Use multiple columns for more precise sorting.

## Practice Challenge

1. List all employees sorted by department, then by name (both ascending).
2. Show all employees with the highest id first.
