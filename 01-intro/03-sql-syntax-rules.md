---
# SQL Syntax Rules

Understanding SQL syntax is crucial for writing correct and efficient queries. Here are the fundamental rules and conventions:

## 1. SQL Statements End with a Semicolon
```sql
SELECT * FROM users;
```

## 2. Case Insensitivity
SQL keywords are case-insensitive. These are equivalent:
```sql
SELECT name FROM users;
select name from users;
```

## 3. Whitespace and Formatting
Whitespace (spaces, tabs, newlines) is ignored, so format queries for readability.

## 4. Comments
- Single-line: `-- comment`
- Multi-line: `/* comment */`

## 5. Identifiers
- Table and column names can be quoted with double quotes (ANSI SQL) or backticks (MySQL):
```sql
SELECT "user"."name" FROM "user";
```

## 6. Common Clauses
- `SELECT`, `FROM`, `WHERE`, `ORDER BY`, `GROUP BY`, `HAVING`, `LIMIT`

## 7. Example Query
```sql
SELECT name, email FROM users WHERE created_at > '2026-01-01' ORDER BY name ASC;
```

## 8. Best Practices
- Use uppercase for SQL keywords
- Use lowercase for table/column names
- Indent nested queries

---
