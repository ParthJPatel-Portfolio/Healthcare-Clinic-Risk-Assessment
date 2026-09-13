# CIS Controls Implementation Mapping

This document maps CIS Critical Security Controls v8.1 to specific risks and threat events identified in the SAMP Walk-in Clinic Risk Assessment.

---

## CIS Control 3: Data Protection

**Group Category:** Protective Technology  
**Implementation Level:** IG1, IG2, IG3

### Safeguards Implemented

#### 3.6 - Encrypt Data on End-User Devices
- **Assets Protected:** Laptops, tablets, smartphones, employee devices
- **Threats Mitigated:** Data theft from lost/stolen devices
- **Threat Events:** Malware infection via USB, device misplacement

#### 3.10 - Encrypt Sensitive Data in Transit
- **Assets Protected:** Telemedicine platform, email system, cloud connections
- **Threats Mitigated:** Man-in-the-middle attacks, credential theft
- **Threat Events:** Unencrypted communication channels, wireless attacks
- **Implementation:** TLS/SSL for all external communications

#### 3.11 - Encrypt Sensitive Data at Rest
- **Assets Protected:** EHR database, cloud storage, financial records
- **Threats Mitigated:** Unauthorized access to stored PHI/PII
- **Threat Events:** Data breaches, ransomware attacks, malware access
- **Implementation:** AES-256 encryption for all sensitive data stores

#### 3.13 - Deploy Data Loss Prevention Solution
- **Assets Protected:** All data systems, email, network egress points
- **Threats Mitigated:** Unauthorized data exfiltration, insider threats
- **Threat Events:** Supply chain attacks on billing system, credential theft
- **Implementation:** Monitor and block unauthorized data transfers

---

## CIS Control 4: Secure Configuration

**Group Category:** Protective Technology  
**Implementation Level:** IG1, IG2, IG3

### Safeguards Implemented

#### 4.2 - Establish Secure Configuration Process for Infrastructure
- **Assets Protected:** Network infrastructure, cloud services, servers
- **Threats Mitigated:** Misconfiguration attacks, malware propagation
- **Threat Events:** Lateral movement after initial breach, DDoS

#### 4.3 - Configure Automatic Session Locking
- **Assets Protected:** Workstations, receptionist desktops, medical devices
- **Threats Mitigated:** Unauthorized access to unattended systems
- **Threat Events:** Patient viewing colleague's PHI, receptionist workstation access
- **Implementation:** Auto-lock after 5-15 minutes inactivity

#### 4.11 - Enforce Remote Wipe Capability
- **Assets Protected:** Mobile devices (tablets, phones)
- **Threats Mitigated:** Data loss from lost/stolen mobile devices
- **Threat Events:** Device misplacement with EHR access

---

## CIS Control 5: Identity & Access Management

**Group Category:** Security Foundational Skills  
**Implementation Level:** IG1, IG2, IG3

### Safeguards Implemented

#### 5.2 - Use Unique Passwords
- **Assets Protected:** All user accounts (systems, cloud, applications)
- **Threats Mitigated:** Credential-based attacks, password reuse compromise
- **Threat Events:** Malicious insider attacks, phishing credential theft
- **Password Policy:** 
  - Minimum 14 characters
  - Mix of uppercase, lowercase, numbers, special characters
  - No reuse of previous 10 passwords
  - Quarterly password rotation

---

## CIS Control 6: Access Control Management

**Group Category:** Security Foundational Skills  
**Implementation Level:** IG1, IG2, IG3

### Safeguards Implemented

#### 6.1 - Establish Access Granting Process
- **Assets Protected:** Server rooms, physical data centers, secure facilities
- **Threats Mitigated:** Unauthorized physical access, sabotage
- **Threat Events:** Riot damage to equipment, unauthorized system access
- **Implementation:** 
  - Role-based access control (RBAC) matrix
  - Manager approval workflow
  - Quarterly access reviews

#### 6.5 - Require MFA for Administrative Access
- **Assets Protected:** Active Directory, cloud admin accounts, EHR admin accounts
- **Threats Mitigated:** Unauthorized privilege escalation, credential compromise
- **Threat Events:** Insider privilege escalation, phishing targeting admins
- **Implementation:** TOTP (Time-based One-Time Password) or hardware tokens
- **Applicability:** All administrative accounts, super-user access

