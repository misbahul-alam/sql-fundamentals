# Primary Key and Foreign Key Constraints

Constraints enforce rules for data in tables.

## Primary Key

Ensures each row is unique and not null.

```sql
CREATE TABLE users (
	user_id INT PRIMARY KEY,
	username VARCHAR(50)
);
```

## Foreign Key

Links rows between tables.

```sql
CREATE TABLE orders (
	order_id INT PRIMARY KEY,
	user_id INT,
	FOREIGN KEY (user_id) REFERENCES users(user_id)
);
```

## Additional Notes

- A table can have only one PRIMARY KEY, but it can span multiple columns (composite key).
- FOREIGN KEY constraints enforce referential integrity between tables.
- You can specify ON DELETE and ON UPDATE actions:
  ```sql
  FOREIGN KEY (user_id) REFERENCES users(user_id) ON DELETE CASCADE
  ```
  This deletes all orders for a user if the user is deleted.
