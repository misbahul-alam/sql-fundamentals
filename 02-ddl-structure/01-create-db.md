# Creating a Database in SQL

The `CREATE DATABASE` statement is used to create a new database in SQL.

## Syntax

```sql
CREATE DATABASE database_name;
```

## Example

```sql
CREATE DATABASE school;
```

This command creates a new database named `school`.

## Additional Notes

- Database names should be unique within the server.
- You may need specific privileges to create a database.
- Some systems allow you to specify options like character set and collation:
  ```sql
  CREATE DATABASE school CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
  ```

## Listing Databases

```sql
SHOW DATABASES;
```

## Dropping a Database

```sql
DROP DATABASE school;
```

Be careful: this deletes the database and all its data.
