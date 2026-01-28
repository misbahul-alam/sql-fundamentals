# GROUP BY

The `GROUP BY` clause groups rows that have the same values into summary rows.

## Basic Usage

```sql
SELECT department, COUNT(*) AS num_employees
FROM employees
GROUP BY department;
```

_Counts the number of employees in each department._

## Example Table

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 2   | Nasrin   | IT         |
| 3   | Sumon    | HR         |

## Example Output

| department | num_employees |
| ---------- | ------------- |
| HR         | 2             |
| IT         | 1             |

## Multiple Columns

```sql
SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department;
```

_Groups by department and calculates average salary for each._

## Common Mistakes

- Selecting columns not in GROUP BY or an aggregate function.
- Forgetting to use aggregate functions with GROUP BY.

## Best Practices

- Only select columns in GROUP BY or use aggregates.
- Use clear aliases for summary columns.

## Practice Challenge

1. Show the total salary for each department.
2. Count the number of employees in each department with more than one employee.
