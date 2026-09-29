# Creating Table and Modifying the Table

## 1. Create a Table

The `CREATE TABLE` command is used to create a new table in a database.

### Example

```sql
CREATE TABLE EMPLOYEE (
  EID INT PRIMARY KEY,
  ENAME VARCHAR(50) NOT NULL,
  DEPT VARCHAR(30) DEFAULT 'HR',
  SALARY DECIMAL(10,2),
  DOJ DATE,
  EXP INT CHECK(EXP > 0)
);
```

## 2. Insert Records

```sql
INSERT INTO EMPLOYEE
VALUES (101, 'Ravi', 'IT', 35000, '2025-01-10', 2);

INSERT INTO EMPLOYEE
VALUES (102, 'Anu', 'HR', 40000, '2024-06-15', 3);
```

## 3. Modify the Table

The `ALTER TABLE` command is used to modify an existing table.

### Add a Column

```sql
ALTER TABLE EMPLOYEE
ADD PHONE VARCHAR(15);
```

### Modify a Column

```sql
ALTER TABLE EMPLOYEE
MODIFY ENAME VARCHAR(100);
```

### Rename a Column

```sql
ALTER TABLE EMPLOYEE
RENAME COLUMN PHONE TO MOBILE;
```

### Drop a Column

```sql
ALTER TABLE EMPLOYEE
DROP COLUMN MOBILE;
```

## 4. View the Table

```sql
SELECT * FROM EMPLOYEE;
```

## 5. Describe the Table

```sql
DESC EMPLOYEE;
```

## Commands Summary

| Command         | Purpose                    |
| --------------- | -------------------------- |
| `CREATE TABLE`  | Creates a new table        |
| `INSERT INTO`   | Inserts records            |
| `ALTER TABLE`   | Modifies an existing table |
| `ADD`           | Adds a new column          |
| `MODIFY`        | Changes column definition  |
| `RENAME COLUMN` | Renames a column           |
| `DROP COLUMN`   | Removes a column           |
| `SELECT`        | Displays records           |
| `DESC`          | Displays table structure   |
