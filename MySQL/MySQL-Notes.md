# MySQL

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

# MySQL Operators and DDL Commands

## MySQL Operators
In MySQL, there are 9 main types of operators:

1. **Arithmetic Operators**  -- Perform basic mathematical operations
2. **Comparison Operators**  -- Compare values (e.g., =, !=, >, <)
3. **Logical Operators**  -- Used to combine multiple conditions (e.g., AND, OR, NOT)
4. **String Operators**  -- Manipulate string values
5. **Bitwise Operators**  -- Perform bitwise operations
6. **Set Operators**  -- Used with multiple queries (e.g., UNION, INTERSECT)
7. **NULL Operators**  -- Check for NULL values
8. **Existence Operators**  -- Used to check existence conditions (e.g., EXISTS)
9. **Other Operators** (such as DISTINCT, ORDER BY, LIMIT) -- Provide additional functionalities

 <img src="https://github.com/user-attachments/assets/fe8c4743-5529-4ec5-bd14-5cca36fe0d11" alt="Operators1" width="400"/>

## DDL (Data Definition Language)
DDL commands are used to define and modify database structures.

- **CREATE**  -- Creates new database objects like tables
- **ALTER**  -- Modifies existing database objects
- **RENAME**  -- Changes the name of a database object
- **TRUNCATE**  -- Removes all records from a table without logging
- **DROP**  -- Deletes a database object

## **SQL Syntax Format**
```
COLUMN_NAME DATA_TYPE(SIZE) CONSTRAINTS;
```
- **COLUMN_NAME** → The name of the column.
- **DATA_TYPE(SIZE)** → The data type and size (optional for some types like `INT`).
- **CONSTRAINTS** → Conditions like `NOT NULL`, `PRIMARY KEY`, `UNIQUE`, etc.


### **Choosing Integer Types** (Check above for Signed or Unsigned values in Numeric Data Types)
----
| **Scenario** | **Best Type** |
|-------------|-------------|
| Storing **boolean values** (`0/1`) | `TINYINT(1)` |
| Counting **small objects** (students in a class) | `SMALLINT` |
| **Population of a city** | `MEDIUMINT` |
| **General-purpose IDs, orders, users** | `INT` |
| **Very large numbers (billions, trillions, money transactions)** | `BIGINT` |

---

## **🔴 Misconception About INT(10)**

```sql
CREATE TABLE Students (
    rollno INT(10) NOT NULL PRIMARY KEY
);
```
- `INT(10)` **does NOT mean** it can store bigger numbers than `INT` alone.
- `INT(10)` **does NOT increase storage size**.
- The size inside parentheses `(10)` **only affects `ZEROFILL` behavior** (if enabled).

### **Correct Way (Recommended)**
```sql
CREATE TABLE Students (
    rollno INT NOT NULL PRIMARY KEY
);
```
- Just writing `INT` is **enough** and **correct**.
- `INT` **always uses 4 bytes** of storage.
- It supports values from **`-2,147,483,648` to `2,147,483,647`**.

---

## **When Does INT(10) Matter?**
If you use `ZEROFILL`, it **pads numbers with leading zeros**:

```sql
CREATE TABLE Students (
    rollno INT(10) ZEROFILL PRIMARY KEY
);
```
Now, inserting `1` into `rollno` will display:
```
0000000001
```
- The `(10)` **means it displays numbers with at least 10 digits**, padding with zeros.
- **Does NOT affect storage or value range**.

---

## **What is `ZEROFILL` in MySQL?**
`ZEROFILL` is an attribute in MySQL that **pads numeric values with leading zeros** when displayed. It **does NOT affect storage or calculations—only how numbers appear when retrieved**.

###  **Example Without `ZEROFILL`**
```sql
CREATE TABLE Students (
    rollno INT(5) NOT NULL PRIMARY KEY
);
INSERT INTO Students (rollno) VALUES (7), (25), (123);
SELECT rollno FROM Students;
```
**🔹 Output (Without `ZEROFILL`)**
```
rollno
------
7
25
123
```
🔹 **Numbers are displayed as normal—no leading zeros.**

### **Example With `ZEROFILL`**
```sql
CREATE TABLE Students (
    rollno INT(5) ZEROFILL PRIMARY KEY
);
INSERT INTO Students (rollno) VALUES (7), (25), (123);
SELECT rollno FROM Students;
```
**🔹 Output (With `ZEROFILL`)**
```
rollno
------
00007
00025
00123
```
🔹 **Numbers are displayed with leading zeros to match the `(5)` width.**

###  **Important Notes About `ZEROFILL`**
- `ZEROFILL` **only affects display, NOT storage**.
- It **automatically makes the column `UNSIGNED`**, meaning **it cannot store negative values**.
- **Deprecated in MySQL 8.0.17 and later** (not recommended for new projects).
- **Does NOT work on `BIGINT`, `SMALLINT`, `TINYINT`, etc., in newer MySQL versions**.

