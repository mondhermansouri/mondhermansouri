# Mondher Mansouri

**Senior Systems & Network Engineer | Cloud & DevOps Specialist | DevSecOps Advocate**

[![GitHub](https://img.shields.io/badge/GitHub-mondhermansouri-181717?style=flat&logo=github)](https://github.com/mondhermansouri)
[![Email](https://img.shields.io/badge/Email-mondher.mansouri%40outlook.com-0078D4?style=flat&logo=microsoftoutlook&logoColor=white)](mailto:mondher.mansouri@outlook.com)

---

## Professional Overview

With **8 years of continuous IT infrastructure experience (2018–2026)**, I specialize in bridging the gap between rigorous enterprise systems/network administration and modern Cloud/DevOps practices. My foundation is rooted in enterprise Windows Server and Linux environments, high-availability networking, virtualization, and systems security. Over the past several years, I have channeled this experience into designing, automating, and securing multi-cloud infrastructure (AWS, Azure, GCP) using Infrastructure as Code (Terraform), configuration management (Ansible), and security-first CI/CD automation (GitHub Actions).

My engineering philosophy emphasizes:
- **Zero-Secret Architectures:** Replacing static credentials with keyless federated identities (OIDC, Workload Identity Federation).
- **Defense-in-Depth:** Segmenting networks (3-tier architectures, least-privilege security groups, WAF/DDoS policies) and securing application configurations.
- **Reproducible Automation:** Treating all infrastructure, configuration, and security baselines as testable, version-controlled code.

---

## Technical Competencies

| Domain | Technologies & Methodologies |
|---|---|
| **Cloud Platforms** | **Amazon Web Services (AWS)**, **Microsoft Azure**, **Google Cloud Platform (GCP)** |
| **Infrastructure as Code (IaC)** | **Terraform** (Reusable Modules, Multi-Environment State, Workspaces, Native Testing), **HCL** |
| **Automation & Configuration** | **Ansible** (Roles, Playbooks, AWS SSM Transport, Dynamic Inventory), **Bash**, **PowerShell** |
| **CI/CD & DevSecOps** | **GitHub Actions** (Reusable Workflows, OIDC Keyless Auth, Matrix Strategies), **Docker** |
| **Systems & Virtualization** | **Linux** (Debian/Ubuntu, RHEL/CentOS), **Windows Server** (Active Directory, Group Policy, PowerShell), **Hyper-V / VMware** |
| **Networking & Traffic** | **TCP/IP**, VPC Design, Subnetting, Route Tables, NAT Gateways, ALB/App Gateway/Cloud LB, DNS, Reverse Proxies |
| **Security & Governance** | **IAM Least Privilege**, **WAF / Cloud Armor**, **KMS / Secrets Manager**, Secret Masking, REST API Security Testing (JWT/Bearer) |
| **Languages & Tooling** | **Python 3** (Automation, REST APIs, Pytest), **Git**, **GitHub CLI**, **TFLint**, **Trivy** |

---

## Featured Portfolio Projects

### 1. [AWS Cloud 3-Tier Infrastructure with Terraform & Ansible](https://github.com/mondhermansouri/aws-cloud-3tier-terraform-ansible)
> Enterprise-grade modular 3-tier high-availability infrastructure on AWS provisioned by Terraform, configured via Ansible over AWS Systems Manager (SSM), and deployed through GitHub Actions.

- **Key Highlights:**
  - Complete 3-tier topology: Public Subnets (ALB, NAT), Private App Subnets (EC2 Auto Scaling Group), and Isolated Data Subnets (RDS MySQL Multi-AZ, ElastiCache Redis).
  - Secure configuration management using Ansible over AWS Systems Manager (SSM) transport—zero open SSH ports (port 22 closed).
  - Keyless GitHub Actions CI/CD leveraging AWS IAM OIDC federation (no static access keys stored in GitHub).
  - Modular structure across isolated `dev`, `staging`, and `prod` environments.
- **Architecture Diagram & Code:** [View Repository](https://github.com/mondhermansouri/aws-cloud-3tier-terraform-ansible)
- **Status:** `Automated CI Matrix Validation: Passed` | *Dry-run & syntax validated offline; live deployment gated by cloud secrets.*

---

### 2. [Azure Cloud 3-Tier Infrastructure with Terraform & Native Testing](https://github.com/mondhermansouri/azure-cloud-3tier-terraform)
> Highly available multi-environment Microsoft Azure architecture built with modular Terraform, automated mocked unit tests (`*.tftest.hcl`), and cascaded GitHub Actions deployment pipelines.

- **Key Highlights:**
  - 3-tier architecture: Azure Front Door / Application Gateway, Linux App Service / VMSS, Azure SQL Serverless with failover, and Private Endpoints.
  - Native Terraform testing framework (`*.tftest.hcl`) running mocked provider tests directly in CI without requiring cloud credentials.
  - Cascading multi-stage delivery pipeline (`Dev -> Test -> Prod`) utilizing GitHub Actions reusable workflows and environment approval gates.
  - DevSecOps static analysis integrating TFLint and Trivy IaC security vulnerability scanning.
- **Architecture Diagram & Code:** [View Repository](https://github.com/mondhermansouri/azure-cloud-3tier-terraform)
- **Status:** `Mocked Unit Tests: Passed` | *Validated offline in CI; live deployment gated by cloud credentials.*

---

### 3. [GCP Cloud 3-Tier Architecture with Workload Identity Federation](https://github.com/mondhermansouri/gcp-cloud-3tier-terraform)
> Modular, highly available 3-tier infrastructure on Google Cloud Platform featuring Workload Identity Federation (WIF) keyless authentication and multi-environment orchestration.

- **Key Highlights:**
  - 3-tier cloud design: Cloud Load Balancing (HTTPS), Cloud Armor WAF/DDoS security policies, Regional Managed Instance Groups (MIG) with autoscaling, Cloud SQL HA with read replica, and Cloud Storage lifecycle rules.
  - Keyless CI/CD authentication via GCP Workload Identity Federation (WIF) and dedicated deployment service accounts (zero long-lived JSON service account keys).
  - Dynamic change detection using paths filtering to evaluate and validate only affected environments (`dev`, `staging`, `prod`).
  - Centralized observability stack with Cloud Monitoring alert policies, log sinks, and uptime checks.
- **Architecture Diagram & Code:** [View Repository](https://github.com/mondhermansouri/gcp-cloud-3tier-terraform)
- **Status:** `Automated Paths-Filter CI: Passed` | *Validated offline in CI; live deployment gated by WIF provider variables.*

---

### 4. [REST API Security Audit Tool (Python / DevSecOps)](https://github.com/mondhermansouri/api-security-audit-tool)
> Automated baseline security testing utility for RESTful APIs implementing token-based authentication (JWT / Bearer tokens).

- **Key Highlights:**
  - Automated security checks evaluating missing authentication, expired/malformed tokens, unauthorized role escalations, and HTTP error handling.
  - Security-first engineering: zero-secret architecture, token masking in all logging outputs, sanitized error propagation, and defensive timeout controls.
  - 100% automated test coverage of authentication states with mocked HTTP responses (`pytest`).
  - Hardened GitHub Actions CI with least-privilege token permissions (`contents: read`).
- **Code & Test Suite:** [View Repository](https://github.com/mondhermansouri/api-security-audit-tool)
- **Status:** `Automated Test Suite: 10/10 Passed (Green)`

---

## Architectural & Deployment Disclaimer

The infrastructure repositories featured above represent production-grade architectural patterns and Infrastructure as Code implementations designed to demonstrate enterprise Cloud, DevOps, and DevSecOps competencies. To maintain environmental cost control and prevent unauthorized cloud spend, all CI/CD workflows are engineered with safety guards that validate formatting, syntax, module structure, and unit tests offline, while gating live cloud deployments behind explicit cloud provider authentication secrets.

---

## Contact & Connect

- **GitHub:** [@mondhermansouri](https://github.com/mondhermansouri)
- **Email:** [mondher.mansouri@outlook.com](mailto:mondher.mansouri@outlook.com)
- **Location & Relocation:** Open to international remote and on-site Cloud / DevOps / Infrastructure roles.
