Ticket 3 — Password Spray Attempt

Ticket ID: SEC-2025-033
Priority: Low
Incident Type: Authentication – Failed Login Patterns
Status: Closed
Detected By: Splunk (Correlation Rule: Password Spray Behaviour)

1. Summary

Splunk correlation rule identified multiple failed login attempts across 27 accounts using a small set of common passwords, consistent with a password spray attack.

2. Event Details

Source IP: 103.91.214.19

Pattern: 27 accounts targeted, 3 password variants used

Login source: External VPN portal

Successful logins: 0

Affected departments: Mixed (HR, Sales, Admin)

3. IOCs

IP linked to previous brute-force activity

Identical attack behaviour logged last month from same subnet

4. Triage Performed

Validated no successful authentication

Verified all accounts locked after threshold

Checked VPN logs for abnormal patterns

Confirmed MFA blocked all attempts

5. Containment Actions

Blocked offending IP address at perimeter firewall

Added new rule to VPN for rate-limiting failed attempts

Logged event for trend monitoring

6. Remaining Risk

Attackers may move to other IP ranges

Password policy still allows shorter passwords than recommended

No auto-alert for repeated spray attempts on different days

7. Recommendations

Extend lockout thresholds

Enable continuous behavioural detection on VPN portal

Consider implementing conditional access for external IP ranges

Strengthen password policy to 14+ character minimums

8. Next Steps

Ticket closed. Assigned to Security Engineering for rule tuning.
