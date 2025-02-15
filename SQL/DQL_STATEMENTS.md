# SQL DQL (Data Query Language) Statements

DQL (Data Query Language) is used to retrieve data from databases using queries.

### 1. SELECT
**Purpose:** Retrieves data from one or more tables.

**Syntax:**
```sql
SELECT column1, column2 FROM table_name;
```

### 2. FROM
**Purpose:** Specifies the table from which to retrieve data.

**Syntax:**
```sql
SELECT * FROM table_name;
```

### 3. WHERE (Using Operators and Functions)
**Purpose:** Filters records based on a condition.

**Syntax:**
```sql
SELECT * FROM table_name WHERE condition;
```

### 4. ORDER BY
**Purpose:** Sorts the result set.

**Syntax:**
```sql
SELECT * FROM table_name ORDER BY column_name ASC/DESC;
```

### 5. GROUP BY
**Purpose:** Groups rows that have the same values in specified columns.

**Syntax:**
```sql
SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name;
```

### 6. HAVING
**Purpose:** Filters records after grouping.

**Syntax:**
```sql
SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name HAVING COUNT(*) > value;
```

### 7. LIMIT
**Purpose:** Limits the number of rows returned.

**Syntax:**
```sql
SELECT * FROM table_name LIMIT number;
```

### 8. JOINs
**Purpose:** Combines rows from multiple tables.

#### a. INNER JOIN
**Returns matching records from both tables.**
```sql
SELECT * FROM table1 INNER JOIN table2 ON table1.id = table2.id;
```

#### b. LEFT JOIN (OUTER)
**Returns all records from the left table and matching records from the right table.**
```sql
SELECT * FROM table1 LEFT JOIN table2 ON table1.id = table2.id;
```

#### c. RIGHT JOIN (OUTER)
**Returns all records from the right table and matching records from the left table.**
```sql
SELECT * FROM table1 RIGHT JOIN table2 ON table1.id = table2.id;
```

#### d. FULL JOIN (OUTER)
**Returns all records from both tables.**
```sql
SELECT * FROM table1 FULL JOIN table2 ON table1.id = table2.id;
```

#### e. SELF JOIN
**Joins a table with itself.**
```sql
SELECT a.column_name, b.column_name FROM table_name a, table_name b WHERE condition;
```

#### f. CROSS JOIN
**Returns the Cartesian product of both tables.**
```sql
SELECT * FROM table1 CROSS JOIN table2;
```

## Summary Table

| DQL Statement | Purpose |
|--------------|---------|
| **SELECT** | Retrieves data |
| **FROM** | Specifies table |
| **WHERE** | Filters records |
| **ORDER BY** | Sorts results |
| **GROUP BY** | Groups records |
| **HAVING** | Filters grouped records |
| **LIMIT** | Restricts result size |
| **INNER JOIN** | Matches records in both tables |
| **LEFT JOIN (OUTER)** | Matches records in left table with right table |
| **RIGHT JOIN (OUTER)** | Matches records in right table with left table |
| **FULL JOIN (OUTER)** | Matches all records from both tables |
| **SELF JOIN** | Joins a table to itself |
| **CROSS JOIN** | Returns Cartesian product |
