# Threat-Hunting-Threat-Mapping-Manufacturing-Industry
This project demonstrates a threat hunting and threat intelligence exercise focused on the manufacturing sector. Using threat intelligence gathered from SocRadar, I analyzed threat actors and techniques commonly associated with attacks against manufacturing organizations and mapped their activities to the MITRE ATT&amp;CK Framework.
The purpose of this exercise was to understand how threat actors operate, identify overlapping attack techniques, and develop threat hunting hypotheses that can be used to proactively detect malicious activity within manufacturing environments.

# Objectives
- Analyze threat actors targeting manufacturing organizations.
- Identify common adversary tactics, techniques, and procedures (TTPs).
- Map identified threats to the MITRE ATT&CK Framework.
- Assess potential risks to manufacturing operations.
- Develop threat hunting hypotheses for detection and response activities.

---
## Threat Intelligence Source

**Platform Used:** SocRadar

The threat intelligence collected from SocRadar was used to identify active threat actors, attack patterns, and techniques relevant to the manufacturing industry.

---

## Threat Actors Analyzed

### Turla

Turla is a sophisticated Advanced Persistent Threat (APT) group known for cyber espionage campaigns, credential theft, persistence mechanisms, and long-term access to victim environments.

### Gold Southfield

Gold Southfield is a financially motivated threat group known for targeting organizations through credential theft, privilege escalation, and unauthorized access techniques.

### SAFE

SAFE-related activities commonly involve the exploitation of weak security controls, exposed credentials, and unauthorized access to critical business systems.

---

## MITRE ATT&CK Mapping

### Technique: T1552 – Unsecured Credentials

**Tactic:** Credential Access

#### Description

Adversaries may search for credentials stored in insecure locations such as:

- Configuration files
- Scripts
- Shared network drives
- Cloud storage repositories
- Backup files
- Local workstation files

These credentials can then be used to gain unauthorized access, establish persistence, and move laterally throughout the environment.

---

## Threat Overlap Analysis

During the threat mapping exercise, an overlap was identified between:

- Turla
- Gold Southfield
- SAFE

All three threat profiles demonstrated activity associated with **MITRE ATT&CK T1552 – Unsecured Credentials**.

This analysis revealed that credential exposure remains one of the most common attack vectors leveraged by threat actors targeting manufacturing organizations.

The overlap demonstrates how different threat actors can employ similar techniques to achieve their objectives, regardless of whether their motivations are espionage, financial gain, or unauthorized access.

---

## Manufacturing Industry Impact

Manufacturing organizations are particularly vulnerable to credential-based attacks due to:

- Legacy systems and applications
- Operational Technology (OT) environments
- Shared administrative accounts
- Service accounts with elevated privileges
- Weak credential management practices
- Flat network architectures

If exploited, unsecured credentials can provide attackers with access to:

- Production systems
- Industrial Control Systems (ICS)
- Engineering workstations
- Enterprise Resource Planning (ERP) systems
- Intellectual property
- Sensitive operational data

---

## Threat Hunting Hypotheses

### Hypothesis 1

Threat actors may be searching network shares, configuration files, and repositories for unsecured credentials associated with manufacturing systems.

### Hypothesis 2

Compromised service account credentials may be used to facilitate lateral movement between IT and OT environments.

### Hypothesis 3

Attackers may leverage harvested credentials to access remote administration tools and privileged systems.

### Hypothesis 4

Legacy manufacturing applications may contain hardcoded credentials that could be exploited by adversaries.

---

## Detection Opportunities

### Authentication Monitoring

Monitor for:

- Multiple failed login attempts
- Logins from unusual locations
- Privileged account misuse
- Service account anomalies

### File Access Monitoring

Monitor access to:

- Configuration files
- Backup repositories
- Password vault exports
- Administrative scripts

### Security Event Monitoring

| Event ID | Description |
|-----------|------------|
| 4624 | Successful Logon |
| 4625 | Failed Logon |
| 4648 | Explicit Credential Use |
| 4672 | Special Privileges Assigned |

---

## Key Findings

- Credential exposure remains a significant cybersecurity risk within manufacturing environments.
- Multiple threat actors leverage MITRE ATT&CK Technique T1552 to gain initial access and establish persistence.
- Legacy systems and Operational Technology environments increase the attack surface.
- Proactive threat hunting can improve detection capabilities and reduce attacker dwell time.
- Threat intelligence and MITRE ATT&CK mapping provide valuable insight into adversary behavior and likely attack paths.

---

## Recommendations

### Identity & Access Management

- Enforce Multi-Factor Authentication (MFA)
- Implement Privileged Access Management (PAM)
- Review service account permissions regularly
- Eliminate shared administrative accounts

### Credential Security

- Remove plaintext credentials from systems
- Secure configuration files
- Use password vault solutions
- Rotate privileged credentials regularly

### Network Security

- Segment IT and OT environments
- Restrict administrative access
- Monitor lateral movement activity
- Implement least privilege access controls

### Continuous Monitoring

- Conduct regular threat hunting exercises
- Monitor threat intelligence feeds
- Continuously map threats to MITRE ATT&CK
- Develop detection rules aligned with adversary TTPs

---

## Skills Demonstrated

- Threat Hunting
- Threat Intelligence Analysis
- MITRE ATT&CK Mapping
- Adversary TTP Analysis
- Cyber Threat Modeling
- Manufacturing Industry Risk Assessment
- Security Monitoring
- Detection Engineering
- Risk-Based Security Analysis

---

## Tools Used

- SocRadar
- MITRE ATT&CK Framework
- Threat Intelligence Research
- Threat Mapping Methodology

---

## Conclusion

This project demonstrates how threat intelligence can be leveraged to identify adversary behaviors, map attack techniques, and develop actionable threat hunting activities. By analyzing the overlap between Turla, Gold Southfield, SAFE, and MITRE ATT&CK Technique T1552 (Unsecured Credentials), I identified a common attack vector that poses significant risk to manufacturing organizations and developed detection-focused recommendations to improve cybersecurity resilience.

---

## Author

**Adesola Boris**

Senior Internal Auditor | IT Audit | Cybersecurity Professional

Focused on Cybersecurity, Threat Hunting, Threat Intelligence, IT Risk Management, and Security Governance.
