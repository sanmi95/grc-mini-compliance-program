# Control Mapping — NimbusCore Inc.

**Frameworks:** NIST CSF v1.1 + ISO/IEC 27001:2022  
**Company:** NimbusCore Inc. (Fictional)  
**Review Date:** 2025  
**Total Controls Assessed:** 23

---

## Status Key

| Badge | Meaning |
|---|---|
| ✅ Implemented | Control is fully in place and documented |
| ⚠️ Partial | Control exists but has gaps or is inconsistently applied |
| ❌ Not Implemented | Control does not exist; remediation required |

## Priority Key

| Badge | Meaning | Timeframe |
|---|---|---|
| 🔴 High | Significant risk exposure | Remediate within 30 days |
| 🟠 Medium | Moderate risk | Remediate within 90 days |
| 🟢 Low | Minor gap or compensating control exists | Monitor |

---

## IDENTIFY

| Control ID | NIST Category | ISO 27001 Ref | Control Description | Status | Priority | Owner |
|---|---|---|---|---|---|---|
| ID.AM-1 | Asset Management | A.8.1 | Physical devices and systems within the organization are inventoried. | ❌ Not Implemented | 🔴 High | Dana Cho |
| ID.AM-2 | Asset Management | A.8.1 | Software platforms and applications within the organization are inventoried. | ⚠️ Partial | 🔴 High | Dana Cho |
| ID.GV-1 | Governance | A.5.1 | Organizational information security policy is established and communicated. | ❌ Not Implemented | 🔴 High | Jordan Mills |
| ID.GV-3 | Governance | A.18.1 | Legal and regulatory requirements regarding cybersecurity are understood and managed. | ⚠️ Partial | 🟠 Medium | Legal/Compliance |
| ID.RA-1 | Risk Assessment | A.8.2 | Asset vulnerabilities are identified and documented. | ❌ Not Implemented | 🔴 High | Dana Cho |
| ID.RA-3 | Risk Assessment | A.6.1 | Threats, both internal and external, are identified and documented. | ❌ Not Implemented | 🔴 High | Dana Cho |

---

## PROTECT

| Control ID | NIST Category | ISO 27001 Ref | Control Description | Status | Priority | Owner |
|---|---|---|---|---|---|---|
| PR.AC-1 | Access Control | A.9.2 | Identities and credentials are managed for authorized devices, users and processes. | ⚠️ Partial | 🔴 High | Marcus Reyes |
| PR.AC-3 | Access Control | A.9.4 | Remote access is managed. | ✅ Implemented | 🟢 Low | Marcus Reyes |
| PR.AC-4 | Access Control | A.9.1 | Access permissions are managed, incorporating principles of least privilege and separation of duties. | ⚠️ Partial | 🔴 High | Marcus Reyes |
| PR.AT-1 | Awareness and Training | A.7.2 | All users are informed and trained. | ⚠️ Partial | 🟠 Medium | Dana Cho |
| PR.DS-1 | Data Security | A.8.3 | Data-at-rest is protected. | ✅ Implemented | 🟢 Low | Marcus Reyes |
| PR.DS-2 | Data Security | A.13.2 | Data-in-transit is protected. | ✅ Implemented | 🟢 Low | Marcus Reyes |
| PR.DS-5 | Data Security | A.13.1 | Protections against data leaks are implemented. | ⚠️ Partial | 🟠 Medium | Dana Cho |
| PR.IP-1 | Info Protection Processes | A.12.1 | A baseline configuration of information technology is created and maintained. | ⚠️ Partial | 🟠 Medium | Marcus Reyes |
| PR.IP-9 | Info Protection Processes | A.16.1 | Response plans (Incident Response, Business Continuity, Disaster Recovery) are in place. | ❌ Not Implemented | 🔴 High | Dana Cho |

---

## DETECT

| Control ID | NIST Category | ISO 27001 Ref | Control Description | Status | Priority | Owner |
|---|---|---|---|---|---|---|
| DE.AE-1 | Anomalies and Events | A.12.4 | A baseline of network operations and expected data flows is established. | ⚠️ Partial | 🟠 Medium | Marcus Reyes |
| DE.CM-1 | Continuous Monitoring | A.12.4 | The network is monitored to detect potential cybersecurity events. | ⚠️ Partial | 🟠 Medium | Dana Cho |
| DE.CM-7 | Continuous Monitoring | A.12.6 | Monitoring for unauthorized personnel, connections, devices, and software is performed. | ❌ Not Implemented | 🔴 High | Dana Cho |

---

## RESPOND

| Control ID | NIST Category | ISO 27001 Ref | Control Description | Status | Priority | Owner |
|---|---|---|---|---|---|---|
| RS.RP-1 | Response Planning | A.16.1 | Response plan is executed during or after an event. | ❌ Not Implemented | 🔴 High | Dana Cho |
| RS.CO-2 | Communications | A.16.1 | Events are reported consistent with established criteria. | ❌ Not Implemented | 🔴 High | Jordan Mills |
| RS.AN-1 | Analysis | A.16.1 | Notifications from detection systems are investigated. | ⚠️ Partial | 🟠 Medium | Dana Cho |

---

## RECOVER

| Control ID | NIST Category | ISO 27001 Ref | Control Description | Status | Priority | Owner |
|---|---|---|---|---|---|---|
| RC.RP-1 | Recovery Planning | A.17.1 | Recovery plan is executed during or after an event. | ❌ Not Implemented | 🔴 High | Marcus Reyes |
| RC.IM-1 | Improvements | A.16.1 | Recovery plans incorporate lessons learned. | ❌ Not Implemented | 🟠 Medium | Dana Cho |

---

## Summary

| Status | Count | % of Total |
|---|---|---|
| ✅ Implemented | 3 | 13% |
| ⚠️ Partial | 10 | 43% |
| ❌ Not Implemented | 10 | 43% |
| **Total** | **23** | **100%** |

| Priority | Count |
|---|---|
| 🔴 High | 12 |
| 🟠 Medium | 8 |
| 🟢 Low | 3 |
