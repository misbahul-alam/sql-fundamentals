# Wildcards & LIKE

The `LIKE` operator is used for pattern matching in text columns.

## % Wildcard

`%` matches any sequence of characters (including none).

```sql
SELECT * FROM employees
WHERE name LIKE 'A%';
```

_Finds names starting with 'A' (e.g., Alice)._

## \_ Wildcard

`_` matches a single character.

```sql
SELECT * FROM employees
WHERE name LIKE '_a%';
```

_Finds names where the second letter is 'a' (e.g., Carol)._

## Example Table

| id  | name   | department |
| --- | ------ | ---------- |
| 1   | Rahim  | HR         |
| 2   | Karim  | IT         |
| 3   | Nasrin | HR         |

## Example Output (WHERE name LIKE 'A%')

| id  | name  | department |
| --- | ----- | ---------- |
| 1   | Rahim | HR         |

## Common Mistakes

- Forgetting to use quotes around patterns.
- Using = instead of LIKE for patterns.

## Best Practices

- Use % at the start/end for flexible matching.
- Combine with NOT for exclusions: `WHERE name NOT LIKE 'A%'`.

## Practice Challenge

1. Find all employees whose names end with 'b'.
2. List employees whose names have exactly 5 letters.
