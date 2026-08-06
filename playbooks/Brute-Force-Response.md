# Brute Force Response Playbook

## Overview

This playbook represents an automated response workflow designed for repeated Windows authentication failures detected by Microsoft Sentinel.

Although this lab focused on detection and investigation, the playbook demonstrates how Microsoft Sentinel can trigger automated actions after an Analytics Rule creates an incident.

---

## Objective

The primary objective of this playbook is to reduce the time required to respond to brute-force authentication attempts.

Automation helps security analysts receive alerts quickly and begin investigations without manually monitoring security events.

---

## Trigger

Microsoft Sentinel Incident

Analytics Rule:

Multiple Failed Logins

---

## Workflow

1. Microsoft Sentinel detects repeated failed authentication attempts.
2. An Analytics Rule creates a security incident.
3. The playbook is triggered.
4. Incident information is collected.
5. The SOC analyst reviews the alert.
6. Investigation begins using KQL queries.

---

## Input

- Incident Name
- Severity
- Source IP Address
- Username
- Timestamp
- Host Name

---

## Expected Actions

- Notify the SOC analyst.
- Record incident information.
- Support investigation activities.
- Maintain consistent response procedures.

---

## Benefits

- Faster response
- Consistent workflow
- Reduced manual effort
- Improved incident handling

---

## Related Files

### Detection Rule

- detection-rules/Multiple-Failed-Logins.md

### Investigation

- investigation/Incident-01-Brute-Force.md

### KQL Query

![Brute-Force-Response](../kql/Failed-Attempts-Greater-Than-5.md)

---

## Conclusion

Automated response workflows help security teams react more quickly to suspicious authentication activity and improve the overall incident response process.