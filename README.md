# SAMP Walk-in Clinic Risk Assessment Report

A comprehensive cybersecurity risk assessment for a medium-sized healthcare clinic implementing a cloud-based Electronic Health Record (EHR) system. This project identifies, evaluates, and prioritizes security risks across organizational, mission, and technical domains aligned with **CIS Critical Security Controls v8.1** and **PHIPA** compliance requirements.

## 📋 Project Overview

**Organization:** SAMP Walk-in Clinic  
**Organization Type:** IG2 (Implementation Group 2) - Medium-sized healthcare provider  
**Assessment Date:** September 2025  
**Scope:** Digital transformation initiative (Cloud-based EHR implementation, CAD $750,000 investment)  
**Patient Volume:** ~150 patients weekly  
**Staff:** ~30 employees (8 physicians, 10 nurses, 2 receptionists, 5 admin, 5 IT support)

### Context
The clinic is transitioning from paper-based health records to a cloud-based EHR system to improve patient care efficiency, real-time data access, and operational performance. This assessment evaluates security risks introduced by digital transformation while ensuring regulatory compliance.

## 👥 Team

| Name | Role |
|------|------|
| Parth Patel | System Administrator |
| Michael Tai | Chief Information Security Officer |
| Augustine Ofosu | Business Process Owner |
| Samuel Nyarko | IT Manager |

## 🔍 Assessment Approach

**Methodology:** Qualitative Risk Assessment  
**Framework:** CIS Critical Security Controls v8.1  
**Regulatory Compliance:** PHIPA (Personal Health Information Protection Act - Ontario)

### Risk Evaluation Scale
- **Likelihood:** Low, Moderate, High, Very High
- **Impact:** Low, Moderate, High, Catastrophic
- **Overall Risk:** Low, Moderate, High, Very High

## 📊 Coverage

### Three-Tier Risk Assessment

#### Tier 1: Organizational
High-level risks impacting the entire organization:
- Patient privacy and data protection
- Legal and regulatory compliance
- Reputational risks
- Third-party vendor management

#### Tier 2: Mission
Risks affecting critical business processes:
- Patient care delivery
- Appointment scheduling
- Medical billing
- Medical imaging services

#### Tier 3: Technical
Risks related to IT systems and infrastructure:
- Cloud-based EHR platform
- Medical imaging devices (X-ray, MRI)
- Network infrastructure
- Data storage and encryption

## 📦 Asset Inventory

The assessment covers 6 major asset categories:

1. **Devices** (16 asset types)
   - Enterprise assets (imaging machines, printers)
   - End-user devices (desktops, laptops, tablets)
   - IoT devices & network infrastructure

2. **Software** (11 applications)
   - Cloud-based EHR, scheduling, billing systems
   - Telemedicine platform
   - Clinical decision support

3. **Data** (4 data types)
   - Patient PII & Protected Health Information (PHI)
   - Financial information
   - System logs & audit trails

4. **Users** (2 categories)
   - Workforce (physicians, nurses, admin, IT staff)
   - Service providers & vendors

5. **Network** (6 infrastructure components)
   - LAN/WAN connections
   - Firewalls & routing systems
   - Wireless access points

6. **Documentation** (4 categories)
   - Business continuity & incident response plans
   - Security policies & agreements
   - Digital certificates & licenses

## 🚨 Key Findings

### High-Risk Threat Events Identified

| Threat | Assets at Risk | Inherent Risk | Control Focus |
|--------|---|---|---|
| **Ransomware/Malware via Phishing** | EHR DB, Cloud systems, Medical billing | Very High | MFA, security training, email filtering |
| **Unauthorized Medical Device Manipulation** | MRI/X-ray machines, PACS | Very High | Firewalls, encryption, access control |
| **Data Exfiltration from Cloud Storage** | PHI, PII, financial records | Very High | Audit logging, DLP policies, monitoring |
| **Credential Theft & Privilege Escalation** | Active Directory, Cloud accounts | Very High | MFA, session timeout, logging |
| **Supply Chain Attack on Billing System** | Medical billing software | Very High | Vendor assessment, API security |
| **Insider Threat / Data Misuse** | EHR, patient records, financial info | High | RBAC, segregation of duties, monitoring |

## 🛡️ Mitigation Controls

**Framework:** CIS Critical Security Controls v8.1

Controls implemented address:
- **CIS Control 3:** Data Protection (encryption at rest & in transit)
- **CIS Control 4:** Secure Configuration (automatic session locking, timeouts)
- **CIS Control 5:** Identity & Access Management (strong passwords, MFA)
- **CIS Control 6:** Access Control (RBAC, authentication)
- **CIS Control 7:** Software Asset Management (patching, vulnerability scanning)
- **CIS Control 8:** Data Recovery (audit logging, monitoring)
- **CIS Control 11:** Data Recovery & Resilience (backups, disaster recovery)
- **CIS Control 13:** Network Monitoring (firewalls, IPS, traffic filtering)
- **CIS Control 14:** Security Awareness (training, phishing drills)

