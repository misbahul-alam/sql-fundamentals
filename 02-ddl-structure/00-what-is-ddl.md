## What is DDL?

DDL stands for **Data Definition Language**. It is a subset of SQL (Structured Query Language) used to define, modify, and manage the structure of database objects such as tables, schemas, indexes, and views.

### Purpose of DDL

DDL commands are used to create, alter, and remove database structures, but not the data itself. These commands help database administrators and developers set up the framework for storing and organizing data.

### Main DDL Commands

- **CREATE**: Used to create new database objects (e.g., tables, databases, indexes).
- **ALTER**: Used to modify the structure of existing database objects.
- **DROP**: Used to delete database objects.
- **TRUNCATE**: Used to remove all records from a table, but not the table itself.
- **RENAME**: Used to rename database objects.

### Examples

```sql
-- Create a new table
CREATE TABLE employees (
	id INT PRIMARY KEY,
	name VARCHAR(100),
	hire_date DATE
);

-- Alter a table to add a new column
ALTER TABLE employees ADD COLUMN salary DECIMAL(10,2);

-- Drop a table
DROP TABLE employees;
```

### Key Points

- DDL changes the structure of the database, not the data.
- DDL operations are often auto-committed, meaning changes are permanent and cannot be rolled back easily.
- DDL is essential for setting up and maintaining the database schema.

---

Continue to the next section to learn how to use the `CREATE` command in SQL.
