# Stored Procedures

A stored procedure is a saved set of SQL statements you can run repeatedly.

## Creating a Stored Procedure

```sql
CREATE PROCEDURE add_employee(
	IN emp_name VARCHAR(50),
	IN emp_dept VARCHAR(50)
)
BEGIN
	INSERT INTO employees(name, department) VALUES (emp_name, emp_dept);
END;
```

_Creates a procedure to add a new employee._

## Calling a Stored Procedure

```sql
CALL add_employee('David', 'Sales');
```

## Why Use Stored Procedures?

- Encapsulate business logic
- Reuse code
- Improve security (limit direct table access)

## Example Table

| id  | name     | department |
| --- | -------- | ---------- |
| 1   | Misbahul | HR         |
| 2   | Nasrin   | IT         |

## Common Mistakes

- Forgetting to use correct parameter types
- Not handling errors inside the procedure

## Best Practices

- Use clear, descriptive names
- Document what each procedure does

## Practice Challenge

1. Write a procedure to update an employee's department.
2. Call your procedure to move 'Nasrin' to 'Sales'.
