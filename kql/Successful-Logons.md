# Successful Logons Detection

## Purpose

This query searches Windows Security Event ID **4624**, which represents successful user logons.

Monitoring successful logon events helps analysts verify legitimate user activity, identify unusual login patterns, and correlate successful authentication with previous failed login attempts.


## Detection Logic

- Search Windows Security Events
- Filter Event ID 4624
- Display recent successful logons
- Show important investigation fields


## KQL Query

```kusto
SecurityEvent
| where TimeGenerated > ago(24h)
| where EventID == 4624
| project TimeGenerated, Computer, EventID, Account, IpAddress, Activity, LogonType
| order by TimeGenerated desc
```


## Query Explanation

This query retrieves successful authentication events recorded by Windows Security Logs.

The output includes the user account, source IP address, computer name, activity, logon type, and timestamp, allowing analysts to review who successfully accessed the system.


## Expected Output

The query displays successful logon events together with the user account, source IP address, destination computer, and authentication details.

These events can be correlated with failed logon attempts to identify successful access following repeated authentication failures.


## MITRE ATT&CK Mapping

| Technique | ID |
|-----------|----|
| Valid Accounts | T1078 |
| External Remote Services | T1133 |


## Evidence

Screenshot:

```
screenshots/03-KQL/02-Successful-Logons-Query.png
```


## Analyst Notes

The successful logon events generated during the lab confirmed that authentication attempts were recorded correctly after valid credentials were used.

Reviewing these events alongside failed logon attempts provides additional context during an authentication investigation.