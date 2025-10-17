<!-- Profile README for github.com/fedlinllc -->

<h1 align="center">FEDLIN — Public Portfolio</h1>
<p align="center"><em>Security Engineering Labs.</em></p>

---

### Featured

**Project 0 — Secure CI/CD Baseline**  
<sub>Provision + verify Azure infra with OIDC-only pipelines and machine-readable outputs for downstream labs.</sub>  
[![Deploy: main](https://github.com/fedlinllc/fedlin-azure-secure-cicd/actions/workflows/deploy-azure.yml/badge.svg?branch=main)](https://github.com/fedlinllc/fedlin-azure-secure-cicd/actions/workflows/deploy-azure.yml)  
[Run Project 0](https://github.com/fedlinllc/fedlin-azure-secure-cicd/actions/workflows/deploy-azure.yml) · [README](https://github.com/fedlinllc/fedlin-azure-secure-cicd#readme)

**Project 1 — Sentinel Vulnerability & Compliance Lab**  
<sub>Wire Microsoft Sentinel to LAW, enable data connectors, seed analytics, and ship evidence via GitHub Actions (OIDC only).</sub>  
[![Sentinel Lab: main](https://github.com/fedlinllc/fedlin-azure-cis-vulnerability-lab/actions/workflows/azure-sentinel-vulncomp-lab.yml/badge.svg?branch=main)](https://github.com/fedlinllc/fedlin-azure-cis-vulnerability-lab/actions/workflows/azure-sentinel-vulncomp-lab.yml)  
[Run Project 1](https://github.com/fedlinllc/fedlin-azure-cis-vulnerability-lab/actions/workflows/azure-sentinel-vulncomp-lab.yml) · [README](https://github.com/fedlinllc/fedlin-azure-cis-vulnerability-lab#readme)  
📸 Evidence: [Screenshots](https://github.com/fedlinllc/fedlin-azure-cis-vulnerability-lab/tree/main/docs/evidence) · [Artifacts](https://github.com/fedlinllc/fedlin-azure-cis-vulnerability-lab/actions)

---

### Tech
![Azure](https://img.shields.io/badge/Cloud-Azure-informational?logo=microsoft-azure&logoColor=white)
![Sentinel](https://img.shields.io/badge/SIEM-Sentinel-informational)
![KQL](https://img.shields.io/badge/Query-KQL-informational)
![GitHub Actions](https://img.shields.io/badge/CI-GitHub_Actions-informational?logo=githubactions&logoColor=white)
![OIDC](https://img.shields.io/badge/Auth-OIDC-informational)
![License: MIT](https://img.shields.io/badge/License-MIT-success)

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

### Stack
`Linux (Ubuntu, Debian)` · `Cloud platforms` · `CI/CD` · `OIDC / identity federation` · `Policy-as-code` · `IaC` · `Observability / logging` · `Detection engineering`

---
