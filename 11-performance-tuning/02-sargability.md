# SARGability

SARGable means a query can use an index efficiently (Search ARGument Able).

## Why SARGability Matters

- Non-SARGable queries are slow (can't use indexes)
- SARGable queries are fast (can use indexes)

## SARGable Example

```sql
SELECT * FROM employees WHERE name = 'Misbahul';
```

_Can use an index on department._

## Non-SARGable Example

```sql
SELECT * FROM employees WHERE UPPER(name) = 'MISBAHUL';
```

_Cannot use an index because of the function on the column._

## Tips for SARGable Queries

- Avoid functions on columns in WHERE (e.g., UPPER, CAST)
- Use simple comparisons (col = value, col > value)
- Avoid calculations on columns (col + 1 = 5)

## Common Mistakes

- Using functions or calculations on indexed columns
- Not realizing why a query is slow

## Best Practices

- Write WHERE clauses that let the database use indexes
- Test with EXPLAIN to check if indexes are used

## Practice Challenge

1. Rewrite a query to make it SARGable: `WHERE YEAR(hire_date) = 2024`
2. How would you index a table to speed up searches by last name?
