# Microsoft Sentinel SOC Lab Architecture

## Overview

This architecture represents the data flow used throughout the lab.

Windows Security Events generated on the virtual machine are collected through Azure Monitor Agent and stored in Log Analytics Workspace. Microsoft Sentinel uses these logs for threat hunting, analytics rule creation, incident generation, and security investigations.

## Components

- Windows Virtual Machine
- Azure Monitor Agent
- Log Analytics Workspace
- Microsoft Sentinel
- KQL Queries
- Analytics Rules
- Incidents
- Investigation

## Data Flow

1. Windows generates Security Events.
2. Azure Monitor Agent forwards logs.
3. Log Analytics stores the collected events.
4. Microsoft Sentinel analyzes the logs.
5. KQL queries identify suspicious activity.
6. Analytics Rules generate incidents.
7. Incidents are investigated using Sentinel.