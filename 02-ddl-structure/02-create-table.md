# Creating a Table in SQL

The `CREATE TABLE` statement is used to create a new table in a database.

## Syntax

```sql
CREATE TABLE table_name (
	column1 datatype [constraint],
	column2 datatype [constraint],
	...
);
```

## Example

```sql
CREATE TABLE students (
	id INT PRIMARY KEY,
	name VARCHAR(100),
	age INT,
	enrollment_date DATE
);
```

This command creates a `students` table with four columns.

## Additional Notes

- Table and column names should be descriptive and follow naming conventions.
- You can specify constraints (e.g., PRIMARY KEY, NOT NULL, UNIQUE) in the column definition.
- Tables can have indexes for faster searches.

## Viewing Tables

```sql
SHOW TABLES;
```

## Dropping a Table

```sql
DROP TABLE students;
```

This removes the table and all its data.