---

## **ALTER Command: Modifying Existing Tables**

### **Add a Column in an Existing Table**
```sql
ALTER TABLE Students
ADD COLUMN school VARCHAR(255);
```
- **`ALTER TABLE Students`** → Modifies the `Students` table.
- **`ADD COLUMN school VARCHAR(255)`** → Adds a new column named `school` with a `VARCHAR(255)` data type.

#### **Optional Modifications**
1. **Set a Default Value:**
   ```sql
   ALTER TABLE Students
   ADD COLUMN school VARCHAR(255) DEFAULT 'Unknown';
   ```

    If you do not provide a value for school, it defaults to 'Unknown'.
    If you do provide a value for school, that value is stored instead like "ABC School".

2. **Make the Column `NOT NULL`**:
   ```sql
   ALTER TABLE Students
   ADD COLUMN school VARCHAR(255) NOT NULL;
   ```
   **⚠️ If the table already has data, you'll need to provide a default value, or it will fail.**
3. **Add the Column at a Specific Position:**
   ```sql
   ALTER TABLE Students
   ADD COLUMN school VARCHAR(255) AFTER name;
   ```
   

---

###  **Remove a Column from an Existing Table**
```sql
ALTER TABLE Students
DROP COLUMN school;
```
- **`ALTER TABLE Students`** → Modifies the `Students` table.
- **`DROP COLUMN school`** → Removes the `school` column from the table.

#### **Important Notes:**
- **Data Loss Warning:** ⚠️ This operation **permanently deletes** the column and its data.
- **Make sure to back up your data before executing this command.**

#### **Remove Multiple Columns:**
```sql
ALTER TABLE Students
DROP COLUMN school,
DROP COLUMN city;
```

---
# SQL Queries

## Selecting and Using a Database
If you want to switch to a specific database or before creating any table in a database for the first time, use:

```sql
USE databasename; -- Here use Database name here "Practice"
```

Then, you can verify it with:

```sql
SELECT DATABASE();
```

However, you must use `USE practice;` (or specify the database in queries) to ensure your commands run on the correct database.

### Example without `SELECT DATABASE();`

```sql
CREATE DATABASE practice;
USE practice;  -- This is necessary to switch to the correct database

CREATE TABLE student (
    rollno INT PRIMARY KEY,
    name VARCHAR(255),
    school VARCHAR(50) NOT NULL
);
```

OR, if you don’t use `USE practice;`, you can specify the database directly:

```sql
CREATE TABLE practice.student (
    rollno INT PRIMARY KEY,
    name VARCHAR(255),
    school VARCHAR(50) NOT NULL
);
```


### Creating the Student Table
```sql
-- Creating a table to store student records
CREATE TABLE student(
    rollno INT PRIMARY KEY,  -- Unique roll number for each student
    name VARCHAR(50),       -- Name of the student
    marks INT NOT NULL,     -- Marks obtained (cannot be NULL)
    grade VARCHAR(1),       -- Grade assigned (single character)
    city VARCHAR(20)        -- City name (up to 20 characters)
);
```

### Inserting Multiple Records into the Student Table
```sql
-- Inserting multiple student records into the table
INSERT INTO student
(rollno, name, marks, grade, city)
VALUES
(101, "Ankit", 94, "A", "Narkatiaganj"),
(102, "Rahul", 85, "B", "Merath"),
(103, "Saket", 71, "C", "Gaya"),
(105, "Pawan", 61, "D", "Patna"),
(106, "Shyam", 50, "F", "BTH"),
(107, "Rohit", 73, "C", "Narkatiaganj"),
(108, "Anuradha", 22, "F", "Patna");
```

### Retrieving Data
```sql
-- Selecting all student records
SELECT * FROM student;

-- Selecting only name and marks columns
SELECT name, marks FROM student;

-- Selecting unique city names
SELECT DISTINCT city FROM student;

-- Selecting students with marks greater than 70 from "Narkatiaganj"
SELECT * FROM student WHERE marks > 70 AND city = "Narkatiaganj";

-- Selecting students from "Narkatiaganj"
SELECT * FROM student WHERE city = "Narkatiaganj";

-- Selecting students with marks greater than 60 or from "Patna"
SELECT * FROM student WHERE marks > 60 OR city = "Patna";

-- Selecting students with marks between 70 and 90
SELECT * FROM student WHERE marks BETWEEN 70 AND 90;

-- Selecting only the first 3 records
SELECT * FROM student LIMIT 3;

-- Selecting the first 3 students with marks greater than 75
SELECT * FROM student WHERE marks > 75 LIMIT 3;

-- Sorting students by city name in ascending order
SELECT * FROM student ORDER BY city ASC;

-- Selecting top 3 students with highest marks
SELECT * FROM student ORDER BY marks DESC LIMIT 3;
```


---

# Using LIMIT in SQL Queries

