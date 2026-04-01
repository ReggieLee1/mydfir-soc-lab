# SSH Brute Force Detection Rule

## Description
Detects multiple failed SSH login attempts from a single IP.

## Logic
- Event: Failed SSH login
- Threshold: 5+ attempts within short timeframe

## MITRE ATT&CK
- T1110 – Brute Force

## Outcome
Helps identify potential unauthorized access attempts.
