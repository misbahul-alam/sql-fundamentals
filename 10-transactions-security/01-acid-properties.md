# ACID Properties

ACID is a set of properties that ensure reliable database transactions:

## Atomicity

- All steps in a transaction succeed or none do (all-or-nothing).
- Example: Transferring money between accounts—both debit and credit must happen, or neither. For example, if Misbahul sends money to Nasrin, both accounts must update together.

## Consistency

- A transaction brings the database from one valid state to another.
- Example: After a transfer from Misbahul to Nasrin, total money in the system remains the same.

## Isolation

- Transactions do not interfere with each other.
- Example: If Misbahul and Karim transfer money at the same time, their changes won’t mix up.

## Durability

- Once a transaction is committed, it stays even if the system crashes.
- Example: After Misbahul sees "Transfer Complete," the change is permanent.

## Why ACID Matters

- Prevents data loss and corruption
- Ensures trust in database operations

## Common Mistakes

- Not using transactions for related changes
- Assuming all databases enforce ACID strictly (some NoSQL do not)

## Best Practices

- Always use transactions for critical operations
- Test for failures and rollbacks

## Practice Challenge

1. Describe a real-life scenario where atomicity is important.
2. What could go wrong if isolation is not enforced?
