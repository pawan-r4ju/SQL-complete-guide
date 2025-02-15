# CONSTRAINTS

## PRIMARY KEY
### PURPOSE: Uniquely identifies each row in a table.
```sql
ID INT PRIMARY KEY;
```

## FOREIGN KEY
### PURPOSE: Establishes a relationship between two tables.
```sql
FOREIGN KEY (customer_id) REFERENCES customers(id);
```

## UNIQUE
### PURPOSE: Ensures all values in a column are distinct (allows NULL).
```sql
EMAIL VARCHAR(255) UNIQUE;
```

## NOT NULL
### PURPOSE: Ensures a column cannot have NULL values.
```sql
NAME VARCHAR(100) NOT NULL;
```

## CHECK
### PURPOSE: Ensures values in a column satisfy a specific condition.
```sql
PRICE DECIMAL(10, 2) CHECK (PRICE > 0);
```

## DEFAULT
### PURPOSE: Provides a default value for a column if no value is specified.
```sql
ORDER_DATE DATE DEFAULT CURRENT_DATE;
```

## SUMMARY TABLE

| CONSTRAINT | PURPOSE | EXAMPLE |
|------------|---------|---------|
| PRIMARY KEY | Uniquely identifies each row | `ID INT PRIMARY KEY;` |
| FOREIGN KEY | Establishes relationship between tables | `FOREIGN KEY (customer_id) REFERENCES customers(id);` |
| UNIQUE | Ensures unique values in column | `EMAIL VARCHAR(255) UNIQUE;` |
| NOT NULL | Ensures column cannot have NULL values | `NAME VARCHAR(100) NOT NULL;` |
| CHECK | Ensures column values meet condition | `PRICE DECIMAL(10, 2) CHECK (PRICE > 0);` |
| DEFAULT | Sets default value if none provided | `ORDER_DATE DATE DEFAULT CURRENT_DATE;` |
