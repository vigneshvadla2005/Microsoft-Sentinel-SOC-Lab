# Failed Logons Detection

## Purpose

This query searches Windows Security Event ID **4625**, which represents failed logon attempts.

Failed logon events are common during password guessing, brute-force attacks, and unauthorized access attempts. Monitoring these events helps identify suspicious authentication activity before an attacker successfully gains access.


## Detection Logic

- Search Windows Security Events
- Filter Event ID 4625
- Display recent failed logon attempts
- Show important investigation fields


## KQL Query

```kusto
SecurityEvent
| where TimeGenerated > ago(24h)
| where EventID == 4625
| project TimeGenerated, Computer, EventID, Account, IpAddress, Activity, LogonType
| order by TimeGenerated desc
```


## Query Explanation

This query filters Windows Security Events collected in Microsoft Sentinel.

Only failed logon events (Event ID 4625) are returned.

The results include:

- TimeGenerated
- Computer
- Account
- IP Address
- Activity
- Logon Type

Sorting by the newest events allows analysts to quickly review recent authentication failures.

## Expected Output

The query returns failed authentication attempts together with the affected account, source IP address, target computer, and logon type.

These details can be used to identify repeated login failures originating from the same source.


## MITRE ATT&CK Mapping

| Technique | ID |
|----------|------|
| Brute Force | T1110 |
| Valid Accounts | T1078 |


## Evidence

Screenshot:

```
screenshots/03-KQL/01-Failed-Logons-Query.png
```


## Analyst Notes

During testing, multiple failed logon events were generated against the Windows virtual machine.

The query successfully identified the source IP address, targeted user accounts, and timestamps of each failed authentication attempt.

This information can be used as the starting point for a brute-force investigation.