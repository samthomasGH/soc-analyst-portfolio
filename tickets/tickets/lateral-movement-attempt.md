Suspicious Lateral Movement Attempt (SMB Enumeration)

Ticket ID: SEC-2025-052
Severity: High
Incident Type: Lateral Movement – SMB Enumeration
Detected By: Splunk Correlation Rule + EDR (CrowdStrike)
Status: In Progress

1. Summary

Splunk detected a high volume of SMB enumeration requests originating from workstation WS-303, targeting 42 internal hosts. CrowdStrike flagged abnormal net.exe usage. This behaviour suggests reconnaissance consistent with early-stage lateral movement.

2. Event Details

Source host: WS-303

User: a.hughes (no admin privileges)

Command observed:

net view \\10.10.14.12

net view /domain

net use attempts

Volume: 120+ discovery commands within 6 minutes

Network behaviour:

SMB traffic spikes to multiple hosts

Kerberos TGT requests failed 11 times

EDR: High-risk behaviour tag applied

3. IOCs

SMB enumeration pattern matches MITRE ATT&CK T1135

High volume credential validation failures

Suspicious net.exe execution chain

Some targeted hosts include domain controllers

4. Triage Performed

Verified user claims they were not performing any network scanning

Reviewed browser history — user downloaded a suspicious “PDF converter” EXE earlier today

Sandbox of EXE shows potential dropper behaviour (trojanised installer)

Checked other hosts for similar behavioural patterns (none found)

5. Containment Actions

Fully isolated workstation WS-303 via EDR

Disabled user account

Quarantined downloaded EXE samples

Blocked domain of EXE origin

Alerted IT Ops to review domain controller logs immediately

6. Remaining Risk

Unknown if malware escalated privileges

Unknown if credentials were stolen and reused

Possible early-stage ransomware pre-enumeration

Possible need for domain-wide credential hygiene check

7. Recommendations

Re-image WS-303

Force password resets across impacted user groups

Perform a golden ticket / Kerberos check on DCs

Run script to detect any implanted scheduled tasks or persistence mechanisms

Add detection rules for further SMB enumeration behaviour

8. Next Steps

Escalated to Incident Response for deeper malware analysis and domain compromise investigation.
