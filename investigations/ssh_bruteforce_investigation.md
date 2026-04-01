# SSH Brute Force Investigation

## Summary
Detected multiple failed SSH login attempts from a single IP address.

## Steps Taken
- Reviewed authentication logs in Kibana
- Identified repeated failed login attempts
- Correlated timestamps and source IP

## Findings
- High volume of failed attempts indicates brute force attack

## Response
- Alert triggered
- Recommended blocking IP and enforcing stronger authentication

## MITRE ATT&CK
- T1110 – Brute Force
