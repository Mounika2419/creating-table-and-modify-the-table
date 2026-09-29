# SQL: Creating and Modifying Tables

This project demonstrates basic **MySQL commands** for creating, modifying, inserting, updating, deleting, and displaying data in tables.

## 1. Show Databases

```sql
SHOW DATABASES;
```

Displays all databases available in the MySQL server.

## 2. Select a Database

```sql
USE aids;
```

Selects the `aids` database for performing SQL operations.

## 3. Create a Table

```sql
CREATE TABLE student (
    sid INT,
    sname VARCHAR(20),
    sdept VARCHAR(20)
);
```

Creates a table named `student` with three columns:

* `sid` – Student ID
* `sname` – Student name
* `sdept` – Student department

## 4. Add a New Column

```sql
ALTER TABLE student ADD sage INT;
```

Adds a new column `sage` to the `student` table to store the student's age.

## 5. Rename a Table

```sql
RENAME TABLE std TO student;
```

Renames the table `std` to `student`.

> **Note:** This command will work only if a table named `std` already exists. If `student` has already been created, this command is unnecessary and will produce an error if `student` already exists.

## 6. Insert Records

```sql
INSERT INTO student VALUES (101, "ram", "aids", 20);
INSERT INTO student VALUES (101, "raju", "aiml", 21);
INSERT INTO student VALUES (103, "ravi", "cse", 20);
INSERT INTO student VALUES (104, "meera", "ece", 21);
INSERT INTO student VALUES (105, "reena", "eee", 19);
```

Adds student records to the `student` table.

The columns are:

| SID | SNAME | SDEPT | SAGE |
| --: | ----- | ----- | ---: |
| 101 | ram   | aids  |   20 |
| 101 | raju  | aiml  |   21 |
| 103 | ravi  | cse   |   20 |
| 104 | meera | ece   |   21 |
| 105 | reena | eee   |   19 |

## 7. Display Table Structure

```sql
DESC student;
```

Displays the structure of the `student` table, including column names, data types, and other information.

## 8. Update a Record

```sql
UPDATE student
SET sid = 102
WHERE sname = "raju";
```

Changes the `sid` of the student named `raju` from `101` to `102`.

## 9. Display All Records

```sql
SELECT * FROM student;
```

Displays all records from the `student` table.

## 10. Drop a Table

```sql
DROP TABLE std;
```

Permanently deletes the `std` table and all its data.

> **Note:** The table `std` must exist for this command to work.

## 11. Display Current Date and Time

```sql
SELECT NOW();
```

Displays the current date and time of the MySQL server.

## 12. Drop the `clg` Table

```sql
DROP TABLE clg;
```

Deletes the `clg` table permanently along with its data.

## 13. Show All Tables

```sql
SHOW TABLES;
```

Displays all tables available in the currently selected database.

## 14. Insert Data into Employee

```sql
INSERT INTO employee (eid, ename, age)
VALUES (101, "anil", 50);
```

Inserts an employee record into the `employee` table.

* `eid` – Employee ID
* `ename` – Employee name
* `age` – Employee age

> **Note:** The `employee` table must already exist before executing this command.

## 15. Modify a Column

```sql
ALTER TABLE student
MODIFY COLUMN sname VARCHAR(25);
```

Changes the size of the `sname` column from `VARCHAR(20)` to `VARCHAR(25)`.

## 16. Display Employee Table Structure

```sql
DESC employee;
```

Displays the structure of the `employee` table.

## 17. Display Employee Records

```sql
SELECT * FROM employee;
```

Displays all records from the `employee` table.

## 18. Update Employee Data

```sql
UPDATE employee
SET age = 20
WHERE eid = 105;
```

Changes the age of the employee whose ID is `105` to `20`.

> **Note:** This command will affect a record only if employee `105` exists.

## 19. Delete a Record

```sql
DELETE FROM employee
WHERE eid = 101;
```

Deletes the employee record whose ID is `101`.

## 20. Truncate a Table

```sql
TRUNCATE TABLE employee;
```

Removes **all records** from the `employee` table while keeping the table structure.

## Important SQL Commands

| SQL Command          | Purpose                         |
| -------------------- | ------------------------------- |
| `SHOW DATABASES`     | Displays all databases          |
| `USE`                | Selects a database              |
| `CREATE TABLE`       | Creates a new table             |
| `ALTER TABLE ADD`    | Adds a new column               |
| `ALTER TABLE MODIFY` | Modifies a column               |
| `RENAME TABLE`       | Renames a table                 |
| `INSERT INTO`        | Adds records                    |
| `SELECT`             | Displays records                |
| `UPDATE`             | Changes existing records        |
| `DELETE`             | Deletes selected records        |
| `TRUNCATE TABLE`     | Removes all records             |
| `DROP TABLE`         | Deletes the table completely    |
| `DESC`               | Displays table structure        |
| `SHOW TABLES`        | Displays tables in the database |
| `NOW()`              | Displays current date and time  |

## Difference Between DELETE, TRUNCATE and DROP

| Command    | Data                     | Table Structure  |
| ---------- | ------------------------ | ---------------- |
| `DELETE`   | Deletes selected records | Remains          |
| `TRUNCATE` | Deletes all records      | Remains          |
| `DROP`     | Deletes all records      | Table is deleted |

## Conclusion

This SQL program demonstrates the basic operations required to **create and modify tables**, insert and manipulate records, and manage database tables using MySQL.
