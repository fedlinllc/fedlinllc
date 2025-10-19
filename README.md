<!-- Profile README for github.com/fedlinllc -->

<h1 align="center">FEDLIN — Public Portfolio</h1>
<p align="center"><em>Security Solutions Architecture.</em></p>

### Tech
![OIDC / SSO](https://img.shields.io/badge/Auth-OIDC%20%2F%20SSO-0F766E)
![Azure](https://img.shields.io/badge/Cloud-Azure-0078D4?logo=microsoft-azure&logoColor=white)
![AWS](https://img.shields.io/badge/Cloud-AWS-232F3E?logo=amazon-aws&logoColor=white)
![Terraform](https://img.shields.io/badge/IaC-Terraform-7B42BC?logo=terraform&logoColor=white)
![Bicep](https://img.shields.io/badge/IaC-Bicep-0A84FF)
![GitHub Actions](https://img.shields.io/badge/CI%2FCD-GitHub_Actions-2088FF?logo=githubactions&logoColor=white)
![Sentinel](https://img.shields.io/badge/SIEM-Sentinel-4B5563)
![CloudWatch](https://img.shields.io/badge/Observability-CloudWatch-4B5563)
![API Gateway](https://img.shields.io/badge/Serverless-API_Gateway-111827)
![Lambda](https://img.shields.io/badge/Serverless-Lambda-F90?logo=awslambda&logoColor=white)
![Vercel](https://img.shields.io/badge/Web-Vercel-111827?logo=vercel&logoColor=white)
![Astro](https://img.shields.io/badge/Web-Astro-0F172A)
![License: MIT](https://img.shields.io/badge/License-MIT-success)

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
`Linux (Ubuntu/Debian)` · `Vercel` · `Astro`

---


### Featured - Azure

**Project 0 — Secure CI/CD Baseline**  
<sub>Provision + verify Azure infra with OIDC-only pipelines and machine-readable outputs for downstream labs.</sub>  
[![Deploy: main](https://github.com/fedlinllc/fedlin-azure-secure-cicd/actions/workflows/deploy-azure.yml/badge.svg?branch=main)](https://github.com/fedlinllc/fedlin-azure-secure-cicd/actions/workflows/deploy-azure.yml)  

**Project 1 — Sentinel Vulnerability & Compliance Lab**  
<sub>Wire Microsoft Sentinel to LAW, enable data connectors, seed analytics, and ship evidence via GitHub Actions (OIDC only).</sub>  
[![Sentinel Lab: main](https://github.com/fedlinllc/fedlin-azure-cis-vulnerability-lab/actions/workflows/azure-sentinel-vulncomp-lab.yml/badge.svg?branch=main)](https://github.com/fedlinllc/fedlin-azure-cis-vulnerability-lab/actions/workflows/azure-sentinel-vulncomp-lab.yml)  


---

### Flow
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

### AWS Flow (high-level)
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

