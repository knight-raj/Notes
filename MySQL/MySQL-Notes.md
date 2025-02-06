# Database and DBMS

## What is a Database?
A database is a collection of data stored in a structured format that can be easily accessed digitally.

## What is DBMS (Database Management System)?
A Database Management System (DBMS) is software that interacts with users, applications, and databases to capture and analyze data. It helps in managing data efficiently.

---

## Types of Databases

### In-Memory Database
An in-memory database stores data in the computer's main memory (RAM) instead of on a disk.
- **Example**: H2 Database

### Relational Database (SQL)
A relational database stores data in the form of rows and columns in a tabular format.
- **Examples**: MySQL, PostgreSQL

### Non-Relational Database (NoSQL)
A non-relational database stores data in a flexible format instead of using tables. It can store data in key-value pairs, JSON, documents, and graphs.
- **Examples**: MongoDB, Redis, Cassandra

---

## Use Cases

### Relational Databases
- Financial transactions
- Inventory management
- Customer Relationship Management (CRM)
- Healthcare data

#### Scaling
- Typically scales **vertically** by upgrading hardware.

#### Limitations
- Struggles with large data and high read/write loads.
- Can be expensive, especially for large deployments.
- Difficult to maintain over time.

### Non-Relational Databases
- Social media applications
- Big data applications
- Geolocation services

#### Scaling
- Typically scales **horizontally** by adding more servers.

#### Limitations
- Limited complex query functionality.
- Data inconsistency.
- Potential lack of ACID compliance.
- Challenges with joins.

---

## Basic SQL Syntax and Keywords

| Keyword | Description |
|---------|-------------|
| **ADD** | Adds a column in an existing table |
| **ADD CONSTRAINT** | Adds a constraint after a table is already created |
| **ALL** | Returns true if all of the subquery values meet the condition |
| **ALTER** | Adds, deletes, or modifies columns in a table, or changes the data type of a column in a table |
| **ALTER COLUMN** | Changes the data type of a column in a table |
| **ALTER TABLE** | Adds, deletes, or modifies columns in a table |
| **AND** | Only includes rows where both conditions are true |
| **ANY** | Returns true if any of the subquery values meet the condition |
| **AS** | Renames a column or table with an alias |
| **ASC** | Sorts the result set in ascending order |
| **BACKUP DATABASE** | Creates a backup of an existing database |
| **BETWEEN** | Selects values within a given range |
| **CASE** | Creates different outputs based on conditions |
| **CHECK** | A constraint that limits the value that can be placed in a column |
| **COLUMN** | Changes the data type of a column or deletes a column in a table |
| **CONSTRAINT** | Adds or deletes a constraint |
| **CREATE** | Creates a database, index, view, table, or procedure |
| **CREATE DATABASE** | Creates a new SQL database |
| **CREATE INDEX** | Creates an index on a table (allows duplicate values) |
| **CREATE OR REPLACE VIEW** | Updates a view |
| **CREATE TABLE** | Creates a new table in the database |
| **CREATE PROCEDURE** | Creates a stored procedure |
| **CREATE UNIQUE INDEX** | Creates a unique index on a table (no duplicate values) |
| **CREATE VIEW** | Creates a view based on the result set of a SELECT statement |
| **DATABASE** | Creates or deletes an SQL database |
| **DEFAULT** | A constraint that provides a default value for a column |
| **DELETE** | Deletes rows from a table |
| **DESC** | Sorts the result set in descending order |
| **DISTINCT** | Selects only distinct (different) values |
| **DROP** | Deletes a column, constraint, database, index, table, or view |
| **DROP COLUMN** | Deletes a column in a table |
| **DROP CONSTRAINT** | Deletes a UNIQUE, PRIMARY KEY, FOREIGN KEY, or CHECK constraint |
| **DROP DATABASE** | Deletes an existing SQL database |
| **DROP DEFAULT** | Deletes a DEFAULT constraint |
| **DROP INDEX** | Deletes an index in a table |
| **DROP TABLE** | Deletes an existing table in the database |
| **DROP VIEW** | Deletes a view |
| **EXEC** | Executes a stored procedure |
| **EXISTS** | Tests for the existence of any record in a subquery |
| **FOREIGN KEY** | A constraint that is a key used to link two tables together |
| **FROM** | Specifies which table to select or delete data from |
| **FULL OUTER JOIN** | Returns all rows when there is a match in either left table or right table |
| **GROUP BY** | Groups the result set (used with aggregate functions: COUNT, MAX, MIN, SUM, AVG) |
| **HAVING** | Used instead of WHERE with aggregate functions |
| **IN** | Allows you to specify multiple values in a WHERE clause |
| **INDEX** | Creates or deletes an index in a table |
| **INNER JOIN** | Returns rows that have matching values in both tables |
| **INSERT INTO** | Inserts new rows in a table |
| **INSERT INTO SELECT** | Copies data from one table into another table |
| **IS NULL** | Tests for empty values |
| **IS NOT NULL** | Tests for non-empty values |
| **JOIN** | Joins tables |
| **LEFT JOIN** | Returns all rows from the left table, and the matching rows from the right table |
| **LIKE** | Searches for a specified pattern in a column |
| **LIMIT** | Specifies the number of records to return in the result set |
| **NOT** | Only includes rows where a condition is not true |
| **NOT NULL** | A constraint that enforces a column to not accept NULL values |
| **OR** | Includes rows where either condition is true |
| **ORDER BY** | Sorts the result set in ascending or descending order |
| **OUTER JOIN** | Returns all rows when there is a match in either left table or right table |
| **PRIMARY KEY** | A constraint that uniquely identifies each record in a database table |
| **PROCEDURE** | A stored procedure |
| **RIGHT JOIN** | Returns all rows from the right table, and the matching rows from the left table |
| **SELECT** | Selects data from a database |
| **SELECT DISTINCT** | Selects only distinct (different) values |
| **SET** | Specifies which columns and values should be updated in a table |
| **TABLE** | Creates a table, or adds, deletes, or modifies columns in a table |
| **TRUNCATE TABLE** | Deletes the data inside a table, but not the table itself |
| **UNION** | Combines the result set of two or more SELECT statements (only distinct values) |
| **UPDATE** | Updates existing rows in a table |
| **VALUES** | Specifies the values of an INSERT INTO statement |
| **VIEW** | Creates, updates, or deletes a view |
| **WHERE** | Filters a result set to include only records that fulfill a specified condition |

