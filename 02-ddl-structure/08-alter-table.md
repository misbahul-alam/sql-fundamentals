# ALTER TABLE Statement

The `ALTER TABLE` statement is used to modify an existing table structure.

## Add a Column

```sql
ALTER TABLE students ADD COLUMN email VARCHAR(100);
```

## Modify a Column

```sql
ALTER TABLE students MODIFY COLUMN name VARCHAR(150);
```

## Drop a Column

```sql
ALTER TABLE students DROP COLUMN age;
```

## Add a Constraint

```sql
ALTER TABLE students ADD CONSTRAINT unique_email UNIQUE (email);
```

These commands allow you to change the structure of a table after it has been created.

## Rename a Table

```sql
ALTER TABLE students RENAME TO learners;
```

## Rename a Column

```sql
ALTER TABLE students RENAME COLUMN name TO full_name;
```

## Change Column Data Type

```sql
ALTER TABLE students ALTER COLUMN age TYPE SMALLINT;
```

## Drop a Constraint

```sql
ALTER TABLE students DROP CONSTRAINT unique_email;
```

## Notes

- ALTER TABLE syntax can vary between SQL dialects (MySQL, PostgreSQL, SQL Server, etc.).
