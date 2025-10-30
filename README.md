<h1 align="center">FEDLIN</h1>
<p align="center"><b>Security Solutions Architecture · Vulnerability Management · Compliance Automation</b></p>
<p align="center">Independent / C2C · Subcontract-ready · Customer-tenant-first</p>

<p align="center">
  <img src="https://img.shields.io/badge/AWS-CloudTrail%20·%20Config%20·%20Security%20Hub-FF9900?logo=amazonaws&logoColor=white" />
  <img src="https://img.shields.io/badge/Azure-Entra%20ID%20·%20Defender%20·%20Policy-0078D4?logo=microsoftazure&logoColor=white" />
  <img src="https://img.shields.io/badge/GCP-Org%20Policies%20·%20SCC-4285F4?logo=googlecloud&logoColor=white" />
  <img src="https://img.shields.io/badge/M365-Entra%20Hardening-2358D5?logo=microsoft&logoColor=white" />
  <img src="https://img.shields.io/badge/GWS-HIPAA%20Baseline-0F9D58?logo=googleworkspace&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub%20Actions-OIDC%20CI%2FCD-000000?logo=githubactions&logoColor=white" />
  <img src="https://img.shields.io/badge/Compliance-SOC%202%20·%20ISO%2027001%20·%20HIPAA-6C757D" />
</p>

## About

FEDLIN is a security engineering and compliance automation consultancy. We build **customer-tenant-first** solutions — evidence, logs, and configuration stay in **your** AWS, Azure/Entra, Microsoft 365, Google Workspace, or GCP environment — and we deliver changes through **GitHub Actions with OIDC** so there are no long-lived secrets to rotate or vault.

We work well with security teams, MSPs, and primes that need to **show** cloud/SaaS security posture and **leave the evidence with the customer** — the way SOC 2, ISO 27001, and HIPAA-style reviews actually expect.

## What We Deliver

### 1) AWS Security Baseline
**What it is:** A starter-but-serious AWS hardening package.  
**What it does:** Turns on CloudTrail in all regions, enables AWS Config with sensible rules, tightens IAM, and sends logs to a customer-owned location.  
**Why it matters:** Looks like what SOC 2 / ISO 27001 reviewers expect to see when they ask “show me your logging and configuration posture.”  
**Repo:** https://github.com/fedlinllc/fedlin-aws-security-baseline

---

### 2) AWS “VistaSec” CMC (Continuous Monitoring Center)
**What it is:** The “prove it” layer on top of the baseline.  
**What it does:** Feeds AWS security signals (Security Hub, GuardDuty, etc.) into a view/report so security, compliance, or an MSP can actually **show** posture on demand.  
**Why it matters:** Lots of people can turn Security Hub on — not many package it as a repeatable service with clear scope.  
**Repo:** https://github.com/fedlinllc/fedlin-aws-vistasec-cmc

---

### 3) Microsoft 365 / Entra Security Baseline
**What it is:** Identity-first hardening for M365/Entra.  
**What it does:** Enforces MFA/Conditional Access, separates risky admin roles, dials back sharing defaults, and gets audit/eDiscovery ready.  
**Why it matters:** This is *exactly* what most “M365 Security Engineer / Architect” job posts describe — you’re just showing it from a consulting org’s perspective.  
**Repo:** https://github.com/fedlinllc/fedlin-m365-security-baseline

---

### 4) Google Workspace HIPAA Baseline
**What it is:** A GWS security tune-up for telehealth/therapy/PHI-adjacent shops.  
**What it does:** Cleans up admin roles, locks down Drive/sharing, enforces 2SV, and tells the customer where to keep evidence — without leaking tenant details to GitHub.  
**Why it matters:** GWS security shows up less often than Microsoft, so having it here is a differentiator for recruiters.  
**Repo:** https://github.com/fedlinllc/fedlin-gws-hipaa-baseline

---

### 5) Email Authentication (DMARC / SPF / DKIM)
**What it is:** The “make your mail pass security reviews” service.  
**What it does:** Configures SPF for M365/GWS, turns on DKIM, rolls out DMARC safely (none → monitor → enforce), and can validate via CI.  
**Why it matters:** This is the small-but-annoying piece a lot of customers ask for after a security baseline — having it productized makes you look organized.  
**Repo:** https://github.com/fedlinllc/fedlin-dmarc-spf-dkim

---

**Delivery pattern for all of the above:** `SERVICE_SCOPE.md` → `EVIDENCE_MODEL.md` → `DELIVERY_MODEL.md` → GitHub Actions (OIDC-only). That’s why this is easy to subcontract or hand to an MSP.


How we engage (business / C2C)

C2C / 1099 friendly. Independent consultant model supported.

Subcontract-ready. Each repo has a defined scope so primes can see what’s delivered.

Customer-owned evidence. We do not insist on hosting your logs/exports — we show you where to put them.

Secure delivery. GitHub Actions with OIDC → no long-lived AWS/Microsoft credentials to rotate.

Contact

Website: https://www.fedlin.com
