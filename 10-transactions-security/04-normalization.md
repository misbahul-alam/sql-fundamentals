# Normalization

Normalization is the process of organizing data to reduce redundancy and improve integrity.

## 1NF (First Normal Form)

- Each column contains atomic (indivisible) values
- No repeating groups or arrays
- Example: Split comma-separated values into separate rows

## 2NF (Second Normal Form)

- Meets 1NF
- Every non-key column depends on the whole primary key
- Example: Remove partial dependencies in composite keys

## 3NF (Third Normal Form)

- Meets 2NF
- No transitive dependencies (non-key columns depend only on the key)
- Example: Move columns that depend on other non-key columns to a new table

## Example

**Not Normalized:**
| id | name | address | city |
|----|-----------|-------------------|-----------|
| 1 | Misbahul | 22/B Green Road | Dhaka |

**Normalized:**
| id | name | address_id |
|----|-----------|------------|
| 1 | Misbahul | 1 |

| address_id | address         | city  |
| ---------- | --------------- | ----- |
| 1          | 22/B Green Road | Dhaka |

## Common Mistakes

- Over-normalizing (too many tables, hard to query)
- Under-normalizing (redundant data, update anomalies)

## Best Practices

- Normalize to 3NF for most applications
- Denormalize only for performance, and only when needed

## Practice Challenge

1. Identify a table in your project that is not in 1NF. How would you fix it?
2. What problems can happen if you skip normalization?
