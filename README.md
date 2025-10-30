<h1 align="center">FEDLIN</h1> <p align="center"><b>Security Solutions Architecture · Vulnerability Management · Compliance Automation</b></p> <p align="center">C2C / 1099 · Subcontract-ready · Customer-tenant-first</p> <p align="center"> <img src="https://img.shields.io/badge/AWS-Security%20Baseline-blue" /> <img src="https://img.shields.io/badge/M365-Entra%20Hardening-blueviolet" /> <img src="https://img.shields.io/badge/GWS-HIPAA%20Baseline-green" /> <img src="https://img.shields.io/badge/GitHub%20Actions-OIDC%20Only-important" /> <img src="https://img.shields.io/badge/Compliance-SOC%202%20·%20ISO%2027001-lightgrey" /> </p>
About

FEDLIN is a security engineering and compliance automation consultancy. We design customer-tenant-first solutions — meaning evidence, logs, and configuration stay in your AWS / Microsoft 365 / Google Workspace environments — and we deliver them through GitHub Actions with OIDC so there are no long-lived secrets to manage.

What we deliver

AWS security baselines that map to SOC 2 / ISO 27001

A continuous monitoring layer on top of AWS baselines (VistaSec CMC)

Microsoft 365 / Entra identity-first hardening

Google Workspace hardening for HIPAA-adjacent/regulated use

Email security (DMARC / SPF / DKIM) for M365/GWS shops

All of it delivered via GitHub Actions (OIDC-only)

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
