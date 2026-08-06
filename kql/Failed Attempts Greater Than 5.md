# Failed Attempts Greater Than 5

## Purpose

This query identifies accounts or source IP addresses with more than five failed logon attempts within the selected time range.

Repeated failed authentication attempts may indicate password guessing or brute-force activity.


## Detection Logic

- Search Windows Security Events
- Filter Event ID 4625
- Count failed logon attempts
- Display only accounts or IP addresses with more than five failures


## KQL Query

```kusto
(Paste your original KQL query here)
```


## Query Explanation

This query summarizes failed logon events and counts the number of failed attempts for each account and source IP address.

Only results with more than five failed logons are displayed.


## Expected Output

The output highlights accounts or IP addresses that exceed the defined threshold, helping analysts quickly identify potential brute-force attacks.


## MITRE ATT&CK Mapping

| Technique | ID |
|-----------|----|
| Brute Force | T1110 |


## Evidence

Screenshot:

screenshots/03-KQL/04-Failed-Attempts-GreaterThan5.png


## Analyst Notes

During testing, repeated failed logon attempts generated multiple Event ID 4625 records.

The query successfully identified accounts exceeding the configured threshold and provided a starting point for investigating possible brute-force activity.