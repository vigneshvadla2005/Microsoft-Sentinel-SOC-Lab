# Event Count Summary

## Objective

Summarize collected Windows Security Events to understand the volume of security activity during the lab.

## Scenario

Before beginning the investigation, event counts were reviewed to verify that Windows Security Events were being collected correctly.

## Detection Logic

- Count collected events
- Group by Event ID
- Review event distribution

## KQL Query

```kusto
SecurityEvent
| where TimeGenerated > ago(24h)
| summarize EventCount=count() by EventID
| order by EventCount desc
```

## Expected Result

Display the number of events collected for each Windows Event ID.

## Evidence

### Screenshot:

![Event Count Summary](../screenshots/03-KQL/08-Event-Count.png)


## MITRE ATT&CK

Not Applicable

## Notes

This query was used to validate log collection and confirm that relevant Windows Security Events were available for threat hunting.