---

# MySQL Data Types

MySQL has three main data types: **string**, **numeric**, and **date and time**.

## String Data Types

| Data Type | Description |
|-----------|-------------|
| **CHAR(size)** | A FIXED length string (can contain letters, numbers, and special characters). The size parameter specifies the column length in characters - can be from 0 to 255. Default is 1. |
| **VARCHAR(size)** | A VARIABLE length string (can contain letters, numbers, and special characters). The size parameter specifies the maximum column length in characters - can be from 0 to 65535. |
| **BINARY(size)** | Equal to CHAR(), but stores binary byte strings. The size parameter specifies the column length in bytes. Default is 1. |
| **VARBINARY(size)** | Equal to VARCHAR(), but stores binary byte strings. The size parameter specifies the maximum column length in bytes. |
| **TINYBLOB** | For BLOBs (Binary Large OBjects). Max length: 255 bytes. |
| **TINYTEXT** | Holds a string with a maximum length of 255 characters. |
| **TEXT(size)** | Holds a string with a maximum length of 65,535 bytes. |
| **BLOB(size)** | For BLOBs (Binary Large OBjects). Holds up to 65,535 bytes of data. |
| **MEDIUMTEXT** | Holds a string with a maximum length of 16,777,215 characters. |
| **MEDIUMBLOB** | For BLOBs (Binary Large OBjects). Holds up to 16,777,215 bytes of data. |
| **LONGTEXT** | Holds a string with a maximum length of 4,294,967,295 characters. |
| **LONGBLOB** | For BLOBs (Binary Large OBjects). Holds up to 4,294,967,295 bytes of data. |
| **ENUM(val1, val2, ...)** | A string object that can have only one value, chosen from a list of possible values. You can list up to 65535 values in an ENUM list. If a value is inserted that is not in the list, a blank value will be inserted. The values are sorted in the order you enter them. |
| **SET(val1, val2, ...)** | A string object that can have 0 or more values, chosen from a list of possible values. You can list up to 64 values in a SET list. |