### Sample Residual Risk Reduction

After control implementation:

| Threat | Control | Before | After |
|--------|---------|--------|-------|
| MRI machine manipulation | Firewalls & IPS | Very High | Moderate |
| DDoS on EHR system | Network traffic throttling | Moderate | Low |
| Malware/ransomware access | Software patching & scanning | Very High | Moderate |
| Insider data theft | RBAC & monitoring | High | Moderate |

## 📁 Project Structure

```
risk-assessment/
├── Risk_Assessment_Report.pdf       # Full RAR document
├── README.md                         # This file
├── assets/
│   ├── asset-inventory.md           # Complete asset list
│   ├── threat-sources.md            # Threat source analysis
│   └── control-mapping.md           # CIS controls implementation
├── risk-analysis/
│   ├── threat-events.md             # Detailed threat analysis
│   ├── vulnerabilities.md           # Vulnerability assessment
│   └── residual-risks.md            # Post-control risk levels
└── documentation/
    ├── PHIPA-compliance.md          # Regulatory requirements
    ├── incident-response-plan.md    # IR procedures
    └── disaster-recovery-plan.md    # DR procedures
```

## 🔐 Security Highlights

✅ **Qualitative risk assessment** using industry-standard descriptive scales  
✅ **Comprehensive asset inventory** covering devices, software, data, users, & infrastructure  
✅ **Threat-driven analysis** based on realistic threat sources for healthcare  
✅ **Vulnerability identification** across 40+ assets with severity/pervasiveness ratings  
✅ **Risk prioritization** using likelihood × impact scoring  
✅ **Layered controls** aligned with CIS v8.1 framework  
✅ **Residual risk evaluation** showing post-control risk reduction  
✅ **PHIPA compliance** focus on patient health information protection  

## 📚 Key Threats Addressed

- **Malicious Insiders** - Data theft, sabotage by authorized personnel
- **Negligent Insiders** - Accidental data exposure, misconfigurations
- **Cybercriminals** - Ransomware, data theft for sale, insurance fraud
- **Advanced Hackers** - DDoS attacks, sophisticated data breaches
- **Physical Threats** - Device theft, environmental damage, sabotage
- **Third-Party Risks** - Cloud provider downtime, vendor vulnerabilities
- **Natural Disasters** - Power surges, water damage, facility failures

## 🛠️ CIS Controls Implementation Status

- ✅ Asset & Configuration Management
- ✅ Identity & Access Management
- ✅ Awareness & Training
- ✅ Data Protection (encryption, DLP)
- ✅ Incident Response & Recovery
- ✅ Network Monitoring & Defense
- ✅ Secure Software Development

## 📋 Regulatory Alignment

- **PHIPA** - Personal Health Information Protection Act (Ontario)
- **CIS Critical Security Controls v8.1** - Industry best practices
- **IG2 Requirements** - Medium-sized organization compliance obligations

## 🎯 Next Steps

1. **Control Implementation Timeline** - Prioritize high-risk mitigation controls
2. **Risk Monitoring** - Establish KRIs (Key Risk Indicators)
3. **Regular Reassessment** - Annual risk assessment updates
4. **Incident Response Testing** - Annual IR plan drills & tabletop exercises
5. **Vulnerability Management** - Continuous scanning & patching
6. **Vendor Risk Management** - Ongoing third-party assessments

## 📖 Assessment Sections

- **Section 1.0** - Scenario & Organizational Context
- **Section 2.0** - Implementation Group Classification (IG2)
- **Section 3.0** - Three-Tier Risk Assessment Framework
- **Section 4.0** - Complete Risk Assessment
  - Asset Inventory
  - Threat Sources Analysis
  - Threat Events & Vulnerabilities
  - Likelihood, Impact & Risk Scoring
  - Mitigation Controls
- **Section 5.0** - Residual Risk Analysis

## 📞 Contact & Questions

For questions about this risk assessment or implementation, contact:
- **CISO:** Michael Tai
- **System Administrator:** Parth Patel
- **IT Manager:** Samuel Nyarko

## 📄 License

This risk assessment is proprietary to SAMP Walk-in Clinic and is for internal use only.

---

**Assessment Date:** September 29, 2025  
**Framework:** CIS Critical Security Controls v8.1  
**Compliance:** PHIPA (Ontario)  
**Classification:** IG2 (Medium-sized Healthcare Organization)
