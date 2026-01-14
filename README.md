# SSH Hardening & Host Security Lab (Ubuntu)
## Overview
This project demonstrates the deployment, 
hardening, and validation of a Linux server with a 
focus on securing SSH access and reducing attack 
surface. The lab simulates a real-world defensive 
security task and documents each step from 
reconnaissance to remediation. The goal of this 
project is to show practical, hands-on experience 
with system hardening, network scanning, and 
security documentation in a version-controlled 
environment. ---
## Environment
- **OS:** Ubuntu 24.04 LTS - **Server Type:** 
Cloud-hosted Linux VM - **Access Method:** SSH 
(key-based authentication) - **Firewall:** UFW ---
## Scope
- Secure SSH service - Restrict network access 
using firewall rules - Validate security controls 
using network scanning - Document findings and 
remediation actions Out of scope: - Web application 
security - Active exploitation of production 
systems ---
## Tools Used
- **OpenSSH** - **UFW (Uncomplicated Firewall)** - 
**Nmap** - **Git / GitHub** - **Termius (iOS SSH 
client)** ---
## Methodology
### 1. Host Discovery
Performed host discovery and port scanning to 
identify exposed services. Artifacts: - 
`scans/host_discovery.txt` - 
`scans/full_port_scan.txt` ---
### 2. Service Enumeration
Enumerated SSH service configuration and 
authentication methods. Artifacts: - 
`scans/ssh_port_post_firewall.txt` - 
`scans/ssh_auth_post_firewall.txt` ---
### 3. Hardening Actions
- Enabled UFW firewall - Allowed SSH explicitly 
before firewall activation - Restricted access to 
required ports only - Verified key-based SSH 
authentication ---
### 4. Validation
Post-hardening scans were conducted to confirm: - 
Only intended ports were accessible - SSH 
authentication methods were restricted - Firewall 
rules were active and enforced ---
## Findings Summary
| Finding | Risk Level | Mitigation | 
|------|-----------|-----------|
| SSH exposed prior to firewall enforcement | 
| Medium | UFW enabled with explicit SSH allow rule 
| |
| Lack of rate limiting on SSH | Low | UFW rate 
| limiting applied | Default SSH exposure | 
| Informational | Validated and documented |
---
## Outcome
The server was successfully hardened with 
restricted network exposure and validated through 
post-remediation scanning. All changes were 
documented and tracked using Git for 
reproducibility and auditability. ---
## Key Takeaways
- Importance of firewall rule ordering - Verifying 
changes with post-hardening scans - Documenting 
security work clearly for audit and review - Using 
version control to track security configurations 
---
## Disclaimer
This project was conducted in a controlled lab 
environment on infrastructure owned by the author.
No unauthorized systems were targeted.