#### 6.8 - Define and Maintain Role-Based Access Control
- **Assets Protected:** All systems, applications, data repositories
- **Threats Mitigated:** Unauthorized access, lateral movement, insider threats
- **Threat Events:** Negligent misconfiguration, malicious data access
- **Roles Defined:**
  - **Physicians** - Full EHR access, medical records, prescriptions
  - **Nurses** - Patient care records, medication administration
  - **Receptionists** - Scheduling, basic patient demographics
  - **Administrators** - User management, audit logs
  - **IT Staff** - System maintenance, configuration management

---

## CIS Control 7: Software & Service Acquisition Management

**Group Category:** Protective Technology  
**Implementation Level:** IG1, IG2, IG3

### Safeguards Implemented

#### 7.4 - Perform Automated Application Patch Management
- **Assets Protected:** All software, operating systems, cloud applications
- **Threats Mitigated:** Exploitation of known vulnerabilities
- **Threat Events:** Printer firmware exploitation, IoT thermostat compromise
- **Schedule:** 
  - Critical patches: within 48 hours
  - High-priority: within 2 weeks
  - Medium: within 4 weeks

#### 7.5 - Perform Automated Vulnerability Scans
- **Assets Protected:** Network, applications, endpoints, cloud services
- **Threats Mitigated:** Discovery of unpatched vulnerabilities
- **Threat Events:** Malware propagation paths, lateral movement
- **Frequency:** Weekly scans, continuous monitoring

#### 7.7 - Remediate Detected Vulnerabilities
- **Assets Protected:** All IT infrastructure
- **Threats Mitigated:** Exploitation of known weaknesses
- **Process:** Vulnerability > Severity Assessment > Remediation > Verification

---

## CIS Control 8: Security Monitoring & Incident Response

**Group Category:** Protective Technology  
**Implementation Level:** IG1, IG2, IG3

### Safeguards Implemented

#### 8.2 - Collect Audit Logs
- **Assets Protected:** All systems, network, applications, data access
- **Threats Mitigated:** Detection of unauthorized access, attack investigation
- **Threat Events:** Insider data theft, malware activity, privilege escalation
- **Logs Collected:**
  - User login/logout events
  - File access and modifications
  - Administrative actions
  - Network traffic (firewall logs)
  - Cloud activity logs

#### 8.5 - Collect Detailed Audit Logs
- **Assets Protected:** Critical systems (EHR, prescriptions, billing, AD)
- **Threats Mitigated:** Forensic analysis of security incidents
- **Data Logged:**
  - Who accessed the data
  - When it was accessed
  - What data was accessed
  - What changes were made
  - Source IP address

#### 8.11 - Conduct Audit Log Reviews
- **Assets Protected:** All monitored systems
- **Threats Mitigated:** Detection of suspicious patterns, insider threats
- **Frequency:** Daily automated alerts, weekly manual review
- **Triggers:** Unusual access patterns, failed login attempts, privilege changes

---

## CIS Control 9: Email & Web Browser Protections

**Group Category:** Protective Technology  
**Implementation Level:** IG1, IG2, IG3

### Safeguards Implemented

#### 9.3 - Maintain Network-Based URL Filters
- **Assets Protected:** Network perimeter, user devices
- **Threats Mitigated:** Phishing attacks, malware downloads
- **Threat Events:** Social engineering targeting physicians/staff
- **Filtering:** Blocks known malicious sites, suspicious domains

#### 9.6 - Block Unnecessary File Types
- **Assets Protected:** Email system, network ingress
- **Threats Mitigated:** Malware delivery via email attachments
- **Blocked Extensions:** .exe, .zip, .bat, .cmd, and other executable types
- **Alternative:** Encrypted cloud storage links for legitimate file transfers

---

## CIS Control 10: Malware & Unwanted Software Defense

**Group Category:** Protective Technology  
**Implementation Level:** IG1, IG2, IG3

### Safeguards Implemented

