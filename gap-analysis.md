# Gap Analysis — NimbusCore Inc.

**Framework:** NIST CSF v1.1 + ISO/IEC 27001:2022  
**Company:** NimbusCore Inc. (Fictional SaaS / Cloud)  
**Analyst:** Gerardo Hernandez  
**Date:** 2025  

---

## Executive Summary

NimbusCore Inc. is a growing SaaS company processing sensitive HR and payroll data for approximately 300 SMB clients. While the company has implemented foundational technical controls such as encryption at rest and in transit and remote access via VPN and SSO, a significant number of governance, operational, and response-oriented controls are either absent or only partially implemented.

Of 23 controls assessed across the NIST CSF and ISO 27001 frameworks:

- **3 controls (13%)** are fully implemented
- **10 controls (43%)** are partially implemented with notable gaps
- **10 controls (43%)** are not implemented at all

This represents a material compliance and risk gap, particularly given NimbusCore's plans to pursue SOC 2 Type II certification and its handling of PII and financial data subject to CCPA and GDPR.

---

## Gap Analysis by Domain

### 1. Governance (IDENTIFY)

**Current State:**  
NimbusCore has no formal Information Security Policy in place. While executive leadership acknowledges security as a priority, no policy has been documented, approved, or communicated to employees.

**Gap:**  
Without a formal policy, the organization lacks a foundational governance document that all other controls depend on. Auditors for SOC 2 and ISO 27001 will require this as a first-order deliverable.

**Risk Exposure:**  
High. Regulatory violations (GDPR, CCPA) and failed audit findings are probable without documented policies.

**Recommended Actions:**
- Draft an Information Security Policy covering scope, objectives, roles, and responsibilities
- Obtain executive sign-off and distribute to all employees
- Schedule annual policy review

---

### 2. Asset Management (IDENTIFY)

**Current State:**  
No formal asset inventory exists for either hardware or software. AWS resources are partially documented in informal notes, but there is no centralized, maintained inventory.

**Gap:**  
Without knowing what assets exist, the organization cannot effectively prioritize protection, manage vulnerabilities, or respond to incidents involving specific systems.

**Risk Exposure:**  
High. Untracked assets are a common source of undetected breaches and audit failures.

**Recommended Actions:**
- Enable AWS Config to auto-discover and track cloud resources
- Build a software/application inventory spreadsheet and assign owners
- Schedule quarterly asset inventory reviews

---

### 3. Risk Assessment (IDENTIFY)

**Current State:**  
No formal risk register or vulnerability management process exists. There have been no scheduled vulnerability scans, and threats are not formally identified or documented.

**Gap:**  
Risk decisions are being made without a documented process, leading to inconsistent prioritization and potential blind spots.

**Risk Exposure:**  
High. Unidentified vulnerabilities in a system handling SSNs and financial data could lead to regulatory penalties and client data breaches.

**Recommended Actions:**
- Create a formal Risk Register (see Project 2 in this portfolio)
- Deploy Amazon Inspector or an equivalent tool for vulnerability scanning
- Schedule quarterly risk review meetings

---

### 4. Access Control (PROTECT)

**Current State:**  
MFA is enforced for admin accounts only. Regular employee accounts, including those with access to customer data in the application, do not require MFA. IAM permissions in AWS are broader than necessary for some engineering team members.

**Gap:**  
The lack of universal MFA is a critical gap. Most credential-based attacks succeed against accounts without MFA. Overly broad IAM permissions increase the blast radius of any compromise.

**Risk Exposure:**  
High. This is one of the most common root causes of SaaS data breaches.

**Recommended Actions:**
- Enforce MFA for all users via Okta policy, not just admins
- Run AWS IAM Access Analyzer and remediate excessive permissions within 30 days
- Implement a quarterly access review process

---

### 5. Security Awareness Training (PROTECT)

**Current State:**  
Training was conducted 18 months ago. There is no recurring program, no phishing simulation, and no tracking of completion.

**Gap:**  
Employees are a primary attack vector (phishing, social engineering). A stale training program provides minimal protection.

**Risk Exposure:**  
Medium. Without regular training, employees are likely unaware of current threat tactics.

**Recommended Actions:**
- Implement a recurring annual training program (minimum)
- Add quarterly phishing simulations using a free tool such as GoPhish
- Track completion rates and follow up with non-completions

---

### 6. Data Loss Prevention (PROTECT)

