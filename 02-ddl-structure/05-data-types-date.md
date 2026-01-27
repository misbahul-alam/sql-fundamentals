# Date and Time Data Types in SQL

Date and time types are used to store dates, times, and timestamps.

- `DATE` – Stores date (YYYY-MM-DD)
- `TIME` – Stores time (HH:MM:SS)
- `DATETIME` or `TIMESTAMP` – Stores date and time

## Example

```sql
CREATE TABLE events (
	event_id INT,
	event_date DATE,
	event_time TIME,
	created_at TIMESTAMP
);
```

This table stores event dates and times.

## More Date/Time Types

- `YEAR` – Stores a year value
- `INTERVAL` – Represents a time span (in some SQL dialects)

## Example: Default Timestamp

```sql
CREATE TABLE logs (
	log_id INT PRIMARY KEY,
	message TEXT,
	created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

This table automatically records the creation time for each log entry.

## Date/Time Functions

```sql
SELECT NOW();      -- Current date and time
SELECT CURDATE();  -- Current date
SELECT CURTIME();  -- Current time
```
