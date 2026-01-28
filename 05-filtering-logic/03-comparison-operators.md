# Comparison Operators

Comparison operators help you filter data based on values and ranges.

## IN

```sql
SELECT * FROM employees
WHERE department IN ('HR', 'IT');
```

_Returns employees in either HR or IT._

## BETWEEN

```sql
SELECT * FROM employees
WHERE id BETWEEN 1 AND 3;
```

_Returns employees with id 1, 2, or 3._

## IS NULL / IS NOT NULL

```sql
SELECT * FROM employees
WHERE department IS NULL;
```

_Returns employees with no department assigned._

## Example Table

| id  | name   | department |
| --- | ------ | ---------- |
| 1   | Rahim  | HR         |
| 2   | Karim  | IT         |
| 3   | Nasrin |            |

## Example Output (WHERE department IS NULL)

| id  | name   | department |
| --- | ------ | ---------- |
| 3   | Nasrin |            |

## Common Mistakes

- Using `=` instead of `IN` for multiple values.
- Forgetting to check for NULL with IS NULL (not = NULL).

## Best Practices

- Use IN for lists, BETWEEN for ranges, and IS NULL for missing data.

## Practice Challenge

1. Find employees with id between 2 and 4.
2. List employees with no department.
