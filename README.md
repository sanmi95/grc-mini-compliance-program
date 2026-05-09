# GRC Mini Compliance Program — NimbusCore Inc.

> A hands-on GRC portfolio project simulating a real-world compliance program for a fictional SaaS company, built to demonstrate practical GRC analyst skills across NIST CSF and ISO 27001.

---

## About This Project

This project was built as part of a GRC Analyst portfolio to demonstrate real-world skills in compliance program design, risk assessment, gap analysis, and policy development.

**Fictional Company:** NimbusCore Inc. — a cloud-based HR and payroll SaaS platform serving ~300 SMB clients on AWS.

**Frameworks Used:**
- NIST Cybersecurity Framework (CSF) v1.1
- ISO/IEC 27001:2022 (Annex A controls)

**Project Goal:** Establish a baseline compliance program, identify gaps against NIST CSF and ISO 27001, and produce the core documentation a company would need to begin a formal security program or prepare for a SOC 2 Type II audit.

---

## Repository Structure

```
grc-mini-compliance-program/
│
├── README.md
│
├── company-profile/
│   └── fictional-company.md        # Company background, tech stack, data handled, current posture
│
├── compliance-framework/
│   ├── control-mapping.md          # 23 controls mapped across NIST CSF + ISO 27001 (Markdown)
│   ├── control-mapping.xlsx        # Same mapping in Excel with color-coded status dashboard
│   └── gap-analysis.md             # Detailed narrative gap analysis with remediation roadmap
│
├── policies/
│   ├── information-security-policy.md   # Formal InfoSec policy document
│   └── acceptable-use-policy.md         # AUP for employees and contractors
│
└── evidence/
    └── sample-evidence-log.md      # Simulated evidence collection log (15 control items)
```

---

## Key Deliverables

### 1. Company Profile
Defines the fictional company scenario including industry, tech stack, data types handled, regulatory obligations, and baseline security posture. This is the foundation all other deliverables are built on.

### 2. Control Mapping (NIST CSF + ISO 27001)
23 controls assessed across all 5 NIST CSF functions (Identify, Protect, Detect, Respond, Recover), each mapped to the corresponding ISO 27001 Annex A reference.

Each control includes:
- Current implementation status (Implemented / Partial / Not Implemented)
- Gap description
- Priority rating (High / Medium / Low)
- Control owner

**Results:**
| Status | Count | % |
|---|---|---|
| Implemented | 3 | 13% |
| Partial | 10 | 43% |
| Not Implemented | 10 | 43% |

### 3. Gap Analysis
A detailed narrative document covering each domain with context, risk exposure, and specific recommended actions. Includes a prioritized remediation roadmap broken into 0-30 days, 30-90 days, and 90+ day horizons.

### 4. Policies
Two foundational policy documents that any company would need as a starting point for a formal security program:
- **Information Security Policy** — covers governance, data classification, access control, incident reporting, and training requirements
- **Acceptable Use Policy** — defines permitted and prohibited uses of company systems

### 5. Evidence Log
A simulated evidence collection log showing how a GRC analyst gathers and documents evidence for 15 controls during an assessment. Includes evidence type, source, status, and notes on gaps identified.

---

## Skills Demonstrated

- GRC framework knowledge (NIST CSF v1.1, ISO 27001:2022)
- Control mapping and cross-framework alignment
- Gap analysis and risk-based prioritization
- Security policy development
- Evidence collection methodology
- Cloud security context (AWS services)
- Documentation and communication for audit readiness

---

## Tools and Technologies Referenced

| Tool | Purpose |
|---|---|
| AWS (EC2, RDS, S3, IAM, CloudTrail) | Cloud infrastructure controls |
| AWS Config | Asset inventory and configuration tracking |
| AWS GuardDuty | Threat detection |
| AWS IAM Access Analyzer | Least privilege assessment |
| AWS Inspector | Vulnerability scanning |
| Okta | Identity and access management, MFA |
| Datadog | Monitoring and alerting |
| GitHub Actions | CI/CD pipeline |

---

## How This Maps to Real GRC Work

| This Project | Real-World Equivalent |
|---|---|
| Control mapping spreadsheet | SOC 2 readiness assessment, ISO 27001 gap assessment |
| Gap analysis document | Audit finding report, risk assessment deliverable |
| Policies | Production security policies required for certification |
| Evidence log | Audit evidence package for SOC 2 or ISO 27001 |
| Remediation roadmap | Risk treatment plan, corrective action plan (CAP) |

---

## About

Built by **Gerardo Hernandez** as part of a hands-on GRC Analyst portfolio.

All company names, personnel, and scenarios in this project are entirely fictional and created for educational and portfolio purposes only.

---

## Related Projects in This Portfolio

- Project 2: Risk Register for a Mock Company
- Project 3: Third-Party Vendor Assessment Template
- Project 4: Incident Response Plan
- Project 5: SOC 2 Control Mapping to AWS
- Project 6: Compliance Dashboard
- Project 7: Mock Internal Audit
