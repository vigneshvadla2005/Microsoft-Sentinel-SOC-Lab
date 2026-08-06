# Detection Engineering

## Overview

Detection engineering focuses on creating security detections that identify suspicious activity while reducing unnecessary alerts.

During this project, custom Analytics Rules were created using KQL queries to automate the detection of common Windows security events.

---

## Detection Rules Created

- Multiple Failed Logins
- Successful Logons
- Process Creation Monitoring
- Suspicious IP Activity

---

## Detection Process

Windows Security Events

↓

KQL Query

↓

Analytics Rule

↓

Incident Generation

↓

SOC Investigation

---

## Event IDs Used

| Event ID | Description |
|----------|-------------|
| 4624 | Successful Logon |
| 4625 | Failed Logon |
| 4688 | Process Creation |

---

## Benefits

- Faster detection
- Reduced manual log analysis
- Consistent alert generation
- Improved investigation workflow

---

## Conclusion

Building Analytics Rules provided practical experience in converting raw Windows security logs into actionable security incidents.