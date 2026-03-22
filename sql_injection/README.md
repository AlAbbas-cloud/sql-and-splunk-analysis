# SQL Injection Demonstration

This section documents a simple SQL injection test performed against the employees database.

---

### Injection Payload Used

```sql
'OR'a'='a
```

### What This Does
This payload forces the SQL condition to always evaluate as TRUE, which can allow an attacker to:

- Bypass login forms
- Access restricted data
- Manipulate database queries

### Why It Works
The application does not validate or sanitize user input.
As a result, raw SQL is passed directly into the query, allowing the attacker to inject their own logic.

This is a classic example of SQL Injection (SQLi).

### Screenshot

![SQL injection](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/sql_injection/screenshots/Run%20an%20SQL%20injection%20attack.png)

### Prevention Methods
Common methods to prevent SQL injection include:

- Prepared Statements / Parameterised Queries  
Ensures user input is treated as data, not executable SQL.

- Input Validation  
Rejects unexpected characters and enforces strict data types.

- Stored Procedures  
Encapsulates SQL logic and reduces direct query manipulation.

- Web Application Firewalls (WAFs)  
Detect and block malicious input patterns.

### Summary
This demonstration highlights the importance of secure coding practices and proper input handling. SQL injection remains one of the most common and dangerous vulnerabilities in web applications, and understanding it is essential for any cybersecurity professional.
