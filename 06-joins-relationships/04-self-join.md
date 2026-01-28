# SELF JOIN

A `SELF JOIN` joins a table to itself. Useful for hierarchical data like managers and employees.

## Syntax

```sql
SELECT e1.name AS employee, e2.name AS manager
FROM employees e1
LEFT JOIN employees e2
	ON e1.manager_id = e2.id;
```

## Example Table

| id  | name  | manager_id |
| --- | ----- | ---------- |
| 1   | Alice | NULL       |
| 2   | Bob   | 1          |
| 3   | Carol | 1          |

## Example Output

| employee | manager |
| -------- | ------- |
| Alice    | NULL    |
| Bob      | Alice   |
| Carol    | Alice   |

## Visual Diagram

Each employee row is joined to another row in the same table (the manager).

## Common Mistakes

- Forgetting to use table aliases (e1, e2).
- Mixing up which column is the manager and which is the employee.

## Best Practices

- Always use aliases for clarity.
- Use LEFT JOIN to include employees without managers.

## Practice Challenge

1. List all employees and their managers.
2. What happens if an employee has no manager?