#### 10.3 - Disable Autorun & Autoplay
- **Assets Protected:** All end-user devices, network infrastructure
- **Threats Mitigated:** Malware propagation via USB drives
- **Threat Events:** USB drive malware infections
- **Implementation:** Disable autorun on all Windows systems

#### 10.5 - Enable Anti-Exploitation Features
- **Assets Protected:** Applications, operating systems
- **Threats Mitigated:** Exploitation of memory vulnerabilities
- **Threat Events:** Malware delivery, ransomware infection
- **Techniques:** ASLR, DEP, CFG enabled on all systems

---

## CIS Control 11: Data Recovery & Resilience

**Group Category:** Protective Technology  
**Implementation Level:** IG1, IG2, IG3

### Safeguards Implemented

#### 11.1 - Establish Data Recovery Process
- **Assets Protected:** All critical data and systems
- **Threats Mitigated:** Data loss from ransomware, disasters, failures
- **Plan Includes:**
  - Recovery time objective (RTO): 4 hours for critical systems
  - Recovery point objective (RPO): 1 hour for EHR data
  - Step-by-step recovery procedures
  - Regular testing (quarterly)

#### 11.2 - Perform Automated Backups
- **Assets Protected:** EHR database, medical records, billing system
- **Threats Mitigated:** Ransomware attacks, data loss
- **Schedule:** 
  - Hourly incremental backups
  - Daily full backups
  - Weekly offsite backups
- **Retention:** 30 days for daily, 1 year for weekly

#### 11.3 - Protect Recovery Data
- **Assets Protected:** Backup infrastructure
- **Threats Mitigated:** Backup compromise during disaster recovery
- **Implementation:**
  - Geographically separated backup sites
  - Encrypted backup storage
  - Access controls on backup systems
  - Regular restore testing

---

## CIS Control 12: Network Infrastructure Management

**Group Category:** Protective Technology  
**Implementation Level:** IG1, IG2, IG3

### Safeguards Implemented

#### 12.6 - Use Secure Network Management & Communication Protocols
- **Assets Protected:** Network infrastructure, administrative access
- **Threats Mitigated:** Network-based attacks on management systems
- **Protocols:** SSH for remote access, TLS for management interfaces
- **Deprecated:** Telnet, HTTP for administrative functions

#### 12.8 - Establish Dedicated Computing Resources for Administration
- **Assets Protected:** Administrative systems, network infrastructure
- **Threats Mitigated:** Admin account compromise affecting clinical systems
- **Implementation:** 
  - Separate admin workstations
  - Dedicated admin network segment
  - Restricted access to clinical systems

---

## CIS Control 13: Network Monitoring & Defense

**Group Category:** Protective Technology  
**Implementation Level:** IG1, IG2, IG3

### Safeguards Implemented

#### 13.1 - Centralize Security Event Alerting
- **Assets Protected:** All network and security devices
- **Threats Mitigated:** Real-time detection of attacks
- **Implementation:** SIEM (Security Information & Event Management)
- **Alert Types:** DDoS, intrusion attempts, policy violations, anomalies

#### 13.4 - Perform Traffic Filtering Between Network Segments
- **Assets Protected:** Network segments, critical systems
- **Threats Mitigated:** Lateral movement, DDoS, data exfiltration
- **Techniques:**
  - Network segmentation (clinical, admin, guest networks)
  - Access control lists (ACLs) between segments
  - Geo-blocking of known attack sources
  - IP blacklisting of malicious IPs

#### 13.8 - Deploy Network Intrusion Prevention Solution
- **Assets Protected:** Network perimeter, internal networks
- **Threats Mitigated:** Network-based attacks, malware transmission
- **Threat Events:** DDoS, malware delivery, exploit attempts
- **Technology:** IPS (Intrusion Prevention System) at network perimeter

#### 13.10 - Perform Application Layer Filtering
- **Assets Protected:** Web applications, APIs, cloud services
- **Threats Mitigated:** Web-based attacks, API exploitation
- **Threat Events:** SQL injection, XSS, API abuse, data exfiltration
- **Implementation:** WAF (Web Application Firewall)

---

## CIS Control 14: Security Awareness & Training

**Group Category:** Security Foundational Skills  
**Implementation Level:** IG1, IG2, IG3

### Safeguards Implemented

