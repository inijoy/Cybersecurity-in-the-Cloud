# Cybersecurity in the Cloud

# PROJECT TITLE:

## Operation Cloud Mirage: Securing AWS Infrastructure Against Advanced Persistent Threats

## Project Overview:

## As organizations migrate their critical infrastructure to the cloud, they gain flexibility and scalability—but also take on new security risks. This project explores a real-world scenario inspired by a ransomware attack in a recently migrated AWS environment, highlighting misconfigurations, access control issues, and the behavior of threat actors. This documentation covers key cybersecurity concepts in a cloud context and provides a full risk analysis and mitigation plan for DigitalWitch Cyber Solutions Ltd.

## Aims & Objectives

- To demonstrate understanding and application of core cloud security principles.
- To identify and mitigate risks related to cloud infrastructure misconfigurations.
- To understand threat actor tactics and profile them using threat intelligence.
- To implement access control and change management in cloud operations.
- To document cybersecurity responses using industry frameworks and metrics.

## Core Security Principles
CIA Triad: The Foundation of Cybersecurity

| **Component** | **Definition** | **Why It Matters in Cloud** |
| --- | --- | --- |
| Confidentiality | Ensuring that data is only accessible to authorized individuals. | Misconfigured S3 buckets can expose sensitive data. |
| Integrity | Protecting data from unauthorized changes or corruption. | Poorly managed IAM can allow malicious changes. |
| Availability | Keeping systems and data accessible to authorized users. | DDoS attacks or misconfigurations can take services offline. |

## DAD Triad (Opposite of CIA)

- Disclosure – Unintended data leaks (opposite of Confidentiality)
- Alteration – Unauthorized data modification (opposite of Integrity)
- Denial – Legitimate users can’t access data (opposite of Availability)

## Identity, Authentication, Authorization, Accounting (IAAA)

| **Term** | **Meaning** | **Cloud Relevance** |
| --- | --- | --- |
| Identification | Who are you? (e.g., IAM user) | AWS IAM roles/users |
| Authentication | Prove it! (e.g., password, key) | MFA, access keys |
| Authorization | What are you allowed to do? | IAM policies & roles |
| Accounting | What did you do? | CloudTrail logs, audit events |

### Importance: IAAA controls the gate to your cloud environment. Weak or excessive IAM roles are often entry points for attackers.

## Risk Management in the Cloud
Definitions:

- **Risk** = Likelihood that a threat will exploit a vulnerability, causing harm.
- **Threat** = Potential cause of harm (e.g., malware, attacker).
- **Vulnerability** = Weakness in your system (e.g., open ports, weak passwords).
- **Impact** = Consequences if the threat materializes.

### Formula:

**Total Risk = Threat × Vulnerability × Asset Value**

**Asset Value:** Importance or sensitivity of data/systems to the business (financial, operational, reputational impact).

Countermeasures & Residual Risk

- **Countermeasures:** Controls to reduce risk (e.g., firewalls, IAM hardening, patching).
- **Residual Risk:** Risk that remains after all countermeasures are in place.

No system is 100% secure. Always monitor for new risks.

## Types of Risk:

| **Type** | **Description** |
| --- | --- |
| Strategic Risk | Poor cloud strategy or vendor lock-in |
| Operational Risk | System failure, human error |
| Technical Risk | Vulnerabilities, outdated systems |
| Compliance Risk | GDPR, HIPAA violations |
| Third-party Risk | Vendor mismanagement |

## Risk Metrics & Controls

- **Risk Assessment:** Identify, analyze, evaluate, and treat risks.
- **Risk Response Types:** Accept, Mitigate, Transfer (e.g., insurance), Avoid
- **Controls:**
    - Preventive (e.g., firewalls)
    - Detective (e.g., SIEM)
    - Corrective (e.g., rollback scripts)

## Monitoring & Reporting: KGI, KPI, KRI

| **Metric** | **Meaning** | **Example** |  |
| --- | --- | --- | --- |
| KGI | Key Goal Indicator | 100% MFA adoption |  |
| KPI | Key Performance Indicator | % of patched systems |  |
| KRI | Key Risk Indicator | # of failed login attempts |  |

# Case Study: DigitalWitch Cyber Solutions Ltd

## **Scenario:**

*DigitalWitch Cyber Solutions Ltd* just recently migrated 80% of its infrastructure to the cloud (AWS).

A few weeks into the migration, several departments began reporting:

- Sudden access denials to internal resources.
- Unauthorized cloud storage access.
- Unusual outbound traffic to unknown IPs.

At the same time, a ransomware note appears on a few virtual machines, demanding payment in Monero. Security teams also discovered that a set of previously whitelisted IPs had been added to firewall rules, and some IAM roles were overly permissive.

