## SQL DML (Data Manipulation Language) Statements

DML (Data Manipulation Language) is used to interact with data in a database, including retrieving, inserting, updating, and deleting records.

### 1. SELECT
**Purpose:** Retrieves data from one or more tables.

**Syntax:**
```sql
SELECT column1, column2, ... FROM table_name WHERE condition;
```

**Example:** Retrieve all employees in the "HR" department:
```sql
SELECT * FROM employees WHERE department = 'HR';
```

### 2. INSERT
**Purpose:** Adds new rows of data into a table.

**Syntax:**
```sql
INSERT INTO table_name (column1, column2, ...) VALUES (value1, value2, ...);
```

**Example:** Insert a new employee into the "employees" table:
```sql
INSERT INTO employees (name, age, department) VALUES ('Alice Johnson', 30, 'Marketing');
```

### 3. UPDATE
**Purpose:** Modifies existing data in a table.

**Syntax:**
```sql
UPDATE table_name SET column1 = value1, column2 = value2, ... WHERE condition;
```

**Example:** Update the salary of an employee with `id = 5`:
```sql
UPDATE employees SET salary = 70000 WHERE id = 5;
```

### 4. DELETE
**Purpose:** Removes rows from a table.

**Syntax:**
```sql
DELETE FROM table_name WHERE condition;
```

**Example:** Delete an employee with `id = 3`:
```sql
DELETE FROM employees WHERE id = 3;
```

### 5. MERGE (or UPSERT)
**Purpose:** Combines `INSERT` and `UPDATE` operations. If a record exists, it updates it; otherwise, it inserts a new record.

**Syntax (Example in PostgreSQL-like syntax):**
```sql
MERGE INTO employees AS target
USING new_employees AS source
ON target.id = source.id
WHEN MATCHED THEN
    UPDATE SET name = source.name, age = source.age
WHEN NOT MATCHED THEN
    INSERT (id, name, age) VALUES (source.id, source.name, source.age);
```

**Example:** Synchronize the "employees" table with new employee data from another table.

### 6. CALL
**Purpose:** Executes a stored procedure.

**Syntax:**
```sql
CALL procedure_name (parameter1, parameter2, ...);
```

**Example:** Call a stored procedure named `GetEmployeeSalary`:
```sql
CALL GetEmployeeSalary(5);
```

### 7. LOCK
**Purpose:** Locks a table or row to prevent other transactions from modifying it.

**Syntax:**
```sql
LOCK TABLE table_name IN mode;
```

**Example:** Lock the "employees" table in exclusive mode:
```sql
LOCK TABLE employees IN EXCLUSIVE MODE;
```

## Summary Table

| DML Statement | Purpose | Example |
|--------------|---------|---------|
| **SELECT** | Retrieve data from a table | `SELECT name, age FROM employees WHERE age > 30;` |
| **INSERT** | Add new rows to a table | `INSERT INTO employees (name, age) VALUES ('John Doe', 28);` |
| **UPDATE** | Modify existing rows in a table | `UPDATE employees SET salary = 60000 WHERE id = 1;` |
| **DELETE** | Remove rows from a table | `DELETE FROM employees WHERE id = 1;` |
| **MERGE** | Combine `INSERT` and `UPDATE` | `MERGE INTO employees USING new_employees ON employees.id = new_employees.id;` |
| **CALL** | Execute a stored procedure | `CALL GetEmployeeSalary(5);` |
| **LOCK** | Lock a table or row | `LOCK TABLE employees IN EXCLUSIVE MODE;` |
