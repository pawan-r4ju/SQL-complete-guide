# SQL Data Types Explained

In SQL, **data types** define the kind of data that can be stored in a column. Each data type has specific characteristics and is used for different purposes. Below is a brief explanation of the commonly used data types:

---

## 1. **INT (Integer)**

- **Description**: Used to store whole numbers (positive or negative) without decimals.
- **Range**: Typically ranges from `-2,147,483,648` to `2,147,483,647` (4 bytes).
- **Use Case**: Ideal for storing numerical values like IDs, ages, counts, etc.
- **Example**:
  ```sql
  CREATE TABLE employees (
      id INT,
      age INT
  );
  ```
2\. VARCHAR (Variable Character)
--------------------------------

-   Description : Stores variable-length strings (text). The maximum length is specified when defining the column.
-   Storage : Only uses as much space as needed (up to the defined limit).
-   Use Case : Suitable for storing names, addresses, or any text where the length may vary.
-   Example :
 ```sql
  CREATE TABLE users (
    username VARCHAR(50),
    email VARCHAR(100)
);
  ```
3\. DATETIME
------------

-   Description : Stores both date and time together in the format `YYYY-MM-DD HH:MM:SS`.
-   Range : Typically from `'1000-01-01 00:00:00'` to `'9999-12-31 23:59:59'`.
-   Use Case : Used for timestamps, logging events, or scheduling tasks.
-   Example :
 ```sql
  CREATE TABLE events (
    event_name VARCHAR(100),
    event_time DATETIME
);
  ```
4\. STRING
----------

-   Description : In SQL, `STRING` is not a standard data type. Instead, it is often synonymous with `VARCHAR` or `TEXT` in some database systems (e.g., SQLite).
-   Use Case : If supported, it is used for storing textual data.
-   Note : Use `VARCHAR` or `TEXT` in most SQL databases.

5\. CHAR (Fixed-Length Character)
---------------------------------

-   Description : Stores fixed-length strings. If the input is shorter than the defined length, it pads the remaining space with spaces.
-   Storage : Always uses the defined amount of space, regardless of the actual data length.
-   Use Case : Best for fixed-length data like country codes (`US`, `IN`) or status flags (`Y`, `N`).
-   Example :
 ```sql
  CREATE TABLE countries (
    country_code CHAR(2)
);
  ```

6\. BOOLEAN
-----------

-   Description : Stores true/false values. Some databases (e.g., MySQL) internally store `BOOLEAN` as `TINYINT(1)` where `1` represents `TRUE` and `0` represents `FALSE`.
-   Use Case : Used for flags or binary conditions (e.g., `is_active`, `has_permission`).
-   Example:
 ```sql
  CREATE TABLE tasks (
    task_name VARCHAR(100),
    is_completed BOOLEAN
);
  ```

7\. JSON
--------

-   Description : Stores JSON (JavaScript Object Notation) data, which is a semi-structured format for representing key-value pairs or arrays.
-   Use Case : Useful for storing flexible or hierarchical data like user preferences, configurations, or logs.
-   Example :
```sql
  CREATE TABLE user_preferences (
    user_id INT,
    preferences JSON
);
  ```
## Summary Table

| Data Type  | Description |
|------------|------------------------------------------------|
| **INT**    | Whole numbers (no decimals). IDs, ages, counts. |
| **VARCHAR** | Variable-length text. Names, addresses, emails. |
| **DATETIME** | Date and time together (YYYY-MM-DD HH:MM:SS). Timestamps, event schedules. |
| **STRING**  | Not a standard SQL type; often equivalent to VARCHAR or TEXT. Textual data (if supported). |
| **CHAR**    | Fixed-length text (padded with spaces if shorter than defined length). Country codes, status flags. |
| **BOOLEAN** | True/false values (often stored as 1/0 in some databases). Flags, binary conditions. |
| **JSON**    | Semi-structured data in key-value pairs or arrays. User preferences, configurations. |