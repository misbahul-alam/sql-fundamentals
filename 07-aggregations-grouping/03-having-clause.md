# HAVING Clause

The `HAVING` clause filters groups created by GROUP BY, similar to WHERE for individual rows.

## Basic Usage

```sql
SELECT department, COUNT(*) AS num_employees
FROM employees
GROUP BY department
HAVING COUNT(*) > 1;
```

_Shows only departments with more than one employee._

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

## Common Mistakes

- Using WHERE instead of HAVING for aggregates.
- Forgetting to use GROUP BY with HAVING.

## Best Practices

- Use WHERE for row-level filtering, HAVING for group-level filtering.
- Combine WHERE and HAVING for efficient queries.

## Practice Challenge

1. Show departments with an average salary above 55000.
2. List departments with fewer than 2 employees.
