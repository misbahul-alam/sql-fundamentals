# Other Table Constraints

Other common constraints include:

- `UNIQUE` – Ensures all values in a column are unique
- `NOT NULL` – Ensures a column cannot have NULL values
- `CHECK` – Ensures values meet a specific condition
- `DEFAULT` – Sets a default value for a column

## Example

```sql
CREATE TABLE employees (
	emp_id INT PRIMARY KEY,
	email VARCHAR(100) UNIQUE,
	salary DECIMAL(8,2) CHECK (salary > 0),
	department VARCHAR(50) DEFAULT 'General',
	hire_date DATE NOT NULL
);
```

## More Constraint Examples

- `UNIQUE` on multiple columns:
  ```sql
  CREATE TABLE enrollments (
  		student_id INT,
  		course_id INT,
  		UNIQUE(student_id, course_id)
  );
  ```
- `CHECK` for value ranges:
  ```sql
  CREATE TABLE grades (
  		grade CHAR(2) CHECK (grade IN ('A', 'B', 'C', 'D', 'F'))
  );
  ```

## Removing Constraints

```sql
ALTER TABLE employees DROP CONSTRAINT constraint_name;
```

Constraint names are set automatically or can be named explicitly.
