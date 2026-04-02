# C2 Detection Rule

## Description
Detects potential Command & Control (C2) activity by identifying repeated outbound connections to a single external IP address at consistent intervals.

---

## Detection Logic
- Monitor outbound network connections from endpoints  
- Identify repeated connections to the same external IP/domain  
- Look for consistent timing intervals (beaconing behavior)  
- Correlate with suspicious or unknown processes  

---

## Data Sources
- Sysmon Event ID 3 (Network Connections)  
- Elastic Agent telemetry  
- Endpoint network logs  

---

## Indicators
- High frequency outbound connections  
- Regular time intervals between connections  
- Unknown or suspicious destination IP/domain  
- Unusual process initiating connections  

---

## MITRE ATT&CK Mapping
- **T1071 – Application Layer Protocol**  
- **T1071.001 – Web Protocols**

---

## Outcome
This rule helps identify compromised systems communicating with attacker-controlled infrastructure, enabling early detection of C2 activity.

---
