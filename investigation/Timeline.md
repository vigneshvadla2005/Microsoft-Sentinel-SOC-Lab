# Incident Timeline

## Investigation Timeline

| Step | Description |
|------|-------------|
| 1 | Windows Security Events collected |
| 2 | Failed authentication events generated |
| 3 | Azure Monitor Agent forwarded logs |
| 4 | Log Analytics Workspace received events |
| 5 | Microsoft Sentinel analyzed incoming logs |
| 6 | Analytics Rule detected repeated failures |
| 7 | Security Incident created automatically |
| 8 | KQL queries executed for investigation |
| 9 | Source IP analyzed |
| 10 | Investigation completed |
| 11 | Findings documented |

---

## Investigation Workflow

Windows Security Events

↓

Azure Monitor Agent

↓

Log Analytics Workspace

↓

Microsoft Sentinel

↓

Analytics Rule

↓

Incident

↓

Threat Hunting

↓

Investigation

↓

Documentation

---

## Conclusion

The investigation followed a structured SOC workflow from event collection through incident analysis and final documentation.