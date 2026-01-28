# Subqueries

A subquery is a query inside another SQL query. It can be used in SELECT, FROM, or WHERE clauses.

## Subquery in WHERE

```sql
SELECT name
FROM employees
WHERE department_id = (
	SELECT id FROM departments WHERE department_name = 'HR'
);
```

_Finds employees who work in the HR department._

## Subquery in FROM

```sql
SELECT avg_salary
FROM (
	SELECT AVG(salary) AS avg_salary FROM employees
) AS sub;
```

_Uses a subquery as a temporary table._

## Example Table

| id  | name     | department_id | salary |
| --- | -------- | ------------- | ------ |
| 1   | Misbahul | 1             | 50000  |
| 2   | Nasrin   | 2             | 60000  |
| 3   | Sumon    | 1             | 55000  |

## Common Mistakes

- Subquery returns more than one row (use IN or EXISTS for multiple results).
- Forgetting to alias subqueries in FROM.

## Best Practices

- Use subqueries for clarity, but avoid nesting too deeply.
- Use EXISTS or IN for better performance with large data sets.

## Practice Challenge

1. Find employees who earn more than the average salary.
2. List departments with more than two employees using a subquery.
