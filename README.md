<h1 align="center">FEDLIN</h1>
<p align="center"><b>Security Solutions Architecture · Cloud/SaaS Hardening · Evidence-Driven Compliance</b></p>
<p align="center">Independent / C2C · Subcontract-ready · Customer-tenant-first</p>

<p align="center">
  <!-- cloud platforms -->
  <img src="https://img.shields.io/badge/AWS-CloudTrail%20·%20Config%20·%20Security%20Hub-blue" />
  <img src="https://img.shields.io/badge/M365-Entra%20ID%20·%20Conditional%20Access-blueviolet" />
  <img src="https://img.shields.io/badge/GWS-SaaS%20Security%20·%20HIPAA-green" />
  <!-- delivery -->
  <img src="https://img.shields.io/badge/GitHub%20Actions-OIDC%20CI%2FCD-important" />
  <!-- compliance -->
  <img src="https://img.shields.io/badge/Compliance-SOC%202%20·%20ISO%2027001%20·%20HIPAA-lightgrey" />
</p>

## About

FEDLIN is a security engineering and compliance automation consultancy. We build **customer-tenant-first** solutions — evidence, logs, and configuration stay in **your** AWS, Microsoft 365 / Entra, or Google Workspace environment — and we deliver changes through **GitHub Actions with OIDC** so there are no long-lived secrets to rotate or vault.

We’re a good fit for security teams, MSPs, and primes who need to **show AWS/M365 security posture** and **leave the evidence with the customer** — the way SOC 2 / ISO 27001 / HIPAA reviews actually expect. :contentReference[oaicite:5]{index=5}

## What we deliver

- **AWS Security Baseline** — CloudTrail, Config, IAM hygiene, Security Hub/GuardDuty ready; documented for SOC 2 / ISO 27001 reviewers. :contentReference[oaicite:6]{index=6}
- **AWS “VistaSec” CMC** — monitoring/reporting layer on top of the baseline so stakeholders can prove posture on demand. :contentReference[oaicite:7]{index=7}
- **M365 / Entra Security Baseline** — MFA/Conditional Access, admin-role separation, collaboration/sharing controls, eDiscovery/audit readiness. :contentReference[oaicite:8]{index=8}
- **Google Workspace HIPAA Baseline** — GWS hardening for telehealth / therapy / PHI-adjacent orgs; tenant-safe. :contentReference[oaicite:9]{index=9}
- **DMARC / SPF / DKIM** — email/DNS authentication for Microsoft 365 and Google Workspace, with optional CI-based validation.
- **All delivered via GitHub Actions (OIDC-only)** — modern, secretless, contractor-friendly delivery. :contentReference[oaicite:10]{index=10}


1) AWS Security Baseline
https://github.com/fedlinllc/fedlin-aws-security-baseline
flowchart LR
    A[AWS Account] --> B[Enable CloudTrail<br/>all regions]
    A --> C[Enable AWS Config<br/>baseline rules]
    A --> D[IAM Hygiene<br/>root/MFA/policy]
    B --> E[S3 Logging Bucket<br/>customer-owned]
    C --> E
    D --> F[Evidence Captured<br/>in customer account]
    G[GitHub Actions<br/>(OIDC)] --> A
    G --> F

2) AWS VistaSec CMC (continuous monitoring center)
https://github.com/fedlinllc/fedlin-aws-vistasec-cmc
flowchart LR
    A[AWS Baseline Ready] --> B[Security Hub / GuardDuty]
    B --> C[Findings / Alerts]
    C --> D[VistaSec CMC View<br/>GitHub / Reports]
    D --> E[Security / Compliance / MSP]
    G[GitHub Actions<br/>(OIDC)] --> B
    G --> D
3) Microsoft 365 / Entra Security Baseline
https://github.com/fedlinllc/fedlin-m365-security-baseline
flowchart LR
    A[Entra / M365 Tenant] --> B[Identity Hardening<br/>MFA + CA]
    A --> C[Admin Role Separation]
    A --> D[SharePoint / OneDrive<br/>sharing defaults]
    A --> E[Audit / eDiscovery ready]
    F[GitHub Actions<br/>(OIDC)] --> A
    F --> E
    E --> G[Evidence in customer tenant]

4) Google Workspace HIPAA Baseline
https://github.com/fedlinllc/fedlin-gws-hipaa-baseline
flowchart LR
    A[Google Workspace Tenant] --> B[Admin / Role Hygiene]
    A --> C[Sharing / Drive Controls<br/>(PHI-aware)]
    A --> D[Security / 2SV Settings]
    A --> E[Audit / Reports]
    E --> F[Customer Evidence Folder]
    G[GitHub Actions<br/>(OIDC-capable)] --> A

5) DMARC / SPF / DKIM
https://github.com/fedlinllc/fedlin-dmarc-spf-dkim
flowchart LR
    A[Discover sending domains] --> B[SPF for M365/GWS]
    A --> C[Enable DKIM]
    A --> D[Create DMARC<br/>with reporting]
    B --> E[Customer DNS Zone]
    C --> E
    D --> E
    F[GitHub Actions DNS check<br/>(OIDC)] --> E


How we engage (business / C2C)

C2C / 1099 friendly. Independent consultant model supported.

Subcontract-ready. Each repo has a defined scope so primes can see what’s delivered.

Customer-owned evidence. We do not insist on hosting your logs/exports — we show you where to put them.

Secure delivery. GitHub Actions with OIDC → no long-lived AWS/Microsoft credentials to rotate.

Contact

Website: https://www.fedlin.com
