# String Data Types in SQL

String data types are used to store text. Common types include:

- `CHAR(n)` – Fixed-length string
- `VARCHAR(n)` – Variable-length string
- `TEXT` – Large text data

## Example

```sql
CREATE TABLE books (
	title VARCHAR(200),
	author CHAR(100),
	description TEXT
);
```

This table stores book titles, authors, and descriptions as strings.

## More String Types

- `NVARCHAR(n)` – Unicode variable-length string (for international text)
- `ENUM` – Set of predefined values

## Choosing String Types

- Use `CHAR` for fixed-length codes, `VARCHAR` for variable text, and `TEXT` for large content.
- `ENUM` is useful for columns with a limited set of values.

## Example: ENUM

```sql
CREATE TABLE shirts (
	size ENUM('S', 'M', 'L', 'XL'),
	color VARCHAR(30)
);
```

This table restricts `size` to specific values.
