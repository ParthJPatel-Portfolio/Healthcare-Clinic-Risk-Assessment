# Threat Events Analysis

Detailed analysis of threat events identified during the SAMP Walk-in Clinic Risk Assessment, including likelihood, impact, and overall risk classification.

---

## Critical Threat Events (Very High Risk)

### 1. Ransomware/Malware Attack on EHR Database

**Threat Event:** Cybercriminals successfully gain access to the EHR database via malware, deploying ransomware to encrypt patient files or stealing PHI for sale on the dark web.

| Factor | Rating | Details |
|---|---|---|
| Relevance | Expected | Highly likely in healthcare |
| Attack Initiation Likelihood | High | Common attack vector |
| Success Likelihood if Initiated | Very High | Strong impact if successful |
| Overall Likelihood | Very High | Expected to occur |
| Impact | Very High | Patient care disruption, massive data breach |
| **Risk Level** | **Very High** | **CRITICAL PRIORITY** |

**Assets at Risk:**
- Patient PII & PHI database
- Financial information
- Electronic Health Records
- EHR management system

**Attack Vectors:**
- Phishing emails with malicious attachments
- Compromised credentials via phishing
- Exploitation of unpatched software vulnerabilities
- Supply chain compromise (vendor access)

**Business Impact:**
- Clinic unable to access patient records
- Patient care delays/cancellations
- Regulatory fines for PHIPA violation
- Reputational damage
- Ransom demands ($100k-$500k typical for healthcare)

**Mitigation Controls:**
- Multi-factor authentication
- Data encryption (at rest & in transit)
- Regular software patching
- Data loss prevention policies
- Security awareness training
- Regular backups with offline copies

---

### 2. Unauthorized Manipulation of Medical Imaging Devices (MRI/X-ray)

**Threat Event:** Cybercriminal compromises X-ray or MRI machine operational settings, resulting in incorrect images and dangerous treatment plans that endanger patient safety.

| Factor | Rating | Details |
|---|---|---|
| Relevance | Anticipated | Emerging threat in healthcare |
| Attack Initiation Likelihood | Moderate | Requires network access |
| Success Likelihood if Initiated | High | Devices often lack modern security |
| Overall Likelihood | High | Likely if unprotected |
| Impact | Very High | Patient safety risk, incorrect diagnosis |
| **Risk Level** | **Very High** | **CRITICAL PRIORITY** |

**Assets at Risk:**
- X-ray imaging machine
- MRI imaging machine
- Radiology Information System
- Patient safety

**Attack Vectors:**
- Man-in-the-middle attack on device communication
- Exploitation of weak device authentication
- Malware infection of connected systems
- Compromised network credentials

**Patient Safety Impact:**
- Incorrect image settings producing unsafe radiation exposure
- Altered protocols causing misdiagnosis
- Wrong treatment plans based on corrupted images
- Legal liability and malpractice risks

**Mitigation Controls:**
- Firewalls & intrusion prevention systems
- Data encryption for device communications
- Role-based access control
- Regular security patching
- Multi-factor authentication
- Network segmentation for medical devices

---

### 3. Data Exfiltration from Cloud Storage Account

**Threat Event:** Attacker disables cloud storage audit logs and workload protection, establishes backdoor access, and steals PHI/PII for sale on dark web or insurance fraud.

| Factor | Rating | Details |
|---|---|---|
| Relevance | Anticipated | Cloud-specific threat |
| Attack Initiation Likelihood | High | Cloud services lucrative target |
| Success Likelihood if Initiated | Very High | Cloud breaches often undetected |
| Overall Likelihood | Very High | Expected attack |
| Impact | Very High | Complete data breach, regulatory fines |
| **Risk Level** | **Very High** | **CRITICAL PRIORITY** |

**Assets at Risk:**
- Cloud storage account
- PHI database copies
- PII records
- Financial information
- Backup systems

**Attack Vectors:**
- Stolen admin credentials
- Compromised cloud API keys
- Third-party vendor compromise
- Misconfigured cloud permissions

