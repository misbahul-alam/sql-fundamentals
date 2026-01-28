# CASE Statements

The `CASE` statement lets you add IF/THEN logic to your SQL queries.

## Basic Usage

```sql
SELECT name,
	CASE
		WHEN department = 'HR' THEN 'Human Resources'
		WHEN department = 'IT' THEN 'Information Tech'
		ELSE 'Other'
	END AS dept_full
FROM employees;
```

_Adds a new column with a readable department name._

## Example Table

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 2   | Nasrin   | IT         |
| 3   | Sumon    | Sales      |

## Example Output

| name     | dept_full        |
| -------- | ---------------- |
| Misbahul | Human Resources  |
| Nasrin   | Information Tech |
| Sumon    | Other            |

## Searched CASE vs Simple CASE

- Searched: `CASE WHEN condition THEN ...`
- Simple: `CASE column WHEN value THEN ...`

## Common Mistakes

- Forgetting ELSE (rows may return NULL).
- Not ending CASE with END.

## Best Practices

- Always include an ELSE for unexpected values.
- Use CASE for readable, flexible queries.

## Practice Challenge

1. Add a column that labels employees as 'High Earner' if salary > 55000, else 'Regular'.
2. Use CASE to group departments into 'Tech' (IT), 'Admin' (HR), or 'Other'.
