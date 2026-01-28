# TRUNCATE vs DELETE

## DELETE

- Removes rows one at a time.
- Can use a `WHERE` clause.
- Slower for large tables (logs each row deletion).
- Can be rolled back (transaction-safe).

**Think of DELETE like erasing specific lines in a notebook:**
You can choose which lines (rows) to erase, and if you make a mistake, you can undo it (if using transactions).

**When to use DELETE:**

- You want to remove only some data (not everything).
- You need to keep the table structure and settings.
- You want the option to undo (ROLLBACK) if something goes wrong.

**Warning:**
If you forget the WHERE clause, all rows will be deleted!

## TRUNCATE

- Removes all rows instantly (no `WHERE` clause allowed).
- Resets table (faster, minimal logging).
- Cannot be rolled back in some databases.
- Often resets auto-increment counters.

**Think of TRUNCATE like tearing out all the pages of a notebook at once:**
You can't pick and choose; everything is gone, and you get a fresh, empty notebook (table).

**When to use TRUNCATE:**

- You want to quickly remove all data from a table.
- You don't need to keep any old data.
- You want to reset auto-increment counters (IDs start from 1 again).

**Warning:**
TRUNCATE is very fast, but you can't use WHERE, and in some databases, you can't undo it!

**TRUNCATE vs DROP:**

- TRUNCATE removes all data but keeps the table structure.
- DROP removes the entire table (structure and data).

**Example:**

```sql
DELETE FROM employees WHERE department = 'IT';
TRUNCATE TABLE employees;
```

-- DELETE removes only IT employees, TRUNCATE removes everyone!

**Summary Table:**

| Feature         | DELETE | TRUNCATE  |
| --------------- | ------ | --------- |
| WHERE allowed   | Yes    | No        |
| Transactional   | Yes    | Sometimes |
| Speed           | Slower | Faster    |
| Resets Identity | No     | Yes       |

---

**Quick Tips:**

- Always double-check your WHERE clause with DELETE.
- Use TRUNCATE for quick cleanups, but be sure you want to erase everything.
- If you need to keep the table but start fresh, TRUNCATE is your friend.
- If you want to remove the table completely, use DROP TABLE.

**Practice Challenge:**

1. Try deleting only students named 'Misbahul' who failed a test from a `students` table.
2. Try truncating a `logs` table to clear all old logs before a new semester.