## What is the LIMIT Clause?
The `LIMIT` clause is used to restrict the number of rows returned or affected by a query. It is commonly used in `SELECT`, `UPDATE`, and `DELETE` operations.

## Supported Databases
- `LIMIT` is not part of the official SQL standard (ANSI SQL).
- Only MySQL and PostgreSQL support `LIMIT` with `SELECT`, `UPDATE`, and `DELETE`.
- SQL Server and Oracle do not support `LIMIT` in `UPDATE` or `DELETE`. Instead, they use alternatives like `TOP` (SQL Server) or `ROWNUM` (Oracle).

## 1. Using LIMIT with SELECT

`LIMIT` is mainly used in `SELECT` queries to fetch a limited number of rows.

### Example 1: Fetch the first 3 students

```sql
SELECT * FROM student ORDER BY rollno ASC LIMIT 3;
```

This retrieves only 3 rows ordered by `rollno`.

### Example 2: Using LIMIT with OFFSET

```sql
SELECT * FROM student ORDER BY rollno ASC LIMIT 3 OFFSET 2;
```

This skips the first 2 rows and then fetches 3 rows.

---

## 2. Using LIMIT with UPDATE

In MySQL, `LIMIT` in an `UPDATE` query ensures that only a specific number of rows are modified.

### Example: Update school name for only 1 student

```sql
UPDATE student
SET school = 'Updated School'
ORDER BY rollno ASC
LIMIT 1;
```

This updates the school name for only 1 student, based on the `ORDER BY rollno ASC` condition.
If `ORDER BY` is not used, MySQL will randomly pick a matching row.

### How to Check Which Row Will Be Updated?
Before running the `UPDATE`, use this `SELECT` query:

```sql
SELECT * FROM student ORDER BY rollno ASC LIMIT 1;
```

This helps identify which student will be updated first.

### PostgreSQL Alternative: Using RETURNING

```sql
UPDATE student
SET school = 'Updated School'
ORDER BY rollno ASC
LIMIT 1
RETURNING *;
```

PostgreSQL allows `RETURNING *` to show the updated row.

---

## 3. Using LIMIT with DELETE

You can delete only a limited number of rows using `LIMIT` in MySQL.

### Example: Delete only 2 students

```sql
DELETE FROM student
ORDER BY rollno ASC
LIMIT 2;
```

Even if more than 2 students match, this deletes only the first 2.

### ORDER BY Must Have a Column Name
You must specify which column to order by.

Example:

```sql
ORDER BY rollno ASC;
```

### ASC (Ascending) or DESC (Descending)
- `ASC` → Sorts from smallest to largest (default).
- `DESC` → Sorts from largest to smallest.

---

# Using SQL OFFSET Clause

SQL `OFFSET` is a powerful clause used to skip a specified number of rows in a query result. It is often combined with the `LIMIT` clause for data pagination.

```sql
SELECT column_names
FROM table_name
ORDER BY column_name
LIMIT number_of_rows OFFSET offset_value;
```

### Example:

#### Select all columns for students, starting from the 10th row

```sql
SELECT rollno, name, school
FROM student
ORDER BY rollno
OFFSET 9 ROWS;
```

Since `OFFSET 9 ROWS` skips the first 9 rows, the result starts from the 10th row.


### Aggregate Functions
```sql
-- Finding the highest marks in the student table
SELECT MAX(marks) FROM student;

-- Finding the lowest marks in the student table
SELECT MIN(marks) FROM student;

-- Calculating the average marks of students
SELECT AVG(marks) FROM student;

-- Counting the number of students in the table
SELECT COUNT(name) FROM student;
```

### Grouping and Aggregation
```sql
-- Grouping students by city and selecting city names
SELECT city FROM student GROUP BY city;

-- Counting the number of students in each city
SELECT city, COUNT(rollno) FROM student GROUP BY city;

-- Counting students grouped by both city and name
SELECT city, name, COUNT(rollno) FROM student GROUP BY city, name;

-- Calculating the average marks per city and sorting by city name
SELECT city, AVG(marks) FROM student GROUP BY city ORDER BY city;

-- Calculating the average marks per city and sorting by average marks
SELECT city, AVG(marks) FROM student GROUP BY city ORDER BY AVG(marks);

-- Sorting the average marks per city in descending order
SELECT city, AVG(marks) FROM student GROUP BY city ORDER BY AVG(marks) DESC;

-- Counting the number of students per grade and sorting by grade
SELECT grade, COUNT(rollno) FROM student GROUP BY grade ORDER BY grade;
```

### Using HAVING Clause
```sql
-- Grouping students by city and counting the number of students in each city, filtering with HAVING clause
SELECT city, COUNT(rollno) FROM student GROUP BY city HAVING MAX(marks) > 60;

-- Retrieving cities where at least one student has grade 'C' and the maximum marks in that city are greater than 72
SELECT city FROM student WHERE grade = "C" GROUP BY city HAVING MAX(marks) > 72 ORDER BY city DESC;
```





