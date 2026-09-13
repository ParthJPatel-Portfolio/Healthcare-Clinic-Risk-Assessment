# Threat Sources Analysis

Assessment of threat sources relevant to SAMP Walk-in Clinic based on capability, intent, and targeting characteristics.

## 1. Malicious Insiders

**Description:** Employees, contractors, or third-party vendors with authorized access who intentionally misuse their access.

| Attribute | Rating | Details |
|---|---|---|
| Capability | High | Direct access to critical systems and data |
| Intent | Moderate | Motivated by financial gain, espionage, revenge, or coercion |
| Targeting | High | Deliberately targeting specific systems/data |
| **Overall Risk** | **High** | **Significant threat due to authorized access** |

### Threat Events
- Employees modify or misuse critical patient data
- External contractors steal confidential data
- Third-party vendors exfiltrate PHI for financial gain
- Deliberate sabotage of medical systems

### Mitigation Priority
🔴 **CRITICAL** - Implement strong access controls, monitoring, and background checks

---

## 2. Negligent or Untrained Insiders

**Description:** Staff members who unintentionally expose data due to lack of cybersecurity training or awareness.

| Attribute | Rating | Details |
|---|---|---|
| Capability | Low | Limited technical knowledge |
| Intent | Very Low | Accidental/unintentional |
| Targeting | Very Low | No deliberate targeting |
| **Overall Risk** | **Low** | **Can be mitigated with training** |

### Threat Events
- Clicking on phishing links leading to credential theft
- Misplacing devices with access to confidential data
- Misconfiguring access controls
- Leaving workstations unlocked/unattended
- Sharing passwords or credentials

### Mitigation Priority
🟡 **HIGH** - Implement security awareness training and technical controls

---

## 3. Politically Sponsored Hackers

**Description:** Advanced threat actors motivated by political or organizational agendas.

| Attribute | Rating | Details |
|---|---|---|
| Capability | High | Advanced technical skills, tools, tactics |
| Intent | High | Motivated by political agenda or revenge |
| Targeting | High | Deliberate targeting of healthcare organizations |
| **Overall Risk** | **High** | **Sophisticated attacks possible** |

### Threat Events
- Successful data breaches exposing patient health information
- DDoS attacks on critical systems
- Targeted phishing campaigns against key staff
- Reputational damage to clinic and patients

### Mitigation Priority
🔴 **CRITICAL** - Implement advanced detection, network hardening, incident response

---

## 4. Cybercriminals

**Description:** Threat actors motivated by financial profit and willing to use sophisticated attack methods.

| Attribute | Rating | Details |
|---|---|---|
| Capability | Very High | Advanced tools, techniques, infrastructure |
| Intent | Very High | Purely motivated by financial gain |
| Targeting | Very High | Healthcare data highly valued on dark web |
| **Overall Risk** | **Very High** | **Most prolific threat to healthcare** |

### Threat Events
- Ransomware attacks encrypting patient records
- Malware deployment for data theft
- PHI/PII sold on dark web (high market value)
- Insurance fraud using stolen medical/financial data
- Extortion demands after data theft

### Threat Context
Healthcare data is particularly valuable:
- Patient PHI sells for $250-$1,000 per record on dark web
- Combined with financial data increases fraud potential
- Ransomware attacks targeting hospitals often succeed due to criticality

### Mitigation Priority
🔴 **CRITICAL** - Multi-layered defense, robust backup strategy, incident response

---

## 5. Third-Party Service Providers

**Description:** Cloud providers and vendors experiencing service disruptions or security failures.

| Attribute | Rating | Details |
|---|---|---|
| Capability | Low | Service failures not attacks |
| Intent | Very Low | No malicious intent |
| Targeting | Very Low | Non-targeted incidents |
| **Overall Risk** | **Low-Moderate** | **Can disrupt service availability** |

### Threat Events
- Unplanned cloud service downtime
- Service outages from provider infrastructure failures
- System misconfigurations at vendor level
- DDoS attacks affecting provider's infrastructure

### Dependency Risk
- **Primary Cloud Provider:** Cloudy's Cloud Service
- **Current Limitation:** No secondary cloud provider backup
- **Business Impact:** 150+ patients/week depend on EHR availability

### Mitigation Priority
🟡 **HIGH** - Implement redundancy, multi-vendor strategy, SLA enforcement

---

## 6. Natural Disasters

**Description:** Environmental events causing physical damage to infrastructure.

| Attribute | Rating | Details |
|---|---|---|
| Capability | Very Low | Environmental damage (not targeted) |
| Intent | Very Low | No intent involved |
| Targeting | Very Low | Random occurrence |
| **Overall Risk** | **Low** | **Can be mitigated with preparation** |

### Threat Events
- Power surges damaging IT equipment
- Water damage from pipes/flooding
- Power outages disrupting clinic operations
- Equipment failures due to environmental stress

### Mitigations Already in Place
- UPS systems (some equipment)
- HVAC systems
- Building infrastructure

### Mitigation Priority
🟡 **MEDIUM** - Implement environmental controls, backups, disaster recovery

---

## 7. Unnatural Disasters (Sabotage/Destruction)

**Description:** Intentional human-caused damage to facilities or equipment.

| Attribute | Rating | Details |
|---|---|---|
| Capability | Low | Physical access required |
| Intent | Low | Requires deliberate motivation |
| Targeting | Moderate | Could target specific systems |
| **Overall Risk** | **Low** | **Lower probability but possible** |

### Threat Events
- Riots resulting in building damage
- Revenge attacks against clinic staff
- Intentional destruction of server rooms
- Equipment vandalism

### Context
- Could occur from public discontent or personal grievances
- Physical security measures primary defense

### Mitigation Priority
🟡 **MEDIUM** - Physical security, surveillance, access controls

---

## Threat Landscape Summary

### By Threat Level

| Level | Threat Source | Primary Concern |
|---|---|---|
| 🔴 CRITICAL | Cybercriminals | Ransomware, data theft |
| 🔴 CRITICAL | Malicious Insiders | Unauthorized data access/misuse |
| 🔴 CRITICAL | Politically Sponsored Hackers | DDoS, data breaches |
| 🟡 HIGH | Negligent Insiders | Accidental exposure |
| 🟡 HIGH | Third-Party Vendors | Service disruption |
| 🟡 MEDIUM | Natural Disasters | Environmental damage |
| 🟡 MEDIUM | Sabotage | Physical destruction |

---

## Healthcare-Specific Threat Context

Why healthcare is a high-value target:

1. **Data Value** - PHI data commands premium prices on dark web
2. **Criticality** - Patient care depends on system availability
3. **Compliance** - PHIPA violations result in significant penalties
4. **Reputation** - Breaches damage patient trust immediately
5. **Leverage** - Ransomware highly effective when patient care at risk
6. **Legacy Systems** - Many clinics run outdated, vulnerable infrastructure

---

**Assessment Date:** September 2025  
**Framework:** Threat Source Capability/Intent/Targeting Analysis  
**Scope:** IG2 Healthcare Organization (SAMP Walk-in Clinic)