## Numeric Data Types

| Data Type | Description |
|-----------|-------------|
| **BIT(size)** | A bit-value type. The number of bits per value is specified in size. The size parameter can hold a value from 1 to 64. The default value for size is 1. |
| **TINYINT(size)** | A very small integer. Signed range is from -128 to 127. Unsigned range is from 0 to 255. The size parameter specifies the maximum display width (which is 255). |
| **BOOL** | Zero is considered as false, nonzero values are considered as true. |
| **BOOLEAN** | Equal to BOOL. |
| **SMALLINT(size)** | A small integer. Signed range is from -32768 to 32767. Unsigned range is from 0 to 65535. The size parameter specifies the maximum display width (which is 255). |
| **MEDIUMINT(size)** | A medium integer. Signed range is from -8388608 to 8388607. Unsigned range is from 0 to 16777215. The size parameter specifies the maximum display width (which is 255). |
| **INT(size)** | A medium integer. Signed range is from -2147483648 to 2147483647. Unsigned range is from 0 to 4294967295. The size parameter specifies the maximum display width (which is 255). |
| **INTEGER(size)** | Equal to INT(size). |
| **BIGINT(size)** | A large integer. Signed range is from -9223372036854775808 to 9223372036854775807. Unsigned range is from 0 to 18446744073709551615. The size parameter specifies the maximum display width (which is 255). |
| **FLOAT(size, d)** | A floating point number. The total number of digits is specified in size. The number of digits after the decimal point is specified in the d parameter. This syntax is deprecated in MySQL 8.0.17, and it will be removed in future MySQL versions. |
| **FLOAT(p)** | A floating point number. MySQL uses the p value to determine whether to use FLOAT or DOUBLE for the resulting data type. If p is from 0 to 24, the data type becomes FLOAT(). If p is from 25 to 53, the data type becomes DOUBLE(). |
| **DOUBLE(size, d)** | A normal-size floating point number. The total number of digits is specified in size. The number of digits after the decimal point is specified in the d parameter. |
| **DOUBLE PRECISION(size, d)** | Equivalent to DOUBLE(size, d). |
| **DECIMAL(size, d)** | An exact fixed-point number. The total number of digits is specified in size. The number of digits after the decimal point is specified in the d parameter. The maximum number for size is 65. The maximum number for d is 30. The default value for size is 10. The default value for d is 0. |
| **DEC(size, d)** | Equal to DECIMAL(size,d). |

**Note:** All numeric data types may have an extra option: **UNSIGNED** or **ZEROFILL**. If you add the UNSIGNED option, MySQL disallows negative values for the column. If you add the ZEROFILL option, MySQL automatically also adds the UNSIGNED attribute to the column.

## Date and Time Data Types

| Data Type | Description |
|-----------|-------------|
| **DATE** | A date. Format: YYYY-MM-DD. The supported range is from '1000-01-01' to '9999-12-31'. |
| **DATETIME(fsp)** | A date and time combination. Format: YYYY-MM-DD hh:mm:ss. The supported range is from '1000-01-01 00:00:00' to '9999-12-31 23:59:59'. Adding DEFAULT and ON UPDATE in the column definition allows automatic initialization and updating to the current date and time. |
| **TIMESTAMP(fsp)** | A timestamp. TIMESTAMP values are stored as the number of seconds since the Unix epoch ('1970-01-01 00:00:00' UTC). Format: YYYY-MM-DD hh:mm:ss. The supported range is from '1970-01-01 00:00:01' UTC to '2038-01-09 03:14:07' UTC. Automatic initialization and updating to the current date and time can be specified using DEFAULT CURRENT_TIMESTAMP and ON UPDATE CURRENT_TIMESTAMP in the column definition. |
| **TIME(fsp)** | A time. Format: hh:mm:ss. The supported range is from '-838:59:59' to '838:59:59'. |
| **YEAR** | A year in four-digit format. Values allowed in four-digit format: 1901 to 2155, and 0000. |

**Note:** MySQL 8.0 does not support year in two-digit format.

