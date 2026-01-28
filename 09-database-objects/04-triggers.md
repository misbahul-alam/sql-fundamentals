# Triggers

A trigger is a special procedure that runs automatically when data changes in a table.

## Why Use Triggers?

- Enforce business rules
- Audit changes
- Automate tasks (e.g., update timestamps)

## Creating a Trigger

```sql
CREATE TRIGGER before_insert_employee
BEFORE INSERT ON employees
FOR EACH ROW
SET NEW.created_at = NOW();
```

_Automatically sets the created_at timestamp before inserting a new employee._

## Example Table

| id  | name     | department | created_at          |
| --- | -------- | ---------- | ------------------- |
| 1   | Misbahul | HR         | 2024-01-01 09:00:00 |

## Common Mistakes

- Creating triggers that cause infinite loops
- Not testing triggers thoroughly

## Best Practices

- Keep triggers simple and focused
- Document what each trigger does

## Practice Challenge

1. Write a trigger to log deletions from the employees table. Test it by deleting an employee named Misbahul.
