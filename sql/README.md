# SQL Section

This folder contains all SQL-related work for the MidTown IT cybersecurity project, including database creation, table creation, CRUD operations, and screenshots demonstrating each step.

---

## 1. Create Database

### SQL Command
```sql
-- Create employees database
CREATE DATABASE AliAbbas_employees_db;
```

### Create Database Screenshot
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

### Create Table Screenshot
![Create Database](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/sql/screenshots/Database%20Created.png)
