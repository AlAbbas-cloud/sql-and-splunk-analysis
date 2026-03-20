# SQL Section

This folder contains all SQL-related work for the MidTown IT cybersecurity project, including database creation, table creation, CRUD operations, and screenshots demonstrating each step.

---

## 1. Create Database

### SQL Command
```sql
-- Create employees database
CREATE DATABASE AliAbbas_employees_db;
```

### Screenshot
![Create Database](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/sql/screenshots/Create%20Database.png)

## 2. Create Table

### SQL Command
```sql
-- Create Employee Table
CREATE TABLE employee (
    employee_no INT PRIMARY KEY,
    name VARCHAR(50),
    date_of_birth DATE,
    position VARCHAR(50),
    email VARCHAR(100),
    phone_no VARCHAR(20)
);
```

### Screenshot
![Create Database](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/sql/screenshots/Database%20Created.png)

## 3. Table Created & Populated

### SQL Command
```sql
-- Insert Employee Records
INSERT INTO employee (employee_no, name, date_of_birth, position, email, phone_no) VALUES
(1234, 'Mary', '1991-01-01', 'Engineer', 'Mary.1991@certiv.com', '981'),
(2345, 'Samuel', '1992-02-02', 'CEO', 'Samuel.1992@certiv.com', '982'),
(3456, 'John', '1983-03-03', 'Data analyst', 'John.1983@certiv.com', '983'),
(4567, 'David', '1984-04-04', 'Engineer', 'David.1984@certiv.com', '984'),
(5678, 'Mark', '1985-05-05', 'Manager', 'Mark.1985@certiv.com', '985'),
(6789, 'Jack', '1986-06-06', 'Manager', 'Jack.1986@certiv.com', '986'),
(7890, 'Kyle', '1987-07-07', 'Salesman', 'Kyle.1987@certiv.com', '987'),
(8901, 'Michael', '1988-08-08', 'Salesman', 'Michael.1988@certiv.come', '988'),
(9012, 'Jared', '1978-01-01', 'Engineer', 'Jared.1978@certiv.com', '989'),
(9013, 'Brandon', '1979-02-02', 'Network admin', 'Brandon.1979@certiv.com', '990'),
(9014, 'Karen', '1984-03-03', 'Data analyst', 'Karen.1984@certviv.com', '991');
```

### Screenshot
![Create Database](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/sql/screenshots/Table%20created%20and%20populated.png)

## 4. Select Queries

### a) Select the first five records

### SQL Command
```sql
-- Select the first five records
SELECT * FROM employee LIMIT 5;
```

### Screenshot
![Create Database](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/sql/screenshots/Select%20the%20first%20five%20records.png)

### b) Select employees who are managers

### SQL Command
```sql
SELECT * FROM employee WHERE position = 'Manager';
```

### Screenshot
![Create Database](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/sql/screenshots/Select%20the%20employees%20who%20are%20managers.png)
