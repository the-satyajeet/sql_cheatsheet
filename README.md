# MySQL Cheat Sheet

## Create database and use it further
```bash
CREATE DATABASE sample;
use sample;
```
## Create table with columns
```bash
CREATE TABLE employees (
  id int ,
  name VARCHAR(100),
  email VARCHAR(150),
  password VARCHAR(100),
  contact VARCHAR(15),
  address text,
  dob date,
  gender enum('M', 'F', 'O'),
  status tinyint(1)
);
```

## Change Table name
```bash
ALTER TABLE employees RENAME TO users;
```

## Describe the columns of a table

```bash
DESCRIBE users;
```

## Add Data Into Tables using the INSERT Query

### 1st Method
```bash
# inserting one row of data only
use stark_ind;
INSERT INTO users
(id, name, email, password, contact, address, dob, gender, status)
VALUES
(1, "John", "john@gmail.com", "12345678", "9877646853", "Gorai Road, Mumbai", "1999-01-10", "M", 1);
```

### 2nd Method
```bash
# inserting multiple rows of data
use stark_ind;
INSERT INTO users
(id, name, email, password, contact, address, dob, gender, status)
VALUES
(2, "Jenny", "jenny@gmail.com", "12363547", "9877566787", "Sec 18, Noida", "1994-04-13", "F", 1),
(3, "Sam", "sam@gmail.com", "123676876", "9877765467", "Sec 33, Noida", "1996-06-14", "M", 1),
(4, "Tony", "tony@gmail.com", "12334536", "987746478", "Sec 62, Noida", "1992-02-19", "F", 1)
```

### 3rd Method

```bash
# without defining the column names as we are using all the columns here (not skipping any column)
use stark_ind;
INSERT INTO users VALUES
(5, "Natasha", "Natasha@gmail.com", "12456567", "987734656", "Mohali, Punjab", "1999-02-24", "F", 1),
(6, "Bruce", "bruce@gmail.com", "123676876", "9877765467", "Sec 33, Noida", "1996-06-14", "M", 1)
```

## SELECT Query with WHERE Clause

### To view only specific columns
```bash
SELECT id, name, gender FROM users;
```

### To set alias (change column name while printing it)
```bash
SELECT id, name as "Student Name", gender as "Sex" FROM users;
```

### To view all the columns
```bash
SELECT * FROM users;
```

> WHERE clause is used to filter records
> Used to extract only those records that fulfill a specified condition.
> = | != | >= | <= | < | >

### To view only if satisfied the condition
```bash
SELECT * FROM users WHERE id > 4;
SELECT * FROM users WHERE name != "Bruce" and name != "Tony";
```

### To view only if satisfied the condition
```bash
SELECT * FROM users WHERE id > 4;
```

