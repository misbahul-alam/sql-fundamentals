# Views

A view is a virtual table based on the result of a SQL query. It does not store data itself, but provides a way to simplify complex queries.

## Creating a View

```sql
CREATE VIEW hr_employees AS
SELECT * FROM employees WHERE department = 'HR';
```

_Creates a view showing only HR employees._

## Using a View

```sql
SELECT name FROM hr_employees;
```

_You can query a view just like a table._

## Updating a View

Some views can be updated directly, but not all (depends on the database and the query).

## Dropping a View

```sql
DROP VIEW hr_employees;
```

## Example Table

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 2   | Nasrin   | IT         |
| 3   | Sumon    | HR         |

## Example Output (SELECT \* FROM hr_employees)

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 3   | Sumon    | HR         |

## Common Mistakes

- Trying to update a view that is not updatable.
- Forgetting to refresh a view if the underlying tables change (in some databases).

## Best Practices

- Use views to simplify complex queries and improve security.
- Name views clearly to indicate their purpose.

## Practice Challenge

1. Create a view for employees in the IT department.
2. Drop the view after you are done using it.
