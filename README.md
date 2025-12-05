# soc-analyst-portfolio
Fictional SOC incident reports and security analysis examples created to demonstrate cybersecurity skills.

SOC Analyst Portfolio

Fictional security operations tickets, Splunk queries, and analysis examples.
============

 Overview

This repository contains fictional SOC (Security Operations Centre) incident reports, sample Splunk detection queries, and security analysis examples created to demonstrate my understanding of:

Security alert triage

SIEM analysis (Splunk, Sentinel concepts)

Incident documentation and reporting

Threat detection logic

Malware/suspicious behaviour investigation

MITRE ATT&CK mapping

Lateral movement & authentication anomaly detection

All examples are entirely fictional with no real organisational data.
The goal of this repository is to show how I would approach SOC Analyst or Blue Team tasks in a professional environment.

Repository Structure
soc-analyst-portfolio/
│
├── tickets/
│   ├── impossible-travel-ticket.md
│   ├── malware-ticket.md
│   ├── password-spray-ticket.md
│   ├── phishing-ticket.md
│   └── smb-lateral-movement-ticket.md
│
├── splunk-queries/
│   ├── authentication-queries.md
│   ├── malware-and-edr-queries.md
│   └── lateral-movement-queries.md
│
└── README.md
================================================

 What This Portfolio Demonstrates
 
 1. SOC Incident Triage Skills

Each ticket shows how I would:

Interpret SIEM/EDR alerts

Investigate authentication anomalies

Identify suspicious processes and behaviour

Recognise phishing, credential harvesting, and malware activity

Recommend containment and remediation steps

Document evidence and decisions clearly

The tickets mimic real SOC workflows from:

Splunk

Microsoft Sentinel

CrowdStrike Falcon

Microsoft Defender

Standard IR processes
=======================

 2. SIEM Analysis & Splunk Querying

The splunk-queries/ folder contains examples of detection and hunting queries for:

Impossible travel

Password sprays

PowerShell malware execution

SMB enumeration

Phishing detection

Lateral movement behaviour

These demonstrate understanding of:

Search logic

Aggregations

Correlation rules

Log source awareness
======================

🧠 3. MITRE ATT&CK Awareness

Many tickets reference behaviours such as:

T1078 – Valid Accounts

T1059 – Command & Scripting Interpreter

T1135 – Network Share Discovery

T1110 – Brute Force

T1566 – Phishing

This shows knowledge of attacker techniques and how SOC teams use ATT&CK to classify incidents.
========================
Sample Ticket Scenarios Included

The repository currently includes the following fictional incidents:

 Impossible Travel Sign-In (Credential Compromise Suspected)

 Malware Dropper via Obfuscated PowerShell Command

 Password Spray Attempt via External VPN Portal

Phishing Email with Credential Harvesting Link

Suspicious SMB Enumeration Suggesting Lateral Movement

More scenarios may be added, including:

Ransomware early-stage activity

Cloud security alerts (AWS/Azure)

Endpoint privilege escalation

DNS tunnelling detection

🧭 Purpose of This Repository

This repository exists to:

Demonstrate SOC Analyst capability

Showcase my written communication and analytical process

Provide examples of how I would document and investigate security alerts

Build a public record of my security learning journey

Serve as a portfolio piece for cybersecurity job applications

It does not represent real incidents, real customers, or confidential information.

 Future Additions

I plan to expand this portfolio with:

Additional Splunk & Sentinel queries

Sigma rules

Threat hunting playbooks

MITRE ATT&CK mappings per ticket

Small datasets of example logs

Blue Team remediation notes

Visual diagrams of investigation workflows

📫 Contact

If you're viewing this as part of a job application or recruitment process, you're welcome to reach out via GitHub or LinkedIn.
