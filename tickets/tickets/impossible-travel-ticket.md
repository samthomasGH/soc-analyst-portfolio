Ticket ID: SEC-2025-001
Priority: High
Incident Type: Suspicious Authentication – Impossible Travel
Status: Closed
Detected By: Microsoft Sentinel (UEBA: Impossible Travel Rule)

1. Summary

Sentinel detected two successful logins for user r.green from geographically distant locations (London, UK and Warsaw, Poland) within 12 minutes, indicating potential credential compromise.

2. Event Details

User: r.green

Department: HR

Privileged Account: No

Login 1: 10:14 UTC — London — 81.25.117.19 — Managed device

Login 2: 10:26 UTC — Warsaw — 185.102.14.55 — Unknown browser

MFA: Token reused; not triggered

Other activity: Accessed HR SharePoint folder; viewed 9 files

3. IOCs

IP 185.102.14.55 associated with medium-risk reputation

Repeated access to HR-sensitive files

Unmanaged device authentication

4. Triage Performed

Confirmed user physically located in London

Reviewed AD sign-in logs and SharePoint access logs

No lateral movement detected

No successful login attempts after the Warsaw event

5. Containment Actions

Forced password reset

Revoked active sessions

Re-enrolled the user in MFA

Alerted HR Manager

6. Remaining Risk

Potential exposure of sensitive HR data

Unknown vector of credential compromise

User may have reused password on external services

7. Recommendations

IT to review outbound data transfer logs

SOC to monitor for further anomalous activity

HR to require password hygiene refresher

Block known malicious IP domain ranges in conditional access

8. Next Steps

Ticket closed after 48 hours of clean monitoring. No further anomalies.
