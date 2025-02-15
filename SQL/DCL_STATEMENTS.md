# SQL DCL (Data Control Language) Statements

DCL (Data Control Language) is used to manage access privileges and security permissions in a database.

### 1. GRANT
**Purpose:** Assigns specific privileges to users or roles.

**Syntax:**
```sql
GRANT privilege_name ON object_name TO user_name;
```

**Example:** Grant SELECT permission on the employees table to a user:
```sql
GRANT SELECT ON employees TO 'john';
```

### 2. REVOKE
**Purpose:** Removes previously granted privileges from users or roles.

**Syntax:**
```sql
REVOKE privilege_name ON object_name FROM user_name;
```

**Example:** Revoke SELECT permission on the employees table from a user:
```sql
REVOKE SELECT ON employees FROM 'john';
```

## Summary Table

| DCL Statement | Purpose | Example |
|--------------|---------|---------|
| **GRANT** | Assign privileges to users or roles | `GRANT SELECT ON employees TO 'john';` |
| **REVOKE** | Remove privileges from users or roles | `REVOKE SELECT ON employees FROM 'john';` |
