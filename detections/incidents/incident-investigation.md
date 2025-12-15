# Incident Investigation – Brute Force Detection

## Incident Summary
- Detection: Brute Force Detection
- Severity: Medium
- MITRE ATT&CK: Credential Access
- Data Source: Windows Security Events

## Detection Logic
Multiple failed login attempts (Event ID 4625) within a short time window.

## Investigation Steps
1. Opened Microsoft Sentinel Incidents
2. Reviewed alert timeline
3. Validated failed login attempts
4. Identified affected host

## Conclusion
This was a simulated brute force attack performed in a lab environment.
