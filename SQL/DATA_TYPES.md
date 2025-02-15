# DATA TYPES

## NUMERIC DATA TYPES
### Purpose: Used to store numerical values.
```sql
INT - Stores whole numbers.
DECIMAL(10,2) - Stores decimal numbers with precision.
FLOAT - Stores floating-point numbers.
BIGINT - Stores large integer values.
SMALLINT - Stores smaller integer values.
TINYINT - Stores very small integer values.
UNSIGNED INT - Stores only positive whole numbers.
SIGNED INT - Stores both positive and negative whole numbers.
```

## STRING DATA TYPES
### Purpose: Used to store text values.
```sql
VARCHAR(255) - Stores variable-length text (up to 255 characters).
CHAR(10) - Stores fixed-length text (exactly 10 characters).
TEXT - Stores large text data.
```

## DATE AND TIME DATA TYPES
### Purpose: Used to store date and time values.
```sql
DATE - Stores date values (YYYY-MM-DD).
TIME - Stores time values (HH:MI:SS).
DATETIME - Stores date and time values.
TIMESTAMP - Stores a timestamp that updates automatically.
```

## BINARY DATA TYPES
### Purpose: Used to store binary data, such as images and multimedia files.
```sql
BLOB - Stores large binary objects.
```

## BOOLEAN DATA TYPES
### Purpose: Stores TRUE or FALSE values.
```sql
BOOLEAN - Stores TRUE/FALSE values (implementation varies by database).
```

## JSON DATA TYPE
### Purpose: Used to store JSON (JavaScript Object Notation) data.
```sql
JSON - Stores structured JSON data.
```

## SUMMARY TABLE

| DATA TYPE | PURPOSE | EXAMPLE |
|-----------|---------|---------|
| INT | Stores whole numbers | `AGE INT;` |
| UNSIGNED INT | Stores only positive whole numbers | `ACCOUNT_BALANCE UNSIGNED INT;` |
| SIGNED INT | Stores positive and negative whole numbers | `TEMPERATURE SIGNED INT;` |
| DECIMAL | Stores decimal numbers | `PRICE DECIMAL(10,2);` |
| FLOAT | Stores floating-point numbers | `RATING FLOAT;` |
| BIGINT | Stores large integer values | `POPULATION BIGINT;` |
| SMALLINT | Stores smaller integer values | `EMPLOYEE_COUNT SMALLINT;` |
| TINYINT | Stores very small integer values | `FLAGS TINYINT;` |
| VARCHAR | Stores variable-length text | `NAME VARCHAR(255);` |
| CHAR | Stores fixed-length text | `CODE CHAR(10);` |
| TEXT | Stores large text data | `DESCRIPTION TEXT;` |
| DATE | Stores date values | `BIRTHDATE DATE;` |
| TIME | Stores time values | `START_TIME TIME;` |
| DATETIME | Stores date and time values | `EVENT_DATETIME DATETIME;` |
| TIMESTAMP | Stores auto-updating timestamp | `CREATED_AT TIMESTAMP;` |
| BLOB | Stores large binary objects | `PROFILE_PICTURE BLOB;` |
| BOOLEAN | Stores TRUE/FALSE values | `IS_ACTIVE BOOLEAN;` |
| JSON | Stores structured JSON data | `DATA JSON;` |