**Data Black Market Value:**
- Single patient PHI: $250-$1,000
- 10,000 patient records: $2.5-$10 million
- Combined with financial data: 2-3x value increase

**Mitigation Controls:**
- Role-based access control
- Multi-factor authentication for cloud admins
- Audit log monitoring & alerting
- Cloud workload protection platform
- Data encryption
- Regular audit log reviews
- Geo-blocking of unauthorized access attempts

---

### 4. Credential Theft & Privilege Escalation via Active Directory

**Threat Event:** Attacker extracts credentials from highly privileged Active Directory accounts and performs privilege escalation to gain access to critical systems.

| Factor | Rating | Details |
|---|---|---|
| Relevance | Expected | Common attack progression |
| Attack Initiation Likelihood | High | High value target |
| Success Likelihood if Initiated | Very High | AD often not sufficiently hardened |
| Overall Likelihood | Very High | Expected attack |
| Impact | Very High | Full system compromise possible |
| **Risk Level** | **Very High** | **CRITICAL PRIORITY** |

**Assets at Risk:**
- Active Directory
- All domain-connected systems
- EHR system
- Cloud accounts
- Network infrastructure

**Attack Vectors:**
- Phishing targeting IT administrators
- Exploitation of domain controller vulnerabilities
- Dumping credentials from compromised systems
- Pass-the-hash attacks
- Kerberos delegation abuse

**Escalation Chain:**
1. Initial compromise (phishing/malware)
2. Lateral movement to privileged system
3. Credential harvesting from memory
4. Privilege escalation to domain admin
5. Backdoor installation for persistence
6. Data exfiltration

**Mitigation Controls:**
- Multi-factor authentication for all admin accounts
- Session timeout policies
- Detailed audit logging
- Privilege access workstations (PAWs)
- Credential Guard enabled
- Regular privileged access reviews

---

### 5. Supply Chain Attack on Medical Billing System

**Threat Event:** Third-party vendor's medical billing software is compromised, allowing exfiltration of PHI and financial information or ransomware deployment.

| Factor | Rating | Details |
|---|---|---|
| Relevance | Anticipated | Increasing threat vector |
| Attack Initiation Likelihood | High | Vendors are common targets |
| Success Likelihood if Initiated | Very High | Direct access to systems |
| Overall Likelihood | Very High | Likely scenario |
| Impact | Very High | Data breach + billing disruption |
| **Risk Level** | **Very High** | **CRITICAL PRIORITY** |

**Assets at Risk:**
- Medical billing software
- Financial records
- Patient insurance information
- Credit card data
- Vendor API connections

**Attack Vectors:**
- Compromise of vendor development environment
- Injection of malicious code into updates
- Exploitation of vendor infrastructure
- Compromised vendor credentials

**Business Impact:**
- Billing system outage
- Inability to process insurance claims
- Financial data theft
- Regulatory compliance violations
- Loss of patient financial records

**Mitigation Controls:**
- Vendor security assessments
- API security hardening
- Data encryption
- DLP policies for vendor connections
- Network monitoring
- Incident response contracts with vendors

---

## High-Risk Threat Events

### 6. DDoS Attack on Cloud-Based EHR System

**Threat Event:** Attackers flood critical health data systems with traffic, disabling primary functions and preventing clinic staff from accessing patient records.

| Factor | Rating | Details |
|---|---|---|
| Relevance | Anticipated | Common healthcare target |
| Attack Initiation Likelihood | High | Distributed attack tools readily available |
| Success Likelihood if Initiated | High | Without mitigation likely to succeed |
| Overall Likelihood | High | Likely attack |
| Impact | High | Service outage, patient care delay |
| **Risk Level** | **High** | **HIGH PRIORITY** |

**Assets at Risk:**
- Cloud-based EHR
- Patient scheduling system
- Cloud infrastructure

**Attack Impact:**
- Patient unable to access records for 4-24 hours
- Appointment scheduling unavailable
- Treatment delays
- Patient care disruption
- Reputational damage

