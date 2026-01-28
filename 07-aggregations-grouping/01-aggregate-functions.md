# Aggregate Functions

Aggregate functions perform calculations on multiple rows and return a single value.

## Common Aggregate Functions

- `SUM(column)`: Total of all values
- `AVG(column)`: Average value
- `MIN(column)`: Smallest value
- `MAX(column)`: Largest value
- `COUNT(column)`: Number of non-NULL values

## Example Table

| id  | name     | salary |
| --- | -------- | ------ |
| 1   | Misbahul | 50000  |
| 2   | Nasrin   | 60000  |
| 3   | Sumon    | 55000  |

## Example Queries

```sql
SELECT SUM(salary) AS total_salary FROM employees;
-- Returns 165000

SELECT AVG(salary) AS avg_salary FROM employees;
-- Returns 55000

SELECT MIN(salary) AS min_salary, MAX(salary) AS max_salary FROM employees;
-- Returns 50000 and 60000

SELECT COUNT(*) AS num_employees FROM employees;
-- Returns 3
```

## Common Mistakes

- Using aggregate functions without GROUP BY when grouping is needed.
- Forgetting to use aliases for result columns.

## Best Practices

- Always use aliases for clarity.
- Use COUNT(\*) to count all rows, COUNT(column) to count non-NULLs.

## Practice Challenge

1. Find the highest and lowest salary in the employees table.
2. Count how many employees have a salary above 55000.
