## What is DQL?

DQL stands for **Data Query Language**. It is a subset of SQL focused on querying and retrieving data from database tables.

### Purpose of DQL

DQL commands are used to fetch data based on specific criteria, allowing users to analyze, filter, and sort information stored in databases.

### Main DQL Command

- **SELECT**: The primary command in DQL, used to retrieve data from one or more tables.

### Examples

```sql
-- Select all records from a table
SELECT * FROM employees;

-- Select specific columns
SELECT name, hire_date FROM employees;

-- Select records with a condition
SELECT * FROM employees WHERE hire_date > '2026-01-15';

-- Order results
SELECT * FROM employees ORDER BY name ASC;
```

### Key Points

- DQL is used only for querying data, not modifying it.
- The SELECT statement is highly flexible, supporting filtering, sorting, grouping, and joining.
- DQL is essential for data analysis and reporting.

---

Continue to the next section to learn more about the `SELECT` command and its features in SQL.
