# COMMIT & ROLLBACK

Transactions let you group multiple SQL statements into a single unit of work.

## COMMIT

- Saves all changes made in the transaction.
- Example:

```sql
BEGIN;
UPDATE accounts SET balance = balance - 100 WHERE name = 'Misbahul';
UPDATE accounts SET balance = balance + 100 WHERE name = 'Nasrin';
COMMIT;
```

_Both updates are saved together._

## ROLLBACK

- Undoes all changes made in the transaction.
- Example:

```sql
BEGIN;
UPDATE accounts SET balance = balance - 100 WHERE name = 'Misbahul';
-- Oops, something went wrong!
ROLLBACK;
```

_No changes are saved._

## Why Use Transactions?

- Prevents partial updates
- Ensures data integrity

## Common Mistakes

- Forgetting to COMMIT (changes are lost)
- Not using transactions for related changes

## Best Practices

- Always use transactions for multi-step changes
- Test ROLLBACK to ensure it works as expected

## Practice Challenge

1. Write a transaction to transfer money between two accounts. Try both COMMIT and ROLLBACK.
2. What happens if you forget to COMMIT?
