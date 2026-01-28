# WHERE Clause

The `WHERE` clause filters rows in your query based on a condition.

## Basic Usage

```sql
SELECT * FROM employees
WHERE department = 'HR';
```

_Returns only employees in the HR department._

## Multiple Conditions

```sql
SELECT * FROM employees
WHERE department = 'IT' AND id > 1;
```

_Returns IT employees with id greater than 1._

## Example Table

| id  | name   | department |
| --- | ------ | ---------- |
| 1   | Rahim  | HR         |
| 2   | Karim  | IT         |
| 3   | Nasrin | HR         |

## Example Output (WHERE department = 'HR')

| id  | name   | department |
| --- | ------ | ---------- |
| 1   | Rahim  | HR         |
| 3   | Nasrin | HR         |

## Common Mistakes

- Using `=` instead of `LIKE` for partial matches.
- Forgetting quotes around text values.

## Best Practices

- Always use WHERE to avoid affecting all rows.
- Combine conditions with AND/OR for more precise filtering.

## Practice Challenge

1. Find all employees not in the HR department.
2. List employees with id greater than 1.
