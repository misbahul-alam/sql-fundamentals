# UPDATE Data

## Update a Single Row

```sql
UPDATE employees
SET department = 'Marketing'
WHERE id = 1;
```

_This command changes the department of the employee with id 1 to 'Marketing'._

### Example Table Before

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 2   | Karim    | IT         |

### Example Table After

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | Marketing  |
| 2   | Karim    | IT         |

## Update Multiple Rows

```sql
UPDATE employees
SET department = 'General'
WHERE department = 'HR';
```

_This command changes all employees in the HR department to the General department._

### Example Table Before

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 2   | Nasrin   | HR         |
| 3   | Karim    | IT         |

### Example Table After

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | General    |
| 2   | Nasrin   | General    |
| 3   | Karim    | IT         |

## Update All Rows

If you omit the WHERE clause, all rows will be updated:

```sql
UPDATE employees
SET department = 'Unknown';
```

**Warning:** This will change every row in the table!

## Common Mistakes

- **Forgetting the WHERE clause:**
  - Updates all rows, not just the intended ones.
- **Wrong column names:**
  - Double-check spelling and case.
- **Data type mismatch:**
  - Make sure the new value matches the column type.

## Best Practices

- Always use a WHERE clause unless you really want to update everything.
- Test your UPDATE with a SELECT first:
  - `SELECT * FROM employees WHERE department = 'HR';`
- Make a backup before large updates.

## Practice Challenge

1. Change the department of 'Bob' to 'Support'.
2. Try updating all employees to have the same department. What happens?

**Notes:**

- Always use a `WHERE` clause to avoid updating all rows unintentionally.
