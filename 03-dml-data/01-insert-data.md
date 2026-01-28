# INSERT Data

## Single Row Insert

```sql
INSERT INTO employees (id, name, department)
VALUES (1, 'Misbahul', 'HR');
```

_This command adds one new row to the `employees` table. You must provide a value for each column listed._

### Example Table Before

| id  | name | department |
| --- | ---- | ---------- |
|     |      |            |

### Example Table After

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |

## Bulk Insert

```sql
INSERT INTO employees (id, name, department)
VALUES
  (2, 'Nasrin', 'IT'),
  (3, 'Karim', 'Finance');
```

_Bulk insert lets you add several rows at once, which is faster and uses less code._

### Example Table After Bulk Insert

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 2   | Nasrin   | IT         |
| 3   | Karim    | Finance    |

## Insert Default Values

If a column has a default value, you can skip it:

```sql
INSERT INTO employees (name, department)
VALUES ('Sumon', 'Sales');
```

_If `id` is auto-increment, it will be filled automatically._

## Common Mistakes

- **Forgetting column names:**
  - If you skip column names, the order must match the table exactly.
- **Wrong data types:**
  - Make sure values match the column types (e.g., don't put text in a number column).
- **Duplicate primary key:**
  - Inserting a row with an existing `id` will cause an error.

## Best Practices

- Always specify column names for clarity and safety.
- Use bulk insert for adding many rows.
- Check for required (NOT NULL) columns.

## Practice Challenge

1. Insert yourself as a new employee in the table.
2. Try inserting a row without specifying the department. What happens?

**Notes:**

- Always specify column names for clarity.
- Bulk inserts are more efficient for adding multiple rows.
