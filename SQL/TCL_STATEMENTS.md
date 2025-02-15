# SQL TCL (Transaction Control Language) Statements

TCL (Transaction Control Language) is used to manage transactions in a database to ensure data integrity and consistency.

### 1. COMMIT
**Purpose:** Saves all changes made in the current transaction permanently.

**Syntax:**
```sql
COMMIT;
```

### 2. ROLLBACK
**Purpose:** Reverts all changes made in the current transaction.

**Syntax:**
```sql
ROLLBACK;
```

### 3. SAVEPOINT
**Purpose:** Creates a savepoint within a transaction to allow partial rollbacks.

**Syntax:**
```sql
SAVEPOINT savepoint_name;
```

### 4. SET TRANSACTION
**Purpose:** Defines the properties of a transaction such as isolation level.

**Syntax:**
```sql
SET TRANSACTION [READ WRITE | READ ONLY];
```

### 5. SET CONSTRAINT
**Purpose:** Controls the enforcement of constraints in a transaction.

**Syntax:**
```sql
SET CONSTRAINTS constraint_name IMMEDIATE | DEFERRED;
```

## Summary Table

| TCL Statement | Purpose |
|--------------|---------|
| **COMMIT** | Saves changes permanently |
| **ROLLBACK** | Reverts changes |
| **SAVEPOINT** | Creates a rollback point |
| **SET TRANSACTION** | Defines transaction properties |
| **SET CONSTRAINT** | Controls constraint enforcement |
