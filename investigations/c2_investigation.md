# Command & Control (C2) Investigation

## Summary
Suspicious outbound network activity was detected from a Windows endpoint communicating with an external server. The behavior was consistent with Command and Control (C2) beaconing, likely generated from a Mythic agent during lab simulation.

---

## Detection Details
- **Alert Type:** C2 Beaconing Activity  
- **Log Source:** Sysmon / Elastic Agent  
- **Relevant Events:** Network connections, process creation  
- **Protocol:** HTTP/HTTPS  

---

## Investigation Steps
1. Reviewed network connection logs in Kibana dashboards.  
2. Identified repeated outbound connections to a single external IP/domain.  
3. Analyzed frequency and interval of connections (beaconing pattern).  
4. Correlated activity with process execution on the host.  
5. Verified activity aligned with Mythic C2 simulation.  

---

## Findings
- Regular, periodic outbound connections to a single IP address.  
- Traffic pattern consistent with beaconing behavior.  
- Activity originated from a suspicious process on the endpoint.  
- Behavior matched known Command & Control techniques.  

---

## Response Actions
- Alert generated in SIEM for suspicious outbound traffic.  
- Recommended isolating affected endpoint.  
- Suggested blocking malicious IP/domain at firewall level.  
- Recommended performing full endpoint analysis for persistence mechanisms.  

---

## MITRE ATT&CK Mapping
- **T1071 – Application Layer Protocol**  
- **T1105 – Ingress Tool Transfer**  
- **T1071.001 – Web Protocols**

---

## Conclusion
The activity was identified as simulated C2 communication using Mythic. This demonstrates the ability to detect beaconing behavior and analyze malicious outbound traffic in a SOC environment.

---
