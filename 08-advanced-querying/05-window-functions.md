# Window Functions

Window functions perform calculations across sets of rows related to the current row.

## Common Window Functions

- `ROW_NUMBER()`: Unique row number per row
- `RANK()`: Ranking with gaps for ties
- `DENSE_RANK()`: Ranking without gaps
- `SUM()`, `AVG()`, etc. as windowed aggregates

## Syntax Example

```sql
SELECT name, department, salary,
	RANK() OVER (PARTITION BY department ORDER BY salary DESC) AS dept_rank
FROM employees;
```

_Ranks employees by salary within each department._

## Example Table

| id  | name     | department | salary |
| --- | -------- | ---------- | ------ |
| 1   | Misbahul | HR         | 50000  |
| 2   | Nasrin   | IT         | 60000  |
| 3   | Sumon    | HR         | 55000  |

## Example Output

| name     | department | salary | dept_rank |
| -------- | ---------- | ------ | --------- |
| Sumon    | HR         | 55000  | 1         |
| Misbahul | HR         | 50000  | 2         |
| Nasrin   | IT         | 60000  | 1         |

## PARTITION BY

Splits data into groups for the window function.

## Common Mistakes

- Forgetting ORDER BY in the window function.
- Not using PARTITION BY when needed.

## Best Practices

- Use window functions for advanced analytics (running totals, rankings).
- Always specify ORDER BY for predictable results.

## Practice Challenge

1. Add a row number to each employee ordered by salary.
2. Rank employees within each department by salary.
