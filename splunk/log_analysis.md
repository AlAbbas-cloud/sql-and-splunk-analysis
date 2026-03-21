# Splunk Installation & Account Setup

This section documents the installation of Splunk Enterprise, initial login, and creation of a Power User account. These steps form the foundation for all later log ingestion and analysis tasks.

---

## 1. Splunk Login

After installing Splunk Enterprise, I accessed the web interface through my browser and logged in using the administrator credentials created during setup.

![Splunk Login](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/splunk/screenshots/Login%20into%20the%20SPLUNK.png)

---

## 2. Power User Creation

A Power User role was created to support log ingestion, searching, and analysis. This role provides elevated permissions without full administrative access.

![Power User Creation](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/splunk/screenshots/Power%20user%20creation.png)

---

# Splunk Log Analysis

This section documents the ingestion and analysis of the `linux_s_30Day.log` dataset in Splunk Enterprise. The goal was to identify suspicious activity, detect anomalies, and demonstrate how Splunk supports SOC-style investigations.

---

## 3. Data Ingestion
![Data Ingestion](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/splunk/screenshots/Data%20ingestion.png)

---

## 4. Failed Password Search
```sql
index=f1data "Failed password"
```
![Failed Password](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/splunk/screenshots/Brute-force%20pattern.png)

### Findings
- Multiple failed SSH login attempts were detected.
- Attempts were made for several invalid users.
- The pattern is consistent with a brute-force attack.
- The log entries show repeated attempts from the same source, suggesting automated activity.
  
### Conclusion
The log data shows clear signs of repeated unauthorized access attempts. 
This demonstrates how Splunk can be used to:

- Detect anomalies
- Identify brute-force patterns
- Investigate authentication failures
- Support real-time security monitoring

Splunk’s search capabilities make it an essential tool for SOC analysts.

### Screenshots
Screenshots of the Splunk search results will be added here.
