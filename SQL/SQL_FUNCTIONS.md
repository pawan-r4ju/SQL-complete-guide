# Functions
## 1. Aggregate Functions
### Purpose: Perform calculations on a set of values and return a single value.

- **COUNT**: Returns the number of rows.
  ```sql
  SELECT COUNT(*) FROM table_name;
  ```
- **SUM**: Returns the total sum of a numeric column.
  ```sql
  SELECT SUM(column_name) FROM table_name;
  ```
- **AVG**: Returns the average value of a numeric column.
  ```sql
  SELECT AVG(column_name) FROM table_name;
  ```
- **MAX**: Returns the highest value in a column.
  ```sql
  SELECT MAX(column_name) FROM table_name;
  ```
- **MIN**: Returns the lowest value in a column.
  ```sql
  SELECT MIN(column_name) FROM table_name;
  ```

## 2. Scalar Functions
### Purpose: Operate on a single value and return a single value.

### a. String Functions
- **UPPER**: Converts a string to uppercase.
  ```sql
  SELECT UPPER('hello');
  ```
- **LOWER**: Converts a string to lowercase.
  ```sql
  SELECT LOWER('HELLO');
  ```
- **LEFT**: Extracts a specific number of characters from the left.
  ```sql
  SELECT LEFT('Hello', 2);
  ```
- **RIGHT**: Extracts a specific number of characters from the right.
  ```sql
  SELECT RIGHT('Hello', 2);
  ```
- **LENGTH**: Returns the length of a string.
  ```sql
  SELECT LENGTH('Hello');
  ```

### b. Numeric Functions
- **ABS**: Returns the absolute value of a number.
  ```sql
  SELECT ABS(-10);
  ```
- **ROUND**: Rounds a number to a specified decimal place.
  ```sql
  SELECT ROUND(10.678, 2);
  ```
- **CEILING**: Rounds a number up to the nearest integer.
  ```sql
  SELECT CEILING(10.2);
  ```
- **FLOOR**: Rounds a number down to the nearest integer.
  ```sql
  SELECT FLOOR(10.8);
  ```

### c. Date and Time Functions (Scalar)
### Purpose: Work with date and time values.

- **NOW**: Returns the current date and time.
  ```sql
  SELECT NOW();
  ```
- **DATE**: Extracts the date part from a datetime.
  ```sql
  SELECT DATE(NOW());
  ```
- **TIME**: Extracts the time part from a datetime.
  ```sql
  SELECT TIME(NOW());
  ```
- **DATEDIFF**: Returns the difference between two dates.
  ```sql
  SELECT DATEDIFF('2025-12-31', '2025-01-01');
  ```

## Summary Table


| Function Type | Function | Purpose |
|--------------|---------|---------|
| **Aggregate** | COUNT | Counts rows |
| | SUM | Sums numeric values |
| | AVG | Calculates average |
| | MAX | Finds maximum value |
| | MIN | Finds minimum value |
| **Scalar (String)** | UPPER | Converts to uppercase |
| | LOWER | Converts to lowercase |
| | LEFT | Extracts left part of string |
| | RIGHT | Extracts right part of string |
| | LENGTH | Finds string length |
| **Scalar (Numeric)** | ABS | Returns absolute value |
| | ROUND | Rounds a number |
| | CEILING | Rounds up |
| | FLOOR | Rounds down |
| **Scalar (Date & Time)** | NOW | Current date & time |
| | DATE | Extracts date part |
| | TIME | Extracts time part |
| | DATEDIFF | Difference between dates |
