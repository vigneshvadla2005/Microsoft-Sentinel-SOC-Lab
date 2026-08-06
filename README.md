# Microsoft Sentinel SOC Lab

## About this project

I created this lab to improve my hands-on skills in Microsoft Sentinel and understand how a SOC analyst detects, investigates, and responds to security incidents in a Windows environment.

Instead of only learning the concepts, I built a working lab where I collected Windows Security Events, wrote KQL queries, created Analytics Rules, generated security incidents, and documented the investigation process with supporting evidence.

This repository contains my KQL queries, detection rules, investigation reports, screenshots, and documentation from the lab.

## Project Goals

The main objectives of this lab were to:

- Learn Microsoft Sentinel through hands-on practice
- Monitor Windows Security Events
- Detect brute-force login attempts
- Investigate Windows Event IDs (4624, 4625, and 4688)
- Write KQL queries for threat hunting
- Create Microsoft Sentinel Analytics Rules
- Investigate generated incidents
- Document each activity with screenshots and evidence


## Repository Structure

Microsoft-Sentinel-SOC-Lab
│
├── detection-rules/     # Microsoft Sentinel Analytics Rules
├── diagrams/            # Architecture diagrams
├── docs/                # Supporting documentation
├── investigation/       # Incident investigation reports
├── kql/                 # KQL hunting queries
├── playbooks/           # Logic Apps / Playbooks
├── screenshots/         # Evidence from the lab
└── README.md


## Lab Workflow

The lab was completed using the following workflow:

1. Created Azure resources and deployed Microsoft Sentinel.
2. Connected a Windows virtual machine to Log Analytics.
3. Enabled Windows Security Event collection.
4. Generated security events inside the virtual machine.
5. Wrote KQL queries to detect suspicious activity.
6. Created Analytics Rules using custom KQL queries.
7. Generated incidents from detection rules.
8. Investigated alerts and reviewed entity information.
9. Documented findings with screenshots and reports.


## Skills Gained

During this project I improved my understanding of:

- Microsoft Sentinel
- Kusto Query Language (KQL)
- Windows Event IDs (4624, 4625, 4688)
- Threat Hunting
- Incident Investigation
- Analytics Rule Creation
- Windows Security Monitoring
- Log Analysis
- MITRE ATT&CK Mapping
- SOC Documentation


## Lab Evidence

The screenshots and documentation in this repository show the practical work completed during the lab.

| Activity | Evidence |
|----------|----------|
| Azure Environment Setup | screenshots/01-Azure |
| Windows Event Viewer | screenshots/02-EventViewer |
| KQL Queries | screenshots/03-KQL |
| Analytics Rules | screenshots/04-AnalyticsRules |
| Incidents | screenshots/05-Incidents |
| Threat Hunting | screenshots/06-ThreatHunting |
| Logic Apps | screenshots/07-LogicApps |
| Sysmon | screenshots/08-Sysmon |
| Investigation | screenshots/09-Investigation |
| Charts | screenshots/10-Charts |


## Technologies Used

### SIEM & Monitoring
- Microsoft Sentinel
- Log Analytics Workspace
- Azure Monitor

### Operating Systems
- Windows 11
- Windows Server
- Kali Linux

### Security Tools
- Windows Event Viewer
- Sysmon
- Microsoft Defender
- Wireshark
- Nmap

### Detection & Monitoring
- KQL (Kusto Query Language)
- Analytics Rules
- Incident Management
- Threat Hunting

### Networking & Security Concepts
- Brute Force Detection
- Windows Event IDs (4624, 4625, 4688)
- Malware Investigation
- Phishing Investigation
- Log Analysis
- MITRE ATT&CK Mapping

## Architecture

The following diagram illustrates the overall architecture of the Microsoft Sentinel SOC lab.

> Diagram will be added after the architecture design is completed.


## MITRE ATT&CK Coverage

The detection rules and hunting queries in this lab focus on techniques commonly observed during Windows security investigations.

| Technique | Description |
|-----------|-------------|
| T1110 | Brute Force |
| T1078 | Valid Accounts |
| T1059 | Command Execution |
| T1055 | Process Injection (Future Work) |
| T1046 | Network Service Discovery |

## What I Learned

Building this lab helped me understand how security analysts investigate Windows events instead of simply reading documentation.

Some key takeaways include:

- Collecting Windows Security Events
- Writing practical KQL hunting queries
- Detecting brute-force attacks
- Investigating incidents in Microsoft Sentinel
- Creating scheduled Analytics Rules
- Mapping activity to MITRE ATT&CK
- Documenting investigations with supporting evidence


## Project Status

This project is actively being improved.

Upcoming updates include:

- Additional KQL hunting queries
- Detection rule documentation
- Investigation reports
- Architecture diagram
- MITRE ATT&CK mapping
- Logic App automation



## Contact

If you'd like to connect or discuss this project, feel free to reach out.

- LinkedIn: https://www.linkedin.com/in/vadla-vignesh
- GitHub: https://github.com/vigneshvadla2005