Ticket 4 — Phishing Email With Credential Harvesting Link

Ticket ID: SEC-2025-041
Severity: Medium
Incident Type: Phishing Attempt – Credential Harvesting
Detected By: Microsoft Defender for Office 365 (Safe Links)
Status: Closed

1. Summary

A phishing email impersonating Microsoft SharePoint was delivered to 14 users across the Sales department. Safe Links rewrote the URL and blocked the landing page on click, preventing credential theft.

2. Event Details

Sender: “SharePoint Notifications” noreply@sharepoint-updates.com

Recipients: 14 (Sales)

Subject: “Important: Your Shared Document Has Been Updated”

Link Target: hxxps://sharepoint-document-review[.]com/login

Clicks: 3 users clicked, all blocked by Safe Links

Attachment: None (link-only attack)

3. IOCs

URL flagged as phishing infrastructure

Domain registered 48 hours ago via NameCheap

IP hosted in bulletproof hosting provider

Same domain appears in threat intel feeds for 2 other organisations this week

4. Triage Performed

Checked mail flow logs: no additional recipients

Verified that no credentials were entered (Safe Links blocked access)

Reviewed Azure AD sign-in logs for affected users — no unusual logins

Queried SIEM for login attempts to the malicious domain — none

5. Containment Actions

Added domain to organisation block list

Initiated phishing awareness follow-up with affected users

Reported URL to Microsoft and external threat feeds

Created a detection rule for future emails from similar lookalike domains

6. Remaining Risk

Users may receive follow-up attacks

Attacker may shift to other lures or bypass Safe Links

Sales team historically has lower phishing training scores

7. Recommendations

Conduct a targeted phishing simulation against the Sales team

Implement stricter domain similarity filtering

Encourage MFA reset for any user who clicked (optional precaution)

8. Next Steps

Ticket closed. Logged as part of weekly phishing trend report.
