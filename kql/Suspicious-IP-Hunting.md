# Threat Hunting – Suspicious IP Investigation

## Objective

Review authentication activity associated with a suspicious IP address.

## Scenario

After identifying repeated authentication failures, the source IP was investigated to determine whether successful logons occurred after the failed attempts.

## Detection Logic

- Review failed logons
- Review successful logons
- Compare authentication activity
- Correlate results

## KQL Query

```kusto
let SuspiciousIP="194.165.16.166";
SecurityEvent
| where IpAddress == SuspiciousIP
| project TimeGenerated, EventID, Account, Activity, Computer
| order by TimeGenerated desc
```

## Expected Result

Display authentication events associated with the selected IP address to support the investigation.

## Evidence

### Investigation Result

### Screenshot:

![Suspicious IP Investigation](../screenshots/03-KQL/07-Suspicious-IP-Hunting.png)


## MITRE ATT&CK

- T1110 – Brute Force
- T1078 – Valid Accounts

## Notes

Correlating failed and successful logon events helps determine whether repeated authentication attempts eventually resulted in a successful login.