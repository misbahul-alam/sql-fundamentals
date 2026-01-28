# CROSS JOIN

A `CROSS JOIN` returns every combination of rows from two tables (Cartesian product).

## Syntax

```sql
SELECT *
FROM employees
CROSS JOIN departments;
```

## Example Tables

**employees**
| id | name |
|----|-----------|
| 1 | Misbahul |
| 2 | Nasrin |

**departments**
| id | department_name |
|----|-----------------|
| 1 | HR |
| 2 | IT |

## Example Output

| name     | department_name |
| -------- | --------------- |
| Misbahul | HR              |
| Misbahul | IT              |
| Nasrin   | HR              |
| Nasrin   | IT              |

## Visual Diagram

Each row from employees is paired with every row from departments.

## Common Mistakes

- Using CROSS JOIN accidentally (can create huge result sets).
- Not understanding the size of the result: rowsA \* rowsB.

## Best Practices

- Use CROSS JOIN only when you really need all combinations.
- Be careful with large tables.

## Practice Challenge

1. Write a query to show all possible employee-department pairs.
2. What happens if one table has 100 rows and the other has 50?
