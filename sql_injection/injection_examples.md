# SQL Injection Demonstration

This section documents a simple SQL injection test performed against the employees database.

### Injection Payload Used

'OR'a'='a


### What This Does
This payload forces the SQL condition to always evaluate as TRUE, allowing an attacker to bypass authentication or access data without proper credentials.

### Why It Works
The application does not validate or sanitize user input, allowing raw SQL to be executed directly.

### Screenshots
Screenshots of the injection test will be added here.