Initial threat intelligence suggests the involvement of **APT32** or **APT41** groups known for cloud espionage and ransomware deployment.

### **Your Tasks:**

You are tasked with conducting a **comprehensive analysis and response strategy**. Your report should include the following sections:

---

1. Identify and describe at least **3 key risks** in the scenario. Classify them using **Total Risk = Threat x Vulnerability x Asset Value**.
2. Define what the **Residual Risk** might be **after patching** and **IAM tightening**.
3. Explain **what secondary risks** could arise after implementing changes.

## **Summary**

### Digital Witch Cyber Solutions Ltd has experienced a multi-vector cloud security breach affecting 80% of recently migrated AWS infrastructure. Initial indicators suggest involvement of Advanced Persistent Threat (APT) groups APT32 or APT41, known for sophisticated cloud espionage and ransomware operations.

### This report provides a comprehensive risk analysis and strategic response recommendations

# **Risk Assessment Framework**

**Risk Calculation Formulas**

**Basic Risk Formula:**

Risk = Threat × Vulnerability × Impact

**Total Risk Formula:**

Total Risk = Threat × Vulnerability × Asset Value

**Residual Risk Formula:**

Residual Risk = Total Risk - Countermeasures

Countermeasures = % Risk Mitigation × Total Risk

# **PART 1. Risk and Threat Analysis**

## **Key Risk Identification and Classification:**

## **Risk 1: Ransomware Deployment and Business Continuity Disruption**

**Risk Components:**

- **Threat Level:** 10/10  (Confirmed ransomware deployment with Monero payment demands)
- **Vulnerability Level:** 7/10  (Virtual machines compromised, potential lateral movement capabilities)
- **Impact:** 10/10  (Critical business operations, revenue generation systems)

**Risk = 10 x 7 x 10 = 700/1000.
To convert % = (700/1000) x 100 = 70%**

## **Total Risk**

- **Threat Level:** 10/10 (Confirmed ransomware deployment with Monero payment demands)
- **Vulnerability Level:** 7/10 (Virtual machines compromised, potential lateral movement capabilities)
- **Asset Value:** $20,000 (Critical business operations, revenue generation systems)

**Total Risk Calculation:**
Threat =10
Vulnerability = 7
Asset Value = $ 20,000
**TR = 10 x 7 x 20,000 = $1,400,000**

## **Description:**  Active ransomware deployment threatens business continuity and revenue generation. The demand for Monero payments indicates sophisticated threat actors familiar with cryptocurrency anonymization techniques, suggesting potential for expanded attack vectors.

## **Risk 2: Unauthorized Data Exfiltration via Compromised Cloud Storage**

### **Risk Components:**

- **Threat Level:** 10/10 (APT32/APT41 active presence with proven data exfiltration capabilities)
- **Vulnerability Level:** 8/10 (Overly permissive IAM roles, unauthorized storage access confirmed)
- **Impact:** 10/10 (Customer data, intellectual property, financial records)

**Risk Calculation:**

**For RISK 2**
Threat = 10
Vulnerability score = 8
Impact =10
**Risk = 10 x 8 x 10 = 800/1000 =80%** 

## **Total Risk**

- **Threat Level:** 10/10 (APT32/APT41 active presence with proven data exfiltration capabilities)
- **Vulnerability Level:** 8/10 (Overly permissive IAM roles, unauthorized storage access confirmed)
- **Asset Value:** $25,000 (Customer data, intellectual property, financial records)

**Total Risk Calculation**

For Total Risk
Threat =10
Vulnerability = 8
Asset Value = $ 25,000
TR = 10 x 8 x25,000 =  $2,000,000

## **Description:** Advanced threat actors have gained unauthorized access to cloud storage repositories containing sensitive customer data, proprietary algorithms, and financial information. The combination of sophisticated threat actors and misconfigured IAM policies creates an extremely high-risk scenario for large-scale data breaches.

## **Risk 3: Network Infrastructure Compromise and Persistent Access**

### **Risk Components:**

- **Threat Level:** 10/10 (Whitelisted malicious IPs indicate advanced persistent threat establishment)
- **Vulnerability Level:** 7/10 (Firewall rules compromised, unusual outbound traffic patterns)
- **Impact:** 9/10 (Network infrastructure, internal communications, operational technology)

 **Risk Calculation**

**For RISK 3**
Threat = 10
Vulnerability = 7
Impact = 9
Risk = 10 x 7 x9 = 630/1000.
To convert % = (630/1000) x 100 = 63%

## **Total Risk**

