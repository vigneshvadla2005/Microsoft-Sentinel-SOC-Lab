# Process Creation Detection Rule

## Overview

This Analytics Rule monitors Windows process creation events to improve visibility into application execution within the monitored endpoint.

Windows Security Event ID 4688 provides valuable information about newly created processes and can help identify suspicious command execution.

---

## Objective

- Monitor process execution
- Detect unusual command activity
- Support threat hunting
- Improve endpoint visibility

---

## Data Source

- Microsoft Sentinel
- Windows Security Events

---

## Event ID

- 4688 – Process Creation

---

## Detection Logic

The Analytics Rule continuously monitors Windows Event ID 4688 and generates alerts whenever configured conditions are matched.

This information assists analysts during incident investigations.

---

## Expected Outcome

The rule provides detailed information about newly created processes including process name, parent process, user account, and execution time.

---

## MITRE ATT&CK

| Technique | ID |
|-----------|----|
| Command and Scripting Interpreter | T1059 |

---

## Investigation Steps

1. Review executed process.
2. Verify parent process.
3. Confirm executing user.
4. Check execution timeline.
5. Investigate suspicious commands if required.

---

## Evidence

### Related KQL Query

[Process-Creation](../kql/Process Creation 4688.md)

### Screenshot

![Process-Creation](../screenshots/03-KQL/03-Process-Creation-4688.png)

---

## Conclusion

Monitoring process creation events improves visibility into endpoint activity and provides valuable forensic evidence during investigations.