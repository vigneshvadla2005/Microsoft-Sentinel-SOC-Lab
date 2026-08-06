# Indicator of Compromise (IOC) Analysis

## Purpose

The objective of this analysis was to identify indicators associated with the detected authentication activity.

---

## Indicators Reviewed

### Source IP Address

Used to identify the origin of failed authentication attempts.

---

### Target User Accounts

Multiple Windows accounts targeted during the attack simulation.

---

### Event IDs

4625 — Failed Logon

4624 — Successful Logon

4688 — Process Creation

---

### Hostname

Windows Virtual Machine

---

### Timestamp

Reviewed authentication sequence to determine attack timing.

---

## Analysis

The source IP generated repeated authentication failures across multiple accounts.

No successful compromise was identified during the investigation.

---

## MITRE ATT&CK

- T1110 — Brute Force

---

## Conclusion

The collected indicators supported the conclusion that the observed activity represented a brute-force authentication attempt rather than legitimate user behavior.