# SQL Troubleshooting & Contingency Task

This section documents how I approached a simulated database corruption issue during my cybersecurity training. The goal was to demonstrate practical troubleshooting skills and recovery processes used in real environments.

---

## Scenario

After creating a SQL database and running several queries successfully, the final query returned no data and produced an error stating that **some files may be corrupted**. The error did not specify which files.

---

## Step-by-Step Troubleshooting Process

### 1. Verify and Back Up the Database
Before attempting any repair:
- Opened phpMyAdmin
- Selected the affected database
- Exported a full SQL backup using the **Quick** export method

This ensures a safe rollback point.

---

### 2. Check Error Logs
Reviewed:
- XAMPP/MySQL error logs  
- phpMyAdmin messages  
- Any warnings related to table structure or storage engine issues

This helps identify whether the issue is logical (schema/data) or physical (file corruption).

---

### 3. Run Table Integrity Checks
Used SQL commands to inspect table health:

```sql
CHECK TABLE employee;

If issues were detected, attempted optimization:

OPTIMIZE TABLE employee;

### 4. Restore from Backup (If Needed)
If corruption persisted:

Created a new database with the same name

Imported the previously exported .sql backup file

This restores the database to a known working state.

### 5. Reinstall XAMPP (Last Resort)
If the corruption was caused by the local environment rather than the database:

Uninstalled and reinstalled XAMPP

Re-imported the database backup

This resolves deeper MySQL engine issues.
