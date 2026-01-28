# CTEs (WITH)

A Common Table Expression (CTE) is a temporary result set you can reference within a SELECT, INSERT, UPDATE, or DELETE statement.

## Syntax

```sql
WITH dept_counts AS (
	SELECT department, COUNT(*) AS num_employees
	FROM employees
	GROUP BY department
)
SELECT * FROM dept_counts WHERE num_employees > 1;
```

_This CTE counts employees per department, then selects departments with more than one employee._

## Why Use CTEs?

- Improves readability for complex queries
- Allows you to break queries into logical steps
- Can reference the CTE multiple times in the main query

## Example Table

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 2   | Nasrin   | IT         |
| 3   | Sumon    | HR         |

## Common Mistakes

- Forgetting to use the CTE name in the main query.
- Using the same CTE name as a table or column.

## Best Practices

- Use CTEs for step-by-step logic in complex queries.
- Name CTEs clearly and descriptively.

## Practice Challenge

1. Write a CTE to find the average salary per department.
2. Use a CTE to list employees who work in departments with more than one employee.
