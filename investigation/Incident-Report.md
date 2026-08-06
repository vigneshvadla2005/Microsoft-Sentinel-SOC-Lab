# Incident Report

## Overview

This report documents the investigation performed after Microsoft Sentinel generated an incident related to repeated failed Windows authentication attempts.

---

## Incident Details

**Platform:** Microsoft Sentinel

**Incident Type:** Authentication Attack

**Status:** Investigated

---

## Timeline

| Time | Activity |
|------|----------|
| Alert Generated | Analytics Rule Triggered |
| Investigation Started | Security Events Reviewed |
| Threat Hunting | KQL Queries Executed |
| Investigation Completed | Findings Documented |

---

## Evidence Reviewed

- Windows Security Events
- Microsoft Sentinel Incident
- KQL Query Results
- Event Timeline
- Source IP Address

---

## Root Cause

Repeated failed authentication attempts were generated from a single source IP address.

The investigation found no evidence that the attacker successfully authenticated.

---

## Analyst Recommendation

- Continue monitoring failed authentication attempts.
- Review authentication policies.
- Monitor repeated activity from the same source IP.

---

## Outcome

The incident was investigated successfully and documented for future reference.