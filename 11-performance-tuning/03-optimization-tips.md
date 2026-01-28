# Optimization Tips

Optimizing SQL queries makes your database faster and more efficient.

## Indexes

- Add indexes to columns used in WHERE, JOIN, and ORDER BY
- Don't over-index (slows down writes)

## Query Design

- Select only the columns you need (avoid SELECT \*)
- Use WHERE to filter early
- Avoid subqueries if a JOIN is faster

## Joins

- Use INNER JOIN when possible (faster than OUTER JOIN)
- Join on indexed columns

## Aggregations

- Use GROUP BY only when needed
- Filter with WHERE before GROUP BY

## Pagination

- Use LIMIT/OFFSET for paging, but be careful with large offsets (can be slow)

## Example

```sql
SELECT name FROM employees WHERE name = 'Misbahul' ORDER BY name LIMIT 10;
```

## Common Mistakes

- Using SELECT \* in production
- Not using indexes
- Filtering after joining (filter before join if possible)

## Best Practices

- Always test query speed with EXPLAIN
- Regularly review and tune indexes

## Practice Challenge

1. Optimize a query that joins three tables and filters by date.
2. What happens if you add too many indexes?
