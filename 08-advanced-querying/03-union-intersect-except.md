# UNION, INTERSECT, EXCEPT

Set operations combine results from two or more queries.

## UNION

Combines results from two queries, removing duplicates.

```sql
SELECT name FROM employees
UNION
SELECT name FROM managers;
```

## UNION ALL

Combines results and keeps duplicates.

```sql
SELECT name FROM employees
UNION ALL
SELECT name FROM managers;
```

## INTERSECT

Returns only rows present in both queries.

```sql
SELECT name FROM employees
INTERSECT
SELECT name FROM managers;
```

## EXCEPT (or MINUS)

Returns rows from the first query not in the second.

```sql
SELECT name FROM employees
EXCEPT
SELECT name FROM managers;
```

## Example Tables

**employees**
| name |
|-----------|
| Misbahul |
| Nasrin |
| Sumon |

**managers**
| name |
|-----------|
| Misbahul |
| Karim |

## Example Output (UNION)

| name     |
| -------- |
| Misbahul |
| Nasrin   |
| Sumon    |
| Karim    |

## Common Mistakes

- Number and order of columns must match in both queries.
- Using INTERSECT/EXCEPT in databases that don't support them.

## Best Practices

- Use UNION ALL for performance if duplicates are OK.
- Always check column compatibility.

## Practice Challenge

1. List all unique names from employees and managers.
2. Find names that are employees but not managers.