**Current State:**  
No formal DLP solution is in place. There is no data classification policy, meaning employees may not know which data requires the highest level of protection.

**Gap:**  
Without data classification and DLP controls, sensitive data such as SSNs and bank account numbers could be exfiltrated without detection.

**Risk Exposure:**  
Medium. A breach of this data could trigger breach notification requirements under CCPA, GDPR, and state laws.

**Recommended Actions:**
- Develop a Data Classification Policy (Confidential, Internal, Public)
- Evaluate AWS Macie for automated sensitive data detection in S3
- Add DLP to the roadmap for the next 6 months

---

### 7. Incident Response (PROTECT / RESPOND)

**Current State:**  
No documented incident response plan exists. The company has responded to minor incidents informally, but roles, escalation paths, communication templates, and playbooks are not defined.

**Gap:**  
When an incident occurs, response time and effectiveness depend entirely on the individuals present. This is both a compliance gap and an operational risk.

**Risk Exposure:**  
High. GDPR requires breach notification within 72 hours. Without an IR plan, meeting this obligation is unlikely.

**Recommended Actions:**
- Draft an Incident Response Plan using NIST SP 800-61 as a reference
- Define at minimum: roles and responsibilities, severity classification, escalation matrix, and communication templates
- Conduct a tabletop exercise simulating a phishing-based data breach

---

### 8. Monitoring and Detection (DETECT)

**Current State:**  
AWS CloudWatch and Datadog are deployed, but no formal baseline has been established. Alerts exist but escalation procedures are informal, and no process exists to detect unauthorized accounts or devices.

**Gap:**  
Without defined baselines and response procedures, monitoring tools generate noise rather than actionable intelligence.

**Risk Exposure:**  
Medium to High. Unauthorized access could go undetected for an extended period.

**Recommended Actions:**
- Enable AWS GuardDuty for threat detection
- Define alert thresholds and an escalation procedure for each alert type
- Implement a monthly IAM access review to detect unauthorized accounts

---

### 9. Recovery Planning (RECOVER)

**Current State:**  
No Disaster Recovery Plan exists. Recovery Time Objectives (RTO) and Recovery Point Objectives (RPO) have not been defined. AWS backup is configured but has not been tested.

**Gap:**  
NimbusCore cannot commit to its clients on recovery timelines, and has no assurance that backups can actually be restored successfully.

**Risk Exposure:**  
High. An untested backup is not a backup. A ransomware event or data center failure could result in extended downtime and client SLA violations.

**Recommended Actions:**
- Define RTO and RPO for each critical system
- Test AWS backup and restore procedures quarterly
- Document a basic Disaster Recovery Plan and assign an owner

---

## Prioritized Remediation Roadmap

### Immediate (0 to 30 days) — High Priority

| # | Action | Owner |
|---|---|---|
| 1 | Draft and publish Information Security Policy | Jordan Mills |
| 2 | Enforce MFA for all Okta accounts | Marcus Reyes |
| 3 | Run IAM Access Analyzer and remediate excessive permissions | Marcus Reyes |
| 4 | Draft Incident Response Plan (basic version) | Dana Cho |
| 5 | Enable AWS GuardDuty | Dana Cho |
| 6 | Enable AWS Config for asset discovery | Dana Cho |

### Short-Term (30 to 90 days) — Medium Priority

| # | Action | Owner |
|---|---|---|
| 7 | Create a formal Risk Register | Dana Cho |
| 8 | Implement recurring security awareness training | Dana Cho |
| 9 | Define alert baselines and escalation procedures in Datadog | Marcus Reyes |
| 10 | Draft Data Classification Policy | Dana Cho |
| 11 | Define RTO/RPO and test backup restoration | Marcus Reyes |

### Long-Term (90+ days) — Ongoing

| # | Action | Owner |
|---|---|---|
| 12 | Conduct quarterly access reviews | Dana Cho |
| 13 | Deploy DLP solution (AWS Macie or equivalent) | Marcus Reyes |
| 14 | Conduct annual tabletop IR exercise | Dana Cho |
| 15 | Map all controls to SOC 2 Trust Service Criteria for audit readiness | Dana Cho |

---

## Conclusion

NimbusCore is in the early stages of building a mature security program. The good news is that foundational technical controls around encryption and access are partially in place. The critical gaps are in governance, documentation, and response planning. Addressing the immediate remediation items above will significantly reduce risk exposure and lay the groundwork for a successful SOC 2 Type II audit.