#### 14.2 - Train Workforce Members to Recognize Social Engineering Attacks
- **Target Audience:** All staff (physicians, nurses, admin, IT)
- **Threats Mitigated:** Phishing attacks, whaling attacks, social engineering
- **Threat Events:** Credential theft, malware infection, data access
- **Training Content:**
  - Phishing email recognition
  - Suspicious link/attachment identification
  - Password security practices
  - Social engineering tactics
- **Frequency:** Annual mandatory training + quarterly refreshers
- **Phishing Drills:** Monthly simulated phishing emails with tracking

#### 14.5 - Train Workforce on Causes of Unintentional Data Exposure
- **Target Audience:** All staff
- **Threats Mitigated:** Accidental data breaches, insider negligence
- **Threat Events:** Misplaced devices, unlocked workstations, oversharing
- **Training Topics:**
  - Data classification
  - Secure handling of PHI
  - Device security practices
  - Clean desk policy

#### 14.6 - Train Workforce Members on Recognizing & Reporting Security Incidents
- **Target Audience:** All staff
- **Threats Mitigated:** Faster incident detection and response
- **Training Content:**
  - Incident identification
  - Reporting procedures
  - Who to contact
  - Non-retaliation policies

---

## CIS Control 15: Vendor Risk Management

**Group Category:** Security Foundational Skills  
**Implementation Level:** IG2, IG3

### Safeguards Implemented

#### 15.1 - Establish & Maintain Inventory of Service Providers
- **Assets Protected:** Cloud services, third-party software, vendors
- **Threats Mitigated:** Supply chain attacks, vendor compromise
- **Inventory Includes:**
  - Cloudy's Cloud Service (EHR hosting)
  - Medical software vendors
  - IT support contractors
  - Maintenance service providers
- **Assessment:** Annual security assessments of critical vendors

---

## CIS Control 16: Secure Application Development

**Group Category:** Security Foundational Skills  
**Implementation Level:** IG2, IG3

### Safeguards Implemented

#### 16.10 - Apply Secure Design Principles in Application Architectures
- **Assets Protected:** Custom applications, cloud configurations
- **Threats Mitigated:** Application vulnerabilities, injection attacks
- **Threat Events:** SQL injection, command injection, malware exploitation
- **Principles:** Input validation, error handling, secure defaults

---

## CIS Control 18: Penetration Testing

**Group Category:** Protective Technology  
**Implementation Level:** IG2, IG3

### Safeguards Implemented

#### 18.5 - Perform Periodic Internal Penetration Tests
- **Scope:** Network, applications, physical security
- **Frequency:** Annual formal testing + semi-annual red team exercises
- **Coverage:**
  - Network architecture testing
  - Web application security
  - Social engineering (phishing, physical)
  - Credential compromise scenarios
- **Purpose:** Identify vulnerabilities before attackers do

---

## Control Implementation Summary

| Control Group | Controls | Priority | Status |
|---|---|---|---|
| Data Protection | 3.6, 3.10, 3.11, 3.13 | Critical | Planned |
| Configuration | 4.2, 4.3, 4.11 | Critical | Planned |
| Identity & Access | 5.2, 6.1, 6.5, 6.8 | Critical | Planned |
| Software Management | 7.4, 7.5, 7.7 | High | Planned |
| Monitoring & Response | 8.2, 8.5, 8.11 | Critical | Planned |
| Email/Web Protection | 9.3, 9.6 | High | Planned |
| Malware Defense | 10.3, 10.5 | High | Planned |
| Recovery & Resilience | 11.1, 11.2, 11.3 | Critical | Planned |
| Network Infrastructure | 12.6, 12.8 | High | Planned |
| Network Defense | 13.1, 13.4, 13.8, 13.10 | Critical | Planned |
| Security Awareness | 14.2, 14.5, 14.6 | High | Planned |
| Vendor Risk | 15.1 | High | Planned |
| Application Security | 16.10 | Medium | Planned |
| Penetration Testing | 18.5 | High | Planned |

---

**Framework:** CIS Critical Security Controls v8.1  
**Assessment Date:** September 2025  
**Implementation Status:** Phased rollout based on risk prioritization  
**Last Updated:** September 2025
