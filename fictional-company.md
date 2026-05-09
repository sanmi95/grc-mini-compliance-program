# NimbusCore Inc. — Company Profile

## Overview

| Field | Details |
|---|---|
| **Company Name** | NimbusCore Inc. |
| **Industry** | SaaS / Cloud Services |
| **Founded** | 2019 |
| **Headquarters** | Austin, Texas, USA |
| **Employees** | ~85 |
| **Customers** | ~300 SMB clients across North America |
| **Annual Revenue** | ~$4.2M ARR |

---

## What NimbusCore Does

NimbusCore provides a cloud-based HR and payroll management platform for small and mid-sized businesses. Clients use the platform to manage employee records, run payroll, and store sensitive HR documents. The platform is hosted entirely on AWS (us-east-1).

---

## Technology Stack

| Component | Technology |
|---|---|
| Cloud Provider | Amazon Web Services (AWS) |
| Primary Services | EC2, RDS (PostgreSQL), S3, IAM, CloudTrail |
| Application | Multi-tenant SaaS web app (React + Node.js) |
| Authentication | SSO via Okta, MFA enforced for admin roles |
| CI/CD | GitHub Actions + AWS CodeDeploy |
| Monitoring | AWS CloudWatch + Datadog |

---

## Data Handled

NimbusCore processes and stores the following sensitive data categories:

- **PII** — Full names, addresses, dates of birth, Social Security Numbers (SSNs)
- **Financial data** — Bank account numbers, salary information, tax records
- **HR documents** — Employment contracts, performance reviews, disciplinary records
- **Authentication credentials** — Hashed passwords, session tokens, API keys

---

## Regulatory Context

| Obligation | Notes |
|---|---|
| SOC 2 Type II | In progress — target audit date Q4 2025 |
| GDPR | Applicable for EU-based contractor data |
| State privacy laws | California (CCPA), Texas (TDPSA) |
| Internal policy | ISO 27001 alignment as strategic goal |

---

## Organizational Structure (Security-Relevant)

| Role | Name (Fictional) | Responsibility |
|---|---|---|
| CEO | Jordan Mills | Executive sponsor for security program |
| CTO | Priya Nair | Owns technology and infrastructure decisions |
| Head of Engineering | Marcus Reyes | Manages dev team, code review, deployments |
| IT/Security Lead | Dana Cho | Day-to-day security operations, GRC program owner |
| Legal/Compliance | External counsel | GDPR and contract review |

---

## Current Security Posture (Baseline)

NimbusCore has some basic security controls in place but lacks a formal compliance program. Key observations:

- MFA is enforced for admin accounts but **not** for all employees
- No formal risk register exists
- Incident response plan is informal and undocumented
- Vendor security assessments are done ad hoc, with no standard questionnaire
- Security awareness training was last done 18 months ago
- No formal asset inventory or data classification policy exists

---

## Purpose of This Compliance Program

This mini compliance program was created to:

1. Establish a baseline against NIST CSF and ISO 27001 controls
2. Identify and prioritize gaps in the current security posture
3. Lay the groundwork for a future SOC 2 Type II audit
4. Build repeatable GRC processes that can scale as the company grows
