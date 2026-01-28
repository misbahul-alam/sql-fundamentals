# Logical Operators

Logical operators let you combine multiple conditions in a WHERE clause.

## AND

```sql
SELECT * FROM employees
WHERE department = 'HR' AND id > 1;
```

_Returns employees in HR with id greater than 1._

## OR

```sql
SELECT * FROM employees
WHERE department = 'HR' OR department = 'IT';
```

_Returns employees in either HR or IT._

## NOT

```sql
SELECT * FROM employees
WHERE NOT department = 'HR';
```

_Returns employees not in HR._

## Example Table

| id  | name   | department |
| --- | ------ | ---------- |
| 1   | Rahim  | HR         |
| 2   | Karim  | IT         |
| 3   | Nasrin | HR         |
| 4   | Sumon  | Sales      |

## Example Output (WHERE department = 'HR' OR department = 'IT')

| id  | name   | department |
| --- | ------ | ---------- |
| 1   | Rahim  | HR         |
| 2   | Karim  | IT         |
| 3   | Nasrin | HR         |

## Common Mistakes

- Mixing up AND/OR logic (remember: AND is more restrictive, OR is less restrictive).
- Forgetting parentheses in complex conditions.

## Best Practices

- Use parentheses to clarify logic: `(A OR B) AND C`.
- Test your conditions with SELECT before using them in UPDATE/DELETE.

## Practice Challenge

1. Find employees in HR or Sales.
2. List employees not in IT.
