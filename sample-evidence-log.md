# Sample Evidence Log — NimbusCore Inc.

**Purpose:** This log simulates the type of evidence a GRC analyst would collect during a compliance assessment or internal audit to validate that controls are implemented.

**Company:** NimbusCore Inc. (Fictional)  
**Analyst:** Gerardo Hernandez  
**Assessment Date:** 2025  

---

> **Note:** In a real-world engagement, each evidence item would include a screenshot, exported report, or document attached to a ticketing or GRC platform (e.g., Vanta, Drata, ServiceNow GRC). This log demonstrates the evidence collection process.

---

## Evidence Items

| Evidence ID | Control ID | NIST Function | Evidence Type | Description | Source | Status | Notes |
|---|---|---|---|---|---|---|---|
| EV-001 | PR.DS-1 | PROTECT | Screenshot | AWS S3 default encryption enabled for all client data buckets | AWS Console — S3 Bucket Properties | Collected | Verified encryption using AES-256 via AWS-managed keys |
| EV-002 | PR.DS-2 | PROTECT | Screenshot | AWS ALB listener enforcing HTTPS (TLS 1.2+) only; HTTP redirected | AWS Console — Load Balancer Listeners | Collected | HTTP to HTTPS redirect confirmed on all public endpoints |
| EV-003 | PR.DS-1 | PROTECT | Screenshot | AWS RDS PostgreSQL instance encryption at rest enabled | AWS Console — RDS Instance Settings | Collected | Encryption enabled at instance creation; cannot be disabled |
| EV-004 | PR.AC-3 | PROTECT | Screenshot | Okta VPN and SSO sign-in policies enforcing authentication before access | Okta Admin Console — Sign-On Policies | Collected | All users required to authenticate via Okta before accessing internal tools |
| EV-005 | PR.AC-1 | PROTECT | Screenshot | Okta MFA policy showing MFA enforced for admin group only | Okta Admin Console — MFA Enrollment Policy | Gap Identified | Regular employees not enrolled in MFA. Remediation required. |
| EV-006 | DE.CM-1 | DETECT | Export | AWS CloudTrail enabled across all regions; log archive in S3 | AWS CloudTrail — Trails Configuration | Collected | Logs retained for 90 days in S3 with CloudWatch integration |
| EV-007 | DE.CM-1 | DETECT | Screenshot | Datadog dashboard showing active monitors for EC2 CPU, memory, and error rates | Datadog — Monitors Overview | Collected | No defined alert thresholds or escalation procedure documented |
| EV-008 | ID.AM-1 | IDENTIFY | N/A | No formal asset inventory found | IT/Security Lead interview | Gap Identified | Asset tracking relies on informal notes. No centralized inventory tool. |
| EV-009 | ID.GV-1 | IDENTIFY | N/A | No Information Security Policy document found | Document repository review | Gap Identified | No formal policy has been drafted, approved, or communicated |
| EV-010 | PR.IP-9 | PROTECT | N/A | No incident response plan found | Document repository review | Gap Identified | IR process is entirely informal; no playbooks or escalation matrix exist |
| EV-011 | RC.RP-1 | RECOVER | Screenshot | AWS Backup plan configured for RDS with 7-day retention | AWS Console — AWS Backup | Partial | Backup exists but no documented recovery test has been performed |
| EV-012 | PR.AT-1 | PROTECT | Email record | Security awareness training completion email from 18 months ago | Email archive | Gap Identified | No recurring training program; last training was a one-time event |
| EV-013 | PR.AC-4 | PROTECT | Export | AWS IAM Access Analyzer findings showing 3 IAM roles with excessive permissions | AWS IAM Access Analyzer — Findings | Gap Identified | Engineer roles have S3:* and IAM:* permissions not required for their function |
| EV-014 | DE.CM-7 | DETECT | N/A | No IAM access review process found | IT/Security Lead interview | Gap Identified | No scheduled review of user accounts; no process to detect inactive or unauthorized accounts |
| EV-015 | ID.RA-1 | IDENTIFY | N/A | No vulnerability scan results found | Document and tool review | Gap Identified | No vulnerability scanner deployed; no scheduled scan cadence |

---

## Evidence Collection Summary

| Status | Count |
|---|---|
| Collected (control operating) | 6 |
| Partial (control exists with gaps) | 1 |
| Gap Identified (control not operating) | 8 |
| **Total** | **15** |

---

## How to Use This Log

In a real GRC engagement or SOC 2 audit, the analyst would:

1. Map each control to an evidence request
2. Collect screenshots, exports, or configuration reports from each system
3. Label and organize evidence in a shared folder (e.g., by control ID)
4. Note any gaps discovered during collection
5. Include evidence references in the audit report or gap analysis

This log would typically be maintained in a GRC platform such as Vanta, Drata, or Tugboat Logic, or in a shared folder with consistent naming conventions.

---

*NimbusCore Inc. — Sample Evidence Log — Fictional document created for portfolio purposes*