**Mitigation Controls:**
- Network traffic throttling
- DDoS protection services
- Auto-scaling infrastructure
- Geo-blocking of attack sources
- Network monitoring

---

### 7. Insider Data Theft or Misuse

**Threat Event:** Authorized staff member or contractor intentionally steals or misuses patient data for financial gain, espionage, or revenge.

| Factor | Rating | Details |
|---|---|---|
| Relevance | Possible | Documented cases in healthcare |
| Attack Initiation Likelihood | Moderate | Malicious insiders exist in any org |
| Success Likelihood if Initiated | Very High | Already have authorized access |
| Overall Likelihood | High | Possible occurrence |
| Impact | High | Data breach, patient harm |
| **Risk Level** | **High** | **HIGH PRIORITY** |

**Assets at Risk:**
- Patient records
- Financial information
- PII/PHI database

**Threat Profile:**
- Disgruntled employees
- Financial motivation (data sells for $250-$1,000 per record)
- Contractors with temporary access
- Vendors with system access

**Detection Challenges:**
- Legitimate access makes activity blend in
- May occur over extended period
- Difficult to distinguish from normal work

**Mitigation Controls:**
- Role-based access control
- Segregation of duties
- Detailed audit logging
- Regular access reviews
- Background checks
- Monitoring of unusual data access
- Employee security training

---

### 8. Wireless Network Attacks (MITM & Credential Theft)

**Threat Event:** Remote attacker performs man-in-the-middle attack on wireless traffic, stealing credentials and patient information.

| Factor | Rating | Details |
|---|---|---|
| Relevance | Expected | Wireless commonly misconfigured |
| Attack Initiation Likelihood | High | No special access needed |
| Success Likelihood if Initiated | Very High | Wireless security often weak |
| Overall Likelihood | Very High | Expected attack |
| Impact | High | Credential theft, data exposure |
| **Risk Level** | **Very High** | **CRITICAL PRIORITY** |

**Assets at Risk:**
- Wireless access points
- Connected devices (tablets, laptops)
- Network traffic
- User credentials

**Attack Vectors:**
- Weak encryption (WEP/WPA2 without suite B)
- Default wireless credentials
- Evil twin networks
- Misconfigured access points

**Data at Risk:**
- Login credentials
- Patient information
- Physician-patient conversations

**Mitigation Controls:**
- Secure Wi-Fi protocols (WPA3)
- Strong encryption
- Multi-factor authentication
- Network segmentation
- Regular security configuration reviews

---

## Moderate-Risk Threat Events

### 9. Phishing Attacks Leading to Credential Theft

**Threat Event:** Medical staff unknowingly click phishing links, leading to credential theft and unauthorized access to confidential health data.

| Factor | Rating | Details |
|---|---|---|
| Relevance | Expected | Extremely common in healthcare |
| Attack Initiation Likelihood | High | Easy to execute |
| Success Likelihood if Initiated | Very High | Humans remain weak link |
| Overall Likelihood | Very High | Expected attack |
| Impact | Moderate | Depends on compromised account |
| **Risk Level** | **Moderate** | **MEDIUM PRIORITY** |

**Assets at Risk:**
- User credentials
- Patient portal
- Medical staff accounts
- Email systems

**Phishing Targets:**
- Physicians (high-value targets)
- IT administrators (privilege escalation)
- Receptionists (patient data access)

**Success Rate:**
- Typical phishing: 15-20% click rate
- Targeted spear phishing: 30-40% success
- Healthcare providers: Higher success rates

**Mitigation Controls:**
- Security awareness training
- Phishing simulation drills (monthly)
- Email filtering & anti-phishing tools
- Multi-factor authentication
- URL filtering

---

### 10. Unpatched Software Exploitation

**Threat Event:** Attackers exploit unpatched vulnerabilities in medical software applications, operating systems, or firmware to gain unauthorized access.

| Factor | Rating | Details |
|---|---|---|
| Relevance | Expected | Known vulnerabilities constantly released |
| Attack Initiation Likelihood | Moderate | Depends on patch availability |
| Success Likelihood if Initiated | High | Exploits available for unpatched systems |
| Overall Likelihood | High | Highly likely |
| Impact | High | System compromise, data access |
| **Risk Level** | **High** | **HIGH PRIORITY** |

