# SQL DDL (Data Definition Language) Statements

DDL (Data Definition Language) is used to define and manage database structures, including tables, schemas, and indexes.

### 1. CREATE
**Purpose:** Creates a new table, database, or other database objects.

**Syntax:**
```sql
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    ...
);
```

**Example:** Create an "employees" table:
```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    department VARCHAR(50)
);
```

### 2. ALTER
**Purpose:** Modifies an existing table structure by adding, modifying, or deleting columns.

**Syntax:**
```sql
ALTER TABLE table_name ADD column_name datatype;
```

**Example:** Add an "email" column to the "employees" table:
```sql
ALTER TABLE employees ADD COLUMN email VARCHAR(255);
```

### 3. DROP
**Purpose:** Deletes an entire table, database, or other database objects.

**Syntax:**
```sql
DROP TABLE table_name;
```

**Example:** Drop the "employees" table:
```sql
DROP TABLE employees;
```

### 4. TRUNCATE
**Purpose:** Removes all records from a table but keeps the structure intact.

**Syntax:**
```sql
TRUNCATE TABLE table_name;
```

**Example:** Remove all records from the "employees" table:
```sql
TRUNCATE TABLE employees;
```

### 5. RENAME
**Purpose:** Renames an existing table or column.

**Syntax:**
```sql
RENAME TABLE old_table_name TO new_table_name;
```

**Example:** Rename the "employees" table to "staff":
```sql
RENAME TABLE employees TO staff;
```

## Summary Table

| DDL Statement | Purpose | Example |
|--------------|---------|---------|
| **CREATE** | Create a new table or database object | `CREATE TABLE employees (id INT, name VARCHAR(100));` |
| **ALTER** | Modify an existing table | `ALTER TABLE employees ADD COLUMN email VARCHAR(255);` |
| **DROP** | Delete a table or database object | `DROP TABLE employees;` |
| **TRUNCATE** | Remove all rows from a table | `TRUNCATE TABLE employees;` |
| **RENAME** | Rename a table or column | `RENAME TABLE employees TO staff;` |