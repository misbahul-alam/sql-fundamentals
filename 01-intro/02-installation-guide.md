---
# SQL Installation Guide

To practice SQL, you need access to a database. You can install a database locally or use an online SQL editor.

## Local Installation

### PostgreSQL
1. Download: [https://www.postgresql.org/download/](https://www.postgresql.org/download/)
2. Install and follow the setup instructions for your OS.
3. Use `psql` (CLI) or pgAdmin (GUI) to connect.

### MySQL
1. Download: [https://dev.mysql.com/downloads/installer/](https://dev.mysql.com/downloads/installer/)
2. Install and follow the setup instructions.
3. Use `mysql` (CLI) or MySQL Workbench (GUI).

### SQLite
1. Download: [https://www.sqlite.org/download.html](https://www.sqlite.org/download.html)
2. No installation required—just run the executable.

## Online SQL Editors

If you don't want to install anything, try:
- [DB Fiddle](https://www.db-fiddle.com/)
- [SQL Fiddle](http://sqlfiddle.com/)
- [SQLite Online](https://sqliteonline.com/)

## Sample Database Setup

Most examples use a simple `users` table. Create it with:
```sql
CREATE TABLE users (
	id INTEGER PRIMARY KEY,
	name VARCHAR(100),
	email VARCHAR(100),
	created_at DATE
);
```

---
