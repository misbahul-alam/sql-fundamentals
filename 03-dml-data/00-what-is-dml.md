## What is DML?

DML stands for **Data Manipulation Language**. It is a subset of SQL used to manage and manipulate data stored within database tables.

### Purpose of DML

DML commands allow users to insert, update, delete, and retrieve data from tables. Unlike DDL, which deals with the structure of the database, DML focuses on the data itself.

### Main DML Commands

- **INSERT**: Adds new records (rows) to a table.
- **UPDATE**: Modifies existing records in a table.
- **DELETE**: Removes records from a table.
- **SELECT**: Retrieves data from one or more tables (sometimes considered part of DQL, but often included in DML).

### Examples

```sql
-- Insert a new record
INSERT INTO employees (id, name, hire_date) VALUES (1, 'Misbahul', '2026-01-15');

-- Update a record
UPDATE employees SET name = 'Misbahul' WHERE id = 1;

-- Delete a record
DELETE FROM employees WHERE id = 1;

-- Select records
SELECT * FROM employees;
```

### Key Points

- DML commands affect the data within tables, not the structure.
- DML operations can be rolled back or committed using transactions.
- DML is essential for day-to-day data management in databases.

---

Continue to the next section to learn how to use the `INSERT` command in SQL.
