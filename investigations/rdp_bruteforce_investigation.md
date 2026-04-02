# RDP Brute Force Investigation

## Summary
An alert was triggered indicating multiple failed Remote Desktop Protocol (RDP) login attempts against a Windows Server. The activity suggested a potential brute force attack originating from a single external IP address.

---

## Detection Details
- **Alert Type:** RDP Brute Force Detection  
- **Log Source:** Windows Security Logs (via Sysmon / Elastic Agent)  
- **Event IDs:** 4625 (Failed Logon)  
- **Protocol:** RDP (TCP Port 3389)  

---

## Investigation Steps
1. Reviewed authentication logs in Kibana dashboards.  
2. Filtered for Event ID 4625 (failed logon attempts).  
3. Identified repeated login failures from a single source IP.  
4. Analyzed timestamps to determine frequency and pattern of attempts.  
5. Checked for any successful login events (Event ID 4624) following failures.  

---

## Findings
- High volume of failed login attempts within a short time frame.  
- Activity originated from a single external IP address.  
- No successful login attempts were observed.  
- Behavior is consistent with automated brute force attack tools.  

---

## Response Actions
- Alert generated in SIEM (Kibana).  
- Recommended blocking the source IP at the firewall.  
- Suggested enforcing account lockout policies.  
- Recommended enabling multi-factor authentication (MFA) for RDP access.  

---

## MITRE ATT&CK Mapping
- **T1110 – Brute Force**  
- **T1021.001 – Remote Services: Remote Desktop Protocol**

---

## Conclusion
The activity was identified as a brute force attack targeting RDP services. While no compromise was confirmed, the event highlights the importance of securing exposed RDP services and implementing stronger authentication controls.

---
