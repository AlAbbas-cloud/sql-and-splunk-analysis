# Splunk Log Analysis

This section documents the ingestion and analysis of the `linux_s_30Day.log` dataset in Splunk Enterprise. The goal was to identify suspicious activity, detect anomalies, and demonstrate how Splunk supports SOC-style investigations.

---

### Search Query Used

```sql
index=f1data "Failed password"
```

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