**Affected Assets:**
- Operating systems (Windows)
- Medical software applications
- Network devices (printer firmware, routers)
- IoT devices (thermostats)

**Vulnerable Examples:**
- Printer firmware exploits for lateral movement
- IoT thermostat use as network backdoor
- Windows OS command injection vulnerabilities

**Patch Management Strategy:**
- Critical patches: 48 hours
- High-priority: 2 weeks
- Medium: 4 weeks
- Regular vulnerability scanning

**Mitigation Controls:**
- Automated patch management
- Vulnerability scanning
- Vulnerability remediation process
- Software inventory management

---

## Low-Risk Threat Events

### 11. Device Misplacement

**Threat Event:** Medical employees recklessly misplace devices (tablets, etc.) with access to confidential data.

| Factor | Rating | Details |
|---|---|---|
| Relevance | Expected | Common occurrence |
| Attack Initiation Likelihood | High | Employee carelessness |
| Success Likelihood if Initiated | Moderate | Device encryption may protect data |
| Overall Likelihood | Moderate | Possible occurrence |
| Impact | Moderate | Depends on data encryption |
| **Risk Level** | **Moderate** | **MEDIUM PRIORITY** |

**Assets at Risk:**
- Tablets with EHR access
- Mobile devices with patient data
- Laptops with sensitive information

**Data Protection:**
- Full device encryption critical
- Remote wipe capability needed
- Session timeout on devices

**Mitigation Controls:**
- Device encryption
- Remote wipe capability
- Session timeout settings
- Device tracking
- Access control on devices

---

### 12. Environmental Threats (Power Outages, Water Damage)

**Threat Event:** Water damage from facilities or power surges cause damage to data processing/storage devices.

| Factor | Rating | Details |
|---|---|---|
| Relevance | Possible | Environmental hazards exist |
| Attack Initiation Likelihood | Low | Random environmental occurrence |
| Success Likelihood if Initiated | High | Damage likely if occurs |
| Overall Likelihood | Moderate | Possible but not highly likely |
| Impact | High | Systems offline, patient care impact |
| **Risk Level** | **Moderate** | **MEDIUM PRIORITY** |

**Assets at Risk:**
- Server infrastructure
- Network equipment
- Power systems
- HVAC systems

**Mitigation Controls:**
- Environmental controls (fire suppression, HVAC)
- UPS systems for power backup
- Regular backups to multiple locations
- Disaster recovery planning
- Regular maintenance

---

## Summary Table: All Threat Events

| Threat Event | Likelihood | Impact | Risk | Priority |
|---|---|---|---|---|
| Ransomware/Malware on EHR | Very High | Very High | **Very High** | 🔴 CRITICAL |
| Medical Device Manipulation | High | Very High | **Very High** | 🔴 CRITICAL |
| Cloud Storage Data Exfiltration | Very High | Very High | **Very High** | 🔴 CRITICAL |
| Active Directory Compromise | Very High | Very High | **Very High** | 🔴 CRITICAL |
| Supply Chain Attack | Very High | Very High | **Very High** | 🔴 CRITICAL |
| DDoS on EHR | High | High | **High** | 🟠 HIGH |
| Insider Threat | High | High | **High** | 🟠 HIGH |
| Wireless MITM Attack | Very High | High | **Very High** | 🔴 CRITICAL |
| Phishing Attacks | Very High | Moderate | **High** | 🟠 HIGH |
| Unpatched Software | High | High | **High** | 🟠 HIGH |
| Device Misplacement | Moderate | Moderate | **Moderate** | 🟡 MEDIUM |
| Environmental Threats | Moderate | High | **Moderate** | 🟡 MEDIUM |

---

**Assessment Date:** September 2025  
**Framework:** Qualitative Risk Assessment  
**Methodology:** Threat Event > Likelihood > Impact > Risk Scoring  
**Total Threat Events Assessed:** 40+
