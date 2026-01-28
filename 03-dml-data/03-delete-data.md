# DELETE Data

## Delete a Single Row

```sql
DELETE FROM employees
WHERE id = 2;
```

_This command removes the employee with id 2 from the table._

### Example Table Before

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 2   | Karim    | IT         |
| 3   | Nasrin   | Finance    |

### Example Table After

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 3   | Nasrin   | Finance    |

## Delete Multiple Rows

```sql
DELETE FROM employees
WHERE department = 'General';
```

_This command removes all employees in the General department._

### Example Table Before

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | General    |
| 2   | Nasrin   | General    |
| 3   | Karim    | IT         |

### Example Table After

| id  | name  | department |
| --- | ----- | ---------- |
| 3   | Karim | IT         |

## Delete All Rows

If you omit the WHERE clause, all rows will be deleted:

```sql
DELETE FROM employees;
```

**Warning:** This will empty the entire table but keep its structure.

## Common Mistakes

- **Forgetting the WHERE clause:**
  - Deletes all rows, not just the intended ones.
- **Wrong column in WHERE:**
  - Double-check your condition.

## Best Practices

- Always double-check your WHERE clause.
- Test your DELETE with a SELECT first:
  - `SELECT * FROM employees WHERE department = 'General';`
- Make a backup before large deletes.

## Practice Challenge

1. Delete all employees in the IT department.
2. Try deleting all rows from the table. What remains?

**Notes:**

- Use `WHERE` to target specific rows. Omitting it deletes all rows.
