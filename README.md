<!-- Profile README for github.com/fedlinllc -->

<h1 align="center">FEDLIN</h1>
<p align="center"><em>Security Solutions Architecture.</em></p>

### Skills
`Discovery & Requirements (stakeholder interviews, constraints, SLAs)` ·
`Solution Architecture (reference designs, integration patterns, data flows)` ·
`Identity & Access (OIDC/SSO, IAM/RBAC/ABAC, least privilege)` ·
`Security & Governance (SCC Standard, Guardrails, Policy-as-Code, secrets hygiene)` ·
`Landing Zones & Baselines (Workspace hardening, org policies, account structure)` ·
`API & App Patterns (HTTP v2, async events, zero-trust edges, rate limiting)` ·
`Delivery (IaC: Terraform/Bicep, GitHub Actions via OIDC, reviews & change mgmt)` ·
`Reliability & Ops (observability, runbooks, error budgets, incident basics)` ·
`Compliance Enablement (evidence automation, audit trails, DR/BCP touchpoints)`


### Tech
![Solution Architecture](https://img.shields.io/badge/Role-Solution_Architecture-334155)
![OIDC / SSO](https://img.shields.io/badge/Auth-OIDC%20%2F%20SSO-0F766E)
![SCC Standard](https://img.shields.io/badge/Security-SCC%20(Standard)-334155)
![Email Auth: SPF · DKIM · DMARC](https://img.shields.io/badge/DNS-Email%20Auth%3A%20SPF%20%C2%B7%20DKIM%20%C2%B7%20DMARC-334155)
![AWS](https://img.shields.io/badge/Cloud-AWS-232F3E?logo=amazon-aws&logoColor=white)
![Azure](https://img.shields.io/badge/Cloud-Azure-0078D4?logo=microsoft-azure&logoColor=white)
![Google Cloud](https://img.shields.io/badge/Cloud-Google%20Cloud-4285F4?logo=googlecloud&logoColor=white)
![Google Workspace Admin](https://img.shields.io/badge/Google-Workspace%20Admin-4285F4?logo=google&logoColor=white)
![Terraform](https://img.shields.io/badge/IaC-Terraform-7B42BC?logo=terraform&logoColor=white)
![Bicep](https://img.shields.io/badge/IaC-Bicep-0A84FF)
![GitHub Actions (OIDC)](https://img.shields.io/badge/CI%2FCD-GitHub_Actions_(OIDC)-2088FF?logo=githubactions&logoColor=white)
![Gitleaks](https://img.shields.io/badge/SecOps-Gitleaks-334155)
![Dependabot](https://img.shields.io/badge/Supply_Chain-Dependabot-334155)
![Vercel](https://img.shields.io/badge/Web-Vercel-111827?logo=vercel&logoColor=white)
![Astro](https://img.shields.io/badge/Web-Astro-0F172A)


---

### Stack
`Identity & Access (OIDC/SSO: Entra ID, IAM Identity Center)` · `IAM / RBAC / ABAC` ·  
`AWS (API Gateway, Lambda, S3, CloudFront, WAF)` · `Azure (ARM, APIM, Storage)` ·  
`IaC (Terraform, Bicep)` · `Policy-as-code (AWS SCP/IAM, Azure Policy)` ·  
`CI/CD (GitHub Actions, OIDC federation)` ·  
`Observability (CloudWatch/CloudTrail, Log Analytics, Sentinel)` ·  
`Compliance automation (AWS Config, Security Hub, evidence workflows)` ·  
`Networking & App Security (TLS, CORS, rate limiting)` ·  
`Serverless & APIs (HTTP v2, event patterns)` ·  
`Linux (Fedora/Ubuntu/Debian)` · `Vercel` · `Astro`

---

## Featured — Azure

**Project 0 — Secure CI/CD Baseline**  
<sub>Provision + verify Azure infra with OIDC-only pipelines and machine-readable outputs for downstream labs.</sub>  
[![Deploy: main](https://github.com/fedlinllc/fedlin-azure-secure-cicd/actions/workflows/deploy-azure.yml/badge.svg?branch=main)](https://github.com/fedlinllc/fedlin-azure-secure-cicd/actions/workflows/deploy-azure.yml)

**Project 1 — Sentinel Vulnerability & Compliance Lab**  
<sub>Wire Microsoft Sentinel to LAW, enable data connectors, seed analytics, and ship evidence via GitHub Actions (OIDC only).</sub>  
[![Sentinel Lab: main](https://github.com/fedlinllc/fedlin-azure-cis-vulnerability-lab/actions/workflows/azure-sentinel-vulncomp-lab.yml/badge.svg?branch=main)](https://github.com/fedlinllc/fedlin-azure-cis-vulnerability-lab/actions/workflows/azure-sentinel-vulncomp-lab.yml)

---

### Flow (Azure)
```mermaid
flowchart LR
  P0[Project 0\nSecure CI/CD] -->|outputs.json| LAW[(Log Analytics Workspace)]
  LAW --> Sentinel[Microsoft Sentinel]
  Sentinel --> Rules[Analytics Rules]
  Sentinel --> Connectors[Defender & Activity Connectors]
  Sentinel --> Evidence[Artifacts & Screenshots]
```
---

### Roadmap
- [x] Project 0: Secure CI/CD Baseline  
- [x] Project 1: Sentinel Vulnerability & Compliance Lab  
- [ ] Project 2: Hardening & Remediation (Defender assessments → Ansible → re-assessment)

---

## Featured — AWS

<a href="https://github.com/fedlinllc/fedlin-vercel-aws-baseline"><b>Vercel × AWS Baseline for Regulated Apps</b></a>  
<sub>Astro on Vercel in front, API Gateway/Lambda in back — SSO-operated, CORS-locked, and compliance-ready via an optional evidence add-on.</sub>

[![Demo](https://img.shields.io/badge/demo-live-0F766E)](https://fedlin-vercel-aws-baseline.vercel.app)
[![Showcase](https://img.shields.io/badge/release-v0.1.0-334155)](https://github.com/fedlinllc/fedlin-vercel-aws-baseline/releases/tag/v0.1.0-showcase)
[![Repo](https://img.shields.io/badge/repo-open-111827)](https://github.com/fedlinllc/fedlin-vercel-aws-baseline)
[![CI](https://github.com/fedlinllc/fedlin-vercel-aws-baseline/actions/workflows/ci.yml/badge.svg)](https://github.com/fedlinllc/fedlin-vercel-aws-baseline/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/fedlinllc/fedlin-vercel-aws-baseline/blob/main/LICENSE)

### Flow (AWS)
```mermaid
flowchart LR
  FE["Vercel (Astro)"] --> APIGW["API Gateway (HTTP v2)"]
  APIGW --> LBD["Lambda /health"]
  LBD --> S3["S3 (evidence artifacts)"]

  subgraph Controls
    SSO["SSO (IAM Identity Center)"]
    CORS["CORS (prod origin only)"]
  end

  SSO -. operations .-> APIGW
  CORS -. enforcement .-> APIGW
```
---

## Featured — GCP

<a href="https://github.com/fedlinllc/fedlin-gws-hipaa-baseline"><b>HIPAA Readiness for Google Workspace + GCP </b></a>  
<sub>Fixed-scope deployment to bring Google Workspace under HIPAA-aligned controls — <b>SCC (Standard) at org scope</b> with guardrails across <b>Admin roles, Groups, Drive/Sharing, external access defaults</b> — plus a documented readiness summary. (No public screenshots/how-tos; evidence stays in tenant.)</sub>

[![Showcase](https://img.shields.io/badge/release-v0.1.0-334155)](https://github.com/fedlinllc/fedlin-gcp-hipaa-showcase/releases/tag/v0.1.0)
[![Repo](https://img.shields.io/badge/repo-open-111827)](https://github.com/fedlinllc/fedlin-gcp-hipaa-showcase)
[![License: MIT](https://img.shields.io/badge/License-MIT-lightgrey)](https://github.com/fedlinllc/fedlin-gws-hipaa-baseline/blob/main/LICENSE)
[![Book](https://img.shields.io/badge/book-call-0F766E)](https://www.fedlin.com/bookings)
<!-- If/when you add a CI workflow in the showcase repo, you can also show it:
[![CI](https://github.com/fedlinllc/fedlin-gcp-hipaa-showcase/actions/workflows/ci.yml/badge.svg)](https://github.com/fedlinllc/fedlin-gcp-hipaa-showcase/actions/workflows/ci.yml)
-->

### Flow (GCP + Workspace)
```mermaid
flowchart LR
  Buyer["Owner / Practice Manager"] --> Intake["Intake & Access<br/>(Temp Super Admin or screenshare)"]

  subgraph Workspace["Google Workspace"]
    Admin["Admin Roles<br/>Hygiene"]
    Groups["Groups<br/>(Access Patterns)"]
    Sharing["Drive / Sharing<br/>Defaults"]
    External["External Access<br/>Defaults"]
    GuardrailsW["Applied Guardrails<br/>(Workspace)"]
    Admin --> GuardrailsW
    Groups --> GuardrailsW
    Sharing --> GuardrailsW
    External --> GuardrailsW
  end

  subgraph GCP["Google Cloud (Initial Guardrails)"]
    OrgPolicies["Org Policies<br/>(High Level)"]
    ProjGuard["Project Guardrails"]
    SCC["Security Command Center<br/>(Standard, Org Scope)"]
    OrgPolicies --> ProjGuard
    OrgPolicies --> SCC
    ProjGuard --> SCC
  end

  Intake --> Admin
  GuardrailsW --> Handoff["Readiness Summary<br/>(Exec 1-pager + Operator checklist)"]
  SCC --> Monitor["Org-Scoped Monitoring<br/>& Findings"]
```
