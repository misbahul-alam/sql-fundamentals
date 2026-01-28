# LIMIT & OFFSET

The `LIMIT` clause restricts the number of rows returned. `OFFSET` skips a number of rows before starting to return rows.

## Basic LIMIT

```sql
SELECT * FROM employees
LIMIT 2;
```

_Returns only the first 2 rows._

## LIMIT with OFFSET

```sql
SELECT * FROM employees
LIMIT 2 OFFSET 1;
```

_Skips the first row, then returns the next 2 rows._

## Example Table

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 2   | Nasrin   | IT         |
| 3   | Sumon    | HR         |
| 4   | Karim    | Sales      |

## Example Output (LIMIT 2 OFFSET 1)

| id  | name   | department |
| --- | ------ | ---------- |
| 2   | Nasrin | IT         |
| 3   | Sumon  | HR         |

## Common Mistakes

- Forgetting that OFFSET starts counting from 0 (the first row is OFFSET 0).
- Using LIMIT without ORDER BY (results may be unpredictable).

## Best Practices

- Always use ORDER BY with LIMIT/OFFSET for consistent results.
- Use LIMIT/OFFSET for pagination in web apps.

## Practice Challenge

1. Show the third and fourth employees in the table.
2. Show only the first employee in alphabetical order by name.
