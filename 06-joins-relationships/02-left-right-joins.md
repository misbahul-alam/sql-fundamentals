# LEFT & RIGHT JOINS

LEFT JOIN and RIGHT JOIN return all rows from one table and matching rows from the other.

## LEFT JOIN

Returns all rows from the left table, and matching rows from the right table. If no match, NULLs are shown.

```sql
SELECT employees.name, departments.department_name
FROM employees
LEFT JOIN departments
	ON employees.department_id = departments.id;
```

## RIGHT JOIN

Returns all rows from the right table, and matching rows from the left table. If no match, NULLs are shown.

```sql
SELECT employees.name, departments.department_name
FROM employees
RIGHT JOIN departments
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

## Example Output (LEFT JOIN)

| name     | department_name |
| -------- | --------------- |
| Misbahul | HR              |
| Nasrin   | IT              |
| Sumon    | Finance         |

## Example Output (RIGHT JOIN)

| name     | department_name |
| -------- | --------------- |
| Misbahul | HR              |
| Nasrin   | IT              |
| Sumon    | Finance         |
| NULL     | Sales           |

## Visual Diagram

LEFT JOIN: All rows from employees, matching departments (NULL if no match).
RIGHT JOIN: All rows from departments, matching employees (NULL if no match).

## Common Mistakes

- Confusing which table is left/right.
- Not handling NULLs in results.

## Best Practices

- Use LEFT JOIN more often (RIGHT JOIN is less common).
- Always check for NULLs in the result.

## Practice Challenge

1. List all employees and their department names, including employees without a department.
2. List all departments and their employees, including departments with no employees.
