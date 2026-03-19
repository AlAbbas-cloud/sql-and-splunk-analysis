# Splunk Log Analysis

After ingesting the `linux_s_30Day.log` dataset into Splunk, I performed a search for failed password attempts.

### Search Query

index=f1data "Failed password"

### Findings
- Multiple failed SSH login attempts were detected.
- Attempts were made for several invalid users.
- The pattern is consistent with a brute-force attack.

### Conclusion
The log data shows clear signs of repeated unauthorized access attempts. This demonstrates how Splunk can be used to detect anomalies and security threats in real time.

### Screenshots
Screenshots of the Splunk search results will be added here.
