# Numeric Data Types in SQL

Numeric data types are used to store numbers. Common types include:

- `INT` – Integer numbers
- `FLOAT` – Floating-point numbers
- `DECIMAL(p, s)` – Fixed-point numbers

## Example

```sql
CREATE TABLE products (
	product_id INT,
	price DECIMAL(10, 2),
	rating FLOAT
);
```

This table stores product IDs, prices, and ratings using numeric types.

## More Numeric Types

- `SMALLINT`, `BIGINT` – Smaller or larger integer ranges
- `DOUBLE` – Double-precision floating-point
- `SERIAL` – Auto-incrementing integer (varies by SQL dialect)

## Choosing Numeric Types

- Use `INT` for whole numbers, `DECIMAL` for precise values (e.g., money), and `FLOAT`/`DOUBLE` for scientific data.
- `DECIMAL` is preferred for financial calculations to avoid rounding errors.

## Example: Auto-Increment

```sql
CREATE TABLE invoices (
	invoice_id INT AUTO_INCREMENT PRIMARY KEY,
	amount DECIMAL(10,2)
);
```

This table uses an auto-incrementing primary key.
