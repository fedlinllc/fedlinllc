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

<p align="center">
  <img src="https://img.shields.io/badge/IaC-Terraform%20·%20Bicep-informational" />
  <img src="https://img.shields.io/badge/Policy-as-code-AWS%20%2F%20Azure%20controls-informational" />
  <img src="https://img.shields.io/badge/Automation-bash%20·%20python-informational" />
  <img src="https://img.shields.io/badge/Practice-DevSecOps-informational" />
</p>

## About

FEDLIN is a security engineering and compliance automation consultancy. We build **customer-tenant-first** solutions — evidence, logs, and configuration stay in **your** AWS, Azure/Entra, Microsoft 365, Google Workspace, or GCP environment — and we deliver changes through **GitHub Actions with OIDC** so there are no long-lived secrets to rotate or vault.

We work well with security teams, MSPs, and primes that need to **show** cloud/SaaS security posture and **leave the evidence with the customer** — the way SOC 2, ISO 27001, and HIPAA-style reviews actually expect.

## What We Deliver

### AWS Security Baseline Implementation
<p>
  <img src="https://img.shields.io/badge/AWS-CloudTrail%20·%20Config-FF9900?logo=amazonaws&logoColor=white" />
  <img src="https://img.shields.io/badge/Delivery-GitHub%20Actions%20(OIDC)-000000?logo=githubactions&logoColor=white" />
  <img src="https://img.shields.io/badge/IaC-Terraform%20(optional)-5C4EE5" />
  <img src="https://img.shields.io/badge/Compliance-SOC%202%20·%20ISO%2027001-6C757D" />
</p>
Establishes CloudTrail (all regions), AWS Config with baseline rules, IAM hygiene, and customer-owned logging to support SOC 2 / ISO 27001 style reviews.  
→ https://github.com/fedlinllc/fedlin-aws-security-baseline

---

### AWS Continuous Monitoring (VistaSec CMC)
<p>
  <img src="https://img.shields.io/badge/AWS-Security%20Hub%20·%20GuardDuty-FF9900?logo=amazonaws&logoColor=white" />
  <img src="https://img.shields.io/badge/Use--case-Continuous%20Monitoring-blue" />
  <img src="https://img.shields.io/badge/Automation-python%20·%20bash-000000" />
  <img src="https://img.shields.io/badge/For-Security%20·%20Compliance%20·%20MSP-6C757D" />
</p>
Extends the baseline with a reporting/visibility layer so security, compliance, or MSP stakeholders can review AWS posture without manual exports.  
→ https://github.com/fedlinllc/fedlin-aws-vistasec-cmc

---

### Microsoft 365 / Entra Security Hardening
<p>
  <img src="https://img.shields.io/badge/M365-MFA%20·%20CA-2358D5?logo=microsoft&logoColor=white" />
  <img src="https://img.shields.io/badge/Entra-Admin%20role%20separation-0078D4?logo=microsoftazure&logoColor=white" />
  <img src="https://img.shields.io/badge/Outcome-Audit%20%2F%20eDiscovery%20ready-6C757D" />
  <img src="https://img.shields.io/badge/Policy-as-code-CA%20%2F%20M365%20profiles-informational" />
</p>
Applies identity-first controls (MFA/Conditional Access), separates privileged roles, aligns collaboration/sharing defaults, and enables audit/eDiscovery for regulated environments.  
→ https://github.com/fedlinllc/fedlin-m365-security-baseline

---

### Google Workspace HIPAA-Oriented Baseline
<p>
  <img src="https://img.shields.io/badge/GWS-Sharing%20controls-0F9D58?logo=googleworkspace&logoColor=white" />
  <img src="https://img.shields.io/badge/Security-2SV%20·%20Admin%20hygiene-0F9D58?logo=google&logoColor=white" />
  <img src="https://img.shields.io/badge/Vertical-Telehealth%20%2F%20Therapy-orange" />
  <img src="https://img.shields.io/badge/Automation-admin%20scripts-lightgrey" />
</p>
Secures Google Workspace for clinics, telehealth, and PHI-adjacent organizations by tightening admin roles, sharing controls, and sign-in protections while keeping evidence in the customer tenant.  
→ https://github.com/fedlinllc/fedlin-gws-hipaa-baseline

---

### Email Authentication Configuration (DMARC / SPF / DKIM)
<p>
  <img src="https://img.shields.io/badge/Email-DMARC%20·%20SPF%20·%20DKIM-6C757D" />
  <img src="https://img.shields.io/badge/DNS-Customer--owned-blue" />
  <img src="https://img.shields.io/badge/Option-CI--based%20validation-000000?logo=githubactions&logoColor=white" />
  <img src="https://img.shields.io/badge/Scripting-bash%20·%20python-lightgrey" />
</p>
Implements sender authentication for Microsoft 365 and Google Workspace domains (SPF, DKIM) and introduces a staged DMARC policy (none → monitor → enforce), with optional CI-driven validation.  
→ https://github.com/fedlinllc/fedlin-dmarc-spf-dkim

---

**Common delivery approach:** `SERVICE_SCOPE.md` → `EVIDENCE_MODEL.md` → `DELIVERY_MODEL.md` → GitHub Actions (OIDC-only), with Terraform/Bicep, policy-as-code, and bash/python automation applied where appropriate.
::contentReference[oaicite:0]{index=0}


## How we engage (business / C2C)

- **C2C / 1099 friendly.** Independent consultant model supported.
- **Subcontract-ready.** Each repo has a defined scope so primes can see what’s delivered.
- **Customer-owned evidence.** We do not insist on hosting your logs/exports — we show you where to put them.
- **Secure delivery.** GitHub Actions with OIDC → no long-lived AWS/Microsoft credentials to rotate.

## Contact

Website: https://www.fedlin.com
Email: info@fedlin.com
