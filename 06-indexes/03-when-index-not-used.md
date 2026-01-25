# When Index Not Used

## Overview

Indexes are not always used by the database, even if they exist. This can happen for several reasons.

## Common Reasons

- The query does not filter on the indexed columns.
- The query uses functions or calculations on the indexed columns.
- The table is too small for the index to be beneficial.
- The database decides a full table scan is faster.

## Example

Suppose you have an index on `score`, but you run:

```sql
SELECT * FROM students WHERE score + 1 = 91;
```

The index on `score` will not be used because of the calculation.

## Practice

Write a query that would prevent the use of an index on the `name` column.
