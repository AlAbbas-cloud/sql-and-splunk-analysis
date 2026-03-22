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
This step involved uploading the `linux_s_30Day.log` file into Splunk Enterprise for indexing. Once ingested, Splunk automatically parsed timestamps, sources, and event types, making the data searchable and ready for analysis.

![Data Ingestion](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/splunk/screenshots/Data%20ingestion.png)


## 4. Failed Password Search

To identify potential brute-force activity, I searched the ingested logs for failed SSH authentication attempts. This query isolates all events containing the phrase **"Failed password"**, allowing quick detection of repeated login failures.

### Search Query
```sql
index=f1data "Failed password"
```
![Failed Password](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/splunk/screenshots/Brute-force%20pattern.png)

## 5. Subtasks Search

To demonstrate the use of subtasks, I created two separate searches and executed one of them.  
The search below filters Windows Event Logs from the monitored host.

### Search Query
```spl
source="WinEventLog:*" host="Esther2024"
```
![Subtask Search](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/splunk/screenshots/Search%20results.png)

## 6. Anomaly Detection

To identify unusual authentication patterns, I ran a time‑based analysis on events containing the keyword **"password"** from the monitored host.  

### Search Query
```spl
source="linux_s_30DAY.log" host="ESTHER2024" password | timechart count by host
```
This query visualizes how often password‑related events occurred over time, making it easier to spot spikes or irregular activity.

![Anomaly Detection](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/splunk/screenshots/Anomaly%20detection.png)


This timechart helps reveal anomalies such as:

- Sudden increases in failed login attempts
- Irregular authentication patterns
- Potential brute‑force activity
- Host‑specific spikes that may indicate targeted attacks

### Findings
- Multiple failed SSH login attempts were detected.
- Attempts were made for several invalid users.
- The pattern is consistent with a brute-force attack.
- The log entries show repeated attempts from the same source, suggesting automated activity.
  
### Conclusion
The log data shows clear signs of repeated unauthorised access attempts. 
This demonstrates how Splunk can be used to:

- Detect anomalies
- Identify brute-force patterns
- Investigate authentication failures
- Support real-time security monitoring
