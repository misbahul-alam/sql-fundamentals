# INNER JOIN

An `INNER JOIN` returns rows when there is a match in both tables.

## Syntax

```sql
SELECT employees.name, departments.department_name
FROM employees
INNER JOIN departments
	ON employees.department_id = departments.id;
```

## Example Tables

**employees**
| id | name | department_id |
|----|----------|---------------|
| 1 | Misbahul | 1 |
| 2 | Nasrin | 2 |
| 3 | Sumon | 1 |

**departments**
| id | department_name |
|----|-----------------|
| 1 | HR |
| 2 | IT |

## Example Output

| name     | department_name |
| -------- | --------------- |
| Misbahul | HR              |
| Nasrin   | IT              |
| Sumon    | HR              |

## Visual Diagram

```
employees         departments
	 | id | dept_id |   | id | department_name |
	 |----|---------|   |----|-----------------|
	 | 1  |   1     |   | 1  | HR              |
	 | 2  |   2     |   | 2  | IT              |
	 | 3  |   1     |
```

**INNER JOIN** only returns rows where `department_id` matches `id` in both tables.

## Common Mistakes

- Forgetting the ON clause or using the wrong columns.
- Assuming INNER JOIN will return unmatched rows (it won't).

## Best Practices

- Always specify the join condition clearly.
- Use table aliases for readability in complex queries.

## Practice Challenge

1. Write a query to list all employees and their department names using INNER JOIN.
2. What happens if an employee has a department_id that doesn't exist in departments?