- **Threat Level:** 10/10 (Whitelisted malicious IPs indicate advanced persistent threat establishment)
- **Vulnerability Level:** 7/10 (Firewall rules compromised, unusual outbound traffic patterns)
- **Asset Value:** $30,000  (Network infrastructure, internal communications, operational technology)

**Total Risk Calculation:**

For Total Risk
Threat =10
Vulnerability = 7
Asset Value = $ 30,000
TR = 10 x 7 x30,000 = $2,100,000

## **Description:** Threat actors have established persistent network access through compromised firewall configurations and whitelisted malicious IP addresses. This enables continued reconnaissance, lateral movement, and potential future attack vectors

## Residual Risk Assessment After Mitigation

### Post-Patching and IAM Tightening Scenario

## **Risk 1 - Ransomware Deployment (Post-Mitigation):**

**Applied Controls:** 

- Endpoint protection
- Backup restoration
- Network segmentation

**Risk Mitigation Score:** 70% average effectiveness

**For Residual Risk = TR - Countermeasure**
Countermeasure =  ( % of Risk Mitigation x TR) =  70/100 x 1,400,000 = 0.70 x 1,400,000
= $980,000

Residual Risk = TR - CM = 1,400,000 - 980,000 = 420,000
Residual Risk = $420,000

% of Residual Risk = (420,000/1,400,000) x 100 = 30%

## Therefore, after implementing Countermeasures to protect the system, we were able to achieve 70% effectiveness, hence leaving us with 30 % Residual Risk

## **Risk 2 - Data Exfiltration (Post-Mitigation):**

**Applied Controls:**

- IAM role restrictions,
- Enhanced monitoring
- Data encryption

**Risk Mitigation Score:** 80% average effectiveness

**For Residual Risk = TR - Countermeasure**
Countermeasure =  ( % of Risk Mitigation x TR) = 80/100 x 2,000,000 = 0.80 x 2,000,000
= $1,600,000

Residual Risk = TR - CM = 2,000,000 - 1,600,000 = 400,000
Residual Risk = $400,000

% of Residual Risk = (400,000/2,00,000) x 100 = 20%

## Therefore, after implementing Countermeasures to protect the system, we were able to achieve 80% effectiveness, hence leaving us with 20 % Residual Risk

## **Risk 3 - Network Compromise (Post-Mitigation):**

**Applied Controls:** 

- Firewall reconfiguration
- IP blacklisting
- Network monitoring

**Risk Mitigation Score:** 63% average effectiveness

**For Residual Risk = TR - Countermeasure**
Countermeasure =  ( % of Risk Mitigation x TR) =  63/100 x 2,100,000 = 0.63 x 2,100,000
= #1,323,000

Residual Risk = TR - CM = 2,100,000 - 1,323,000 = 777,000
Residual Risk = $777,000

% of Residual Risk = (777,000/2,100,000) x 100 = 37%

## Therefore, after implementing Countermeasures to protect the system, we were able to achieve 63% effectiveness, hence leaving us with 37% Residual Risk

## Secondary Risk Analysis:

### Operational Impact Risks from Security Implementations

### **Secondary Risk 1: Legitimate User Access Disruption**

## **Description:**

- Implementing overly restrictive IAM policies can inadvertently block authorized users from accessing essential business systems.
- The probability of occurrence is high, estimated at 70%.
- While the resulting business disruption is expected to be moderate, the financial impact can be significantly reduced by adopting a phased implementation approach combined with a robust user access validation protocol.

## **Secondary Risk 2: Third-Party Integration Failures**

## **Description:**

- Overly restrictive firewall configurations may unintentionally disrupt connections with critical third-party services, APIs, and cloud-based partner integrations.
- The probability of occurrence is medium, estimated at 50% but the potential for operational disruption is high.
- However, conducting comprehensive integration testing and implementing a structured whitelisting procedure can substantially reduce the financial impact.

## **Secondary Risk 3: Performance Degradation**

## **Description:**

- The implementation of advanced monitoring and security controls may introduce latency or resource strain, potentially affecting system performance and user experience.
- The probability of this risk occurring is medium, approximately 45% with a corresponding medium impact on productivity.
- However, optimizing the configuration of security tools and ensuring appropriate resource allocation can help mitigate the financial burden.

## **Secondary Risk 4: Compliance and Audit Complications**

## **Description:**

- Accelerated implementation of security changes can lead to incomplete compliance documentation and inconsistencies in audit trails, increasing the likelihood of regulatory scrutiny.
- The probability of occurrence is medium, estimated at 40% with a high associated regulatory risk.
- However, maintaining comprehensive change documentation and enforcing strict compliance validation procedures can significantly reduce the financial impact

## Risk Prioritization Matrix

