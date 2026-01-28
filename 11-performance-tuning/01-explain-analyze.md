# EXPLAIN & ANALYZE

`EXPLAIN` and `ANALYZE` help you understand how SQL queries are executed and how to optimize them.

## EXPLAIN

Shows the query plan (steps the database will take).

```sql
EXPLAIN SELECT * FROM employees WHERE name = 'Misbahul';
```

_Shows if indexes are used, how tables are scanned, etc._

## ANALYZE

Runs the query and shows actual performance details (timing, rows processed).

```sql
EXPLAIN ANALYZE SELECT * FROM employees WHERE name = 'Misbahul';
```

## Example Output (simplified)

| Step       | Rows | Extra Info          |
| ---------- | ---- | ------------------- |
| Index Scan | 1    | Using index on name |
| Filter     | 1    | name = 'Misbahul'   |

## Why Use These?

- Find slow parts of queries
- See if indexes are used
- Optimize joins and filters

## Common Mistakes

- Ignoring query plans (leads to slow queries)
- Not understanding what each step means

## Best Practices

- Always check EXPLAIN for complex or slow queries
- Add indexes if full table scans are shown

## Practice Challenge

1. Run EXPLAIN on a query that joins two tables. What steps are shown?
2. Try adding an index and see if the plan changes.
