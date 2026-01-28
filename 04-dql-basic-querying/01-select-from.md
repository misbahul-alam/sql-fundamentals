# SELECT & FROM

The `SELECT` statement is used to retrieve data from a database. The `FROM` clause specifies the table.

## Basic SELECT

```sql
SELECT * FROM employees;
```

_This returns all columns and all rows from the `employees` table._

## Selecting Specific Columns

```sql
SELECT name, department FROM employees;
```

_This returns only the `name` and `department` columns._

## Using Aliases

You can rename columns in your result using `AS`:

```sql
SELECT name AS employee_name, department AS dept FROM employees;
```

## Example Table

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 2   | Karim    | IT         |

## Example Output

| employee_name | dept |
| ------------- | ---- |
| Misbahul      | HR   |
| Karim         | IT   |

## Common Mistakes

- Using `SELECT *` in production (not recommended for large tables).
- Misspelling column names.

## Best Practices

- Always specify only the columns you need.
- Use aliases for clarity in your results.

## Practice Challenge

1. Select only the `name` column from the `employees` table.
2. Select all columns but rename `department` to `dept` in the result.