| Risk Category | Total Risk Score | Residual Risk Score | Priority Level | Timeline |
| --- | --- | --- | --- | --- |
| Data Exfiltration | $2,000,000 | $400,000 | P1~ Immediate | 0-24 hours |
| Ransomware Deployment |  **$1,400,000** | $420,000 | P1 ~ Immediate | 0-24 hours |
| Network Compromise | $2,100,000 |  $777,000 | P2 ~ Urgent | 24-72 hours |

### Strategic Recommendations:

1. **Immediate Actions (0-24 hours):**
    - Isolate affected virtual machines and storage systems
    - Revoke and regenerate all potentially compromised credentials
    - Implement emergency firewall rules to block malicious IP addresses
    
2. **Short-term Mitigation (24-72 hours):**
    - Comprehensive IAM audit and role optimization
    - Deploy advanced threat detection and response tools
    - Establish secure communication channels for incident coordination
    
3. **Long-term Security Enhancement (1-4 weeks):**
    - Implement Zero Trust architecture principles
    - Establish continuous security monitoring and threat intelligence integration
    - Develop comprehensive incident response and business continuity procedures

# **Part 2: Cloud Misconfigurations & Attack Surface**

## **Common Cloud Misconfigurations:**

1. Public S3 Buckets
2. Default “Allow All” Security Groups
3. No IAM Policy Boundaries
4. Disabled CloudTrail Logging
5. Open Ports (SSH, RDP, etc.)

## Misconfigurations That Enabled Breach:

- Open ports and overly permissive IAM roles allowed lateral movement and ransomware drop.

## **Shared Responsibility Model:**

| **Layer** | **AWS Patches** | **You Patch** |
| --- | --- | --- |
| IaaS (e.g., EC2) | Hardware, hypervisor | OS, apps |
| PaaS (e.g., RDS) | OS, platform | App configs |
| SaaS (e.g., S3) | All infra | Your data, IAM settings |

# **Part 3: Threat Actor Profile – APT41**

- **Origin**: China
- **TTPs**: Credential dumping, DLL injection, C2 over HTTPS
- **Targets**: Finance, healthcare, telcos
- **Malware Used**: Cobalt Strike, ShadowPad, PlugX

**IOCs to Watch**:

- Outbound traffic to dynamic DNS
- Creation of new IAM roles
- Unusual login times/IPs

# **Part 4: Malware Investigation**

## **Definitions:**

| **Type** | **Description** | **Example** |
| --- | --- | --- |
| **Ransomware** | Encrypts files, demands payment | WannaCry |
| **Rootkit** | Hides attacker’s presence | Necurs |
| **Trojan** | Disguises as legit software | Emotet |
| **Worm** | Self-replicates, spreads | Conficker |
| **Keylogger** | Captures keystrokes | HawkEye |

## **Most Likely in Scenario**: Ransomware (based on note, encryption, traffic)

- Real-World Similar Case: **DarkSide** ransomware in Colonial Pipeline Attack

# **Part 5: Access Control in Change Management**

## **Role-Based Access Control (RBAC)**

| **Role** | **Permissions** |
| --- | --- |
| DevOps | Deployments only |
| QA | Read-only test environments |
| Security | IAM, monitoring access |
| App Owners | Modify app configs only |

## **Change Authorization Workflow**

1. Propose: DevOps Team
2. Review: QA & Security
3. Approve: Cloud Architect
4. Deploy: Ops Team
5. Validate: Monitoring team

## **Logging & Auditing**

- Enable CloudTrail
- Centralized log storage in S3
- Real-time alerting via CloudWatch

## **Least Privilege**

- Time-bound IAM roles (e.g., 1-hour change window)
- Temporary credentials
- Automated revocation post-change

## **Mock Access Review Report**

| **User** | **Role** | **Temporary Access** | **Justification** |
| --- | --- | --- | --- |
| alice.dev | DevOps | Yes (2h) | Required to deploy patch |
| bob.sec | Security | Full | Audit firewall rule updates |
| jules.qa | QA | No | View-only testing validation |

## **Lessons Learned**

- Always use IAM policies with the principle of **least privilege**.
- Implement **real-time monitoring** of cloud changes.
- Run **continuous vulnerability scans** on cloud services.
- Segment your network to reduce the blast radius of malware.
- Enable **MFA and CloudTrail logging** by default.

 2025 Iniabasi Okorie | All Rights Reserved

🔗 LinkedIn: [linkedin.com/in/iniabasiokorie](https://linkedin.com/in/iniabasiokorie)

📌 Please do not copy, reproduce, or republish this content without permission.

Created by Iniabasi Okorie

Not for unauthorized distribution

[linkedin.com/in/iniabasiokorie](http://linkedin.com/in/iniabasiokorie)