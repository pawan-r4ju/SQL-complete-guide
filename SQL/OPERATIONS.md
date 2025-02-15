## SQL Operators Explained

SQL operators are symbols or keywords that perform operations on data. They are used in queries to compare values, perform arithmetic calculations, combine conditions, and more.

### 1. Arithmetic Operators
| Operator | Description | Example |
|----------|-------------|---------|
| `+` | Addition | `SELECT 5 + 3; → 8` |
| `-` | Subtraction | `SELECT 10 - 4; → 6` |
| `*` | Multiplication | `SELECT 3 * 7; → 21` |
| `/` | Division | `SELECT 10 / 2; → 5` |
| `%` or `MOD` | Modulus (remainder) | `SELECT 10 % 3; → 1` |

### 2. Comparison Operators
| Operator | Description | Example |
|----------|-------------|---------|
| `=` | Equal to | `SELECT * FROM users WHERE age = 25;` |
| `!=` or `<>` | Not equal to | `SELECT * FROM users WHERE age != 25;` |
| `>` | Greater than | `SELECT * FROM products WHERE price > 100;` |
| `<` | Less than | `SELECT * FROM products WHERE price < 50;` |
| `>=` | Greater than or equal to | `SELECT * FROM employees WHERE salary >= 5000;` |
| `<=` | Less than or equal to | `SELECT * FROM employees WHERE salary <= 3000;` |

### 3. Logical Operators
| Operator | Description | Example |
|----------|-------------|---------|
| `AND` | Both conditions must be true | `SELECT * FROM users WHERE age > 18 AND age < 30;` |
| `OR` | At least one condition must be true | `SELECT * FROM users WHERE age = 25 OR age = 30;` |
| `NOT` | Negates a condition | `SELECT * FROM users WHERE NOT age = 25;` |

### 4. Bitwise Operators
| Operator | Description | Example |
|----------|-------------|---------|
| `&` | Bitwise AND | `SELECT 5 & 3; → 1` |
| `|` | Bitwise OR | `SELECT 5 | 3; → 7` |
| `^` | Bitwise XOR | `SELECT 5 ^ 3; → 6` |
| `~` | Bitwise NOT | `SELECT ~5; → -6` |
| `<<` | Bitwise left shift | `SELECT 5 << 1; → 10` |
| `>>` | Bitwise right shift | `SELECT 5 >> 1; → 2` |

### 5. String Operators
| Operator | Description | Example |
|----------|-------------|---------|
| `||` or `CONCAT()` | Concatenation | `SELECT 'Hello' || ' World'; → Hello World` |
| `LIKE` | Pattern matching | `SELECT * FROM users WHERE name LIKE 'A%';` |
| `ILIKE` | Case-insensitive pattern matching (PostgreSQL) | `SELECT * FROM users WHERE name ILIKE 'a%';` |

### 6. Set Operators
| Operator | Description | Example |
|----------|-------------|---------|
| `UNION` | Combines results, removes duplicates | `SELECT name FROM table1 UNION SELECT name FROM table2;` |
| `UNION ALL` | Combines results, keeps duplicates | `SELECT name FROM table1 UNION ALL SELECT name FROM table2;` |
| `INTERSECT` | Returns common rows | `SELECT name FROM table1 INTERSECT SELECT name FROM table2;` |
| `EXCEPT` | Returns rows from first query not in second | `SELECT name FROM table1 EXCEPT SELECT name FROM table2;` |

### 7. Special Operators
| Operator | Description | Example |
|----------|-------------|---------|
| `IS NULL` | Checks if a value is NULL | `SELECT * FROM users WHERE email IS NULL;` |
| `IS NOT NULL` | Checks if a value is not NULL | `SELECT * FROM users WHERE email IS NOT NULL;` |
| `IN` | Matches any value in a list | `SELECT * FROM users WHERE age IN (25, 30, 35);` |
| `BETWEEN` | Checks if a value is within a range | `SELECT * FROM products WHERE price BETWEEN 50 AND 100;` |
| `EXISTS` | Checks if a subquery returns any rows | `SELECT * FROM users WHERE EXISTS (SELECT 1 FROM orders WHERE orders.user_id = users.id);` |

### Key Notes
- **Database-Specific Variations:** Some operators (e.g., `ILIKE`) are only available in certain databases like PostgreSQL.
- **Combining Operators:** Use multiple operators in a single query for complex conditions. Use parentheses `()` to control evaluation order.
- **Performance Considerations:** Operators like `LIKE` with wildcards (%) or `NOT` can impact query performance.

Example:
```sql
SELECT * FROM employees WHERE (salary > 5000 AND age < 30) OR department = 'HR';
```
