# RDP Brute Force Detection Rule

## Description
Detects multiple failed Remote Desktop Protocol (RDP) login attempts, which may indicate a brute force attack targeting a Windows system.

---

## Detection Logic
- Monitor Windows Security Event Logs  
- Filter for Event ID 4625 (failed logon attempts)  
- Identify multiple failed attempts from a single IP address  
- Apply threshold (e.g., 5+ failed attempts within a short timeframe)  

---

## Data Sources
- Windows Security Logs  
- Elastic Agent / Sysmon telemetry  
- RDP authentication logs  

---

## Indicators
- Multiple failed login attempts  
- Same source IP across attempts  
- High frequency of authentication failures  
- Possible follow-up success event (Event ID 4624)  

---

## MITRE ATT&CK Mapping
- **T1110 – Brute Force**  
- **T1021.001 – Remote Services: Remote Desktop Protocol**

---

## Outcome
This rule enables detection of unauthorized access attempts and helps prevent account compromise through brute force attacks.

---
