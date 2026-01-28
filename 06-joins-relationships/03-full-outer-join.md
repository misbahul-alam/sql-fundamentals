# FULL OUTER JOIN

A `FULL OUTER JOIN` returns all rows from both tables, matching rows where possible. If there is no match, NULLs are shown.

## Syntax

```sql
SELECT employees.name, departments.department_name
FROM employees
FULL OUTER JOIN departments
	ON employees.department_id = departments.id;
```

## Example Tables

**employees**
| id | name | department_id |
|----|----------|---------------|
| 1 | Misbahul | 1 |
| 2 | Nasrin | 2 |
| 3 | Sumon | 3 |

**departments**
| id | department_name |
|----|-----------------|
| 1 | HR |
| 2 | IT |
| 3 | Finance |
| 4 | Sales |

## Example Output

| name     | department_name |
| -------- | --------------- |
| Misbahul | HR              |
| Nasrin   | IT              |
| Sumon    | Finance         |
| NULL     | Sales           |

## Visual Diagram

FULL OUTER JOIN: All rows from both tables, NULLs where no match.

## Common Mistakes

- Not all databases support FULL OUTER JOIN (use UNION of LEFT and RIGHT JOINs if needed).
- Not handling NULLs in results.

## Best Practices

- Use FULL OUTER JOIN to see all data, even if not matched.
- Always check for NULLs in the result.

## Practice Challenge

1. List all employees and all departments, showing NULL where there is no match.
2. What happens if a department has no employees?
