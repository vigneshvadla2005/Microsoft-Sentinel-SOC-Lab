# Failed Logons Across All Accounts

## Purpose

This query provides an overview of failed authentication attempts across all user accounts.

It helps identify which accounts are being targeted most frequently.


## Detection Logic

- Search Windows Security Events
- Filter Event ID 4625
- Group results by account


## KQL Query

```kusto
(Paste your original KQL query here)
```


## Query Explanation

The query summarizes failed logon events for each account and displays the number of authentication failures.

This helps identify accounts that are repeatedly targeted.


## Expected Output

A list of user accounts with the number of failed logon attempts.


## MITRE ATT&CK Mapping

| Technique | ID |
|-----------|----|
| Brute Force | T1110 |
| Valid Accounts | T1078 |


## Evidence

Screenshot:

screenshots/03-KQL/05-Failed-Logons-All-Accounts.png


## Analyst Notes

This query was used during the lab to compare failed authentication activity across multiple user accounts and identify the most frequently targeted accounts.