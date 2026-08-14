# Emmanuel Onen
### Senior Systems Engineer | Infrastructure Architect | Cloud Engineer

📍 George Town, Cayman Islands (EST — UTC-5)
🔗 [LinkedIn](https://linkedin.com/in/emmanuelonen) | 📧 eonenit@gmail.com

---

## About Me

Cloud Infrastructure Architect with 15+ years delivering enterprise hybrid and multicloud platforms across financial services, aviation, government, and highly regulated environments. Currently targeting Senior Cloud Engineer, Infrastructure Architect, and DevOps roles across local and remote markets (Cayman Islands, US, UK, Canada).

Specializing in hybrid cloud integration (Azure & AWS), Nutanix HCI, VMware, HPE enterprise storage, Veeam DR, and automated Infrastructure as Code (IaC) workflows.

---

## Core Tech Stack

* **Cloud & Infrastructure:** Microsoft Azure · Enterprise Networking (Hub-Spoke, VPN, Private Endpoints) · Hybrid Cloud
* **Infrastructure as Code (IaC):** Terraform (HCL) · Azure Bicep · Remote State Architecture · Drift Remediation
* **Identity & Security:** Entra ID (Azure AD) · RBAC · Conditional Access · Least-Privilege IAM · Active Directory / GPO
* **Observability & Scripting:** Azure Monitor · Log Analytics (KQL) · PowerShell · Bash · Azure CLI
* **Virtualization & Storage:** Nutanix HCI · VMware vSphere · HPE Enterprise Storage (Synergy, Alletra, 3PAR) · Veeam DR

---

## Enterprise Azure Cloud Engineering Portfolio (2026)

*A structured 5-lab engineering series building, securing, observing, and codifying a production landing zone for Global Logistics & Enterprise Services.*

| Lab | Architectural Focus | Key Technologies | Status |
| :--- | :--- | :--- | :--- |
| [Lab 1 — Active Directory](https://github.com/emmanuelonen/lab1-active-directory) | Hybrid Identity Foundation | Windows Server 2025 · DC Promotion · OUs · GPOs · Identity | ✅ Complete |
| [Lab 2 — Azure Networking](https://github.com/emmanuelonen/lab2-azure-networking) | Enterprise Network Topology | Hub-Spoke VNets · NSGs · Private Endpoints · Private DNS | ✅ Complete |
| [Lab 3 — Azure Identity](https://github.com/emmanuelonen/lab3-azure-identity-governance) | Zero Trust & Access Governance | Entra ID · RBAC · Managed Identities · Conditional Access | ✅ Complete |
| [Lab 4 — KQL & Azure Monitor](https://github.com/emmanuelonen/Lab4-Azure-Monitor-Observability) | Enterprise Observability | Log Analytics · KQL Queries · Workbooks · Alert Rules | ✅ Complete |
| [Lab 5 — Terraform & Bicep on Azure](https://github.com/emmanuelonen/Lab-05-IaC-Terraform-Bicep) | Declarative IaC Automation | Declarative HCL · Remote State Locking · Drift Detection · Bicep | ✅ Complete |
| [Lab 6 — M365 Security & Governance](https://github.com/emmanuelonen/Lab6-M365-Identity-Security) | Identity-Driven Security & Compliance | Graph SDK v2.x · Exchange Online · Purview DLP · PowerShell 7 | ✅ Complete |
| Lab 7 — SharePoint Permissions & Compliance | Enterprise Permissions & Governance | SharePoint Online · Information Barriers · Sensitivity Labels · PowerShell | ⏳ Scheduled |
| Lab 8 — Kubernetes & Containers on Azure | Container Orchestration & Scaling | Azure Kubernetes Service (AKS) · ACR · Docker · HPA · Helm | ⏳ Scheduled |
| Lab 9 — Microsoft Sentinel AI Threat Detection | Automated SIEM/SOAR Incident Response | Microsoft Sentinel · KQL Analytics Rules · Logic Apps Playbooks · Defender | ⏳ Scheduled |
| Lab 10 — Conditional Access as Code (CaC) | DevSecOps & Pipeline-Driven IAM | GitHub Actions · Graph API · az rest · JSON Baselines · CI/CD | ⏳ Scheduled |

---
### ⏳ Scheduled Labs (Roadmap)

#### 📁 Lab 7 — SharePoint: Enterprise Permissions Architecture & Information Barriers
* **The Real Business Problem:** A Finance document containing salary data is accidentally shared with the entire company because someone clicked "Share with Everyone" on the wrong folder. HR and Legal can see each other's confidential matter files. There is no structure — just one flat SharePoint with broken inheritance and no governance.
* **What You Build & Solve:** Design a SharePoint site collection architecture for three departments (Finance, HR, Legal) with unique permission inheritance broken at site level, sensitivity labels applied at library level that prevent external sharing of confidential content, and an information barrier policy that prevents Finance users from even seeing HR content in search results. Then run a permissions audit report in PowerShell that outputs every user, their access level and which sites they can reach — the exact report a governance team produces quarterly.
* **Why It Stands Out:** SharePoint permissions debt is one of the most common and most painful problems in enterprise IT. The information barrier element is specifically relevant to financial services — banks and investment firms are legally required to separate research teams from trading desks using exactly this mechanism. That connection to regulated industry compliance will resonate immediately with any hiring manager in that space.
* **Certification Alignment:** SC-400 · MS-102

---

#### ☸️ Lab 8 — Kubernetes & Containers on Azure (AKS)
* **The Real Business Problem:** A development team deploys a containerised application directly on a VM. It works once. The second deployment breaks the first. Scaling requires manual VM duplication. There is no rollback. The ops team has no visibility. Every enterprise running microservices or modern applications hits this wall.
* **What You Build & Solve:** Deploy an Azure Kubernetes Service (AKS) cluster using Terraform from your Lab 5 remote state backend — IaC and containers in one workflow. Containerise a simple application using Docker, push the image to Azure Container Registry (ACR), deploy it to AKS, configure horizontal pod autoscaling, and connect the cluster logs to your Lab 4 Log Analytics Workspace. Then simulate a failed deployment and demonstrate a rollback using `kubectl rollout undo`.
* **Why It Stands Out:** This directly bridges Labs 2, 4 and 5 into the most in-demand skill in cloud engineering right now. The rollback demonstration is the interview moment — it proves you understand Kubernetes operationally, not just conceptually. AKS experience is listed in the majority of senior cloud engineering job descriptions in 2026.
* **Certification Alignment:** AZ-104 · AZ-400 · CKA (Certified Kubernetes Administrator)

---

#### 🛡️ Lab 9 — Microsoft Sentinel: AI-Driven Threat Detection & Automated Response
* **The Real Business Problem:** A company's security team receives 400 alerts per day. They investigate 40. The other 360 go unreviewed. An attacker dwells in the network for 23 days before detection — the industry average. The problem is not lack of data. It is lack of automated triage and response.
* **What You Build & Solve:** Deploy Microsoft Sentinel connected to your Lab 4 Log Analytics Workspace — so all your existing telemetry feeds directly in. Configure three analytics rules: a Scheduled rule detecting impossible travel sign-ins (same user, two countries, 30 minutes apart), a Microsoft Security rule ingesting Defender for Endpoint alerts, and a Fusion rule enabling AI-driven multi-signal attack correlation. Build a Playbook (Logic App) that automatically disables an Entra ID user account the moment Sentinel raises a high-severity identity alert — zero human intervention required. Then generate a test alert and watch the automation execute end to end.
* **Why It Stands Out:** Demonstrates the complete security operations loop — detect, triage, respond, contain — fully automated. The Playbook connecting Sentinel to Entra ID directly connects Lab 9 back to Lab 3. That cross-lab narrative is exactly what hiring managers look for in enterprise security. The impossible travel detection rule is also a real-world scenario question in senior interviews.
* **Certification Alignment:** SC-200 (Microsoft Security Operations Analyst) · AZ-500

---

#### 🔄 Lab 10 — Conditional Access as Code (CaC) with GitHub Actions CI/CD
* **The Real Business Problem:** A security engineer manually configures 12 Conditional Access policies across a production tenant. Six months later nobody knows which policies exist, what they do, who changed them, or whether they match the security baseline. An auditor asks for a policy changelog. There is none. This is the state of identity governance in most organisations.
* **What You Build & Solve:** Export your Lab 3 Conditional Access policies to JSON using the Microsoft Graph API. Store them in a GitHub repository as the single source of truth. Build a GitHub Actions workflow that on every pull request runs `az rest` to validate policy syntax, posts a `what-if` diff showing exactly what would change in the tenant, requires a reviewer approval, and on merge automatically deploys the updated policies via Graph API. Then simulate a policy drift — manually edit a policy in the portal — and demonstrate that the pipeline detects and remediates the drift on next run.
* **Why It Stands Out:** This is the intersection of three disciplines simultaneously: IAM, IaC, and DevSecOps. It represents the most mature tier in this portfolio and reflects what a Principal Cloud Engineer or DevSecOps Architect does daily. It closes the portfolio loop perfectly: Lab 1 built identity on-premises, Lab 3 built cloud identity manually, and Lab 10 puts that identity governance into a fully automated, version-controlled, peer-reviewed pipeline.
* **Certification Alignment:** AZ-400 (DevOps Solutions) · SC-300 (Identity & Access Administrator)

---

## Certifications & Technical Roadmap

**Active Certifications & Credentials:**
* Nutanix Certified Professional — Multicloud Infrastructure (NCP-MCI)
* Nutanix Certified Professional — Unified Storage (NCP-US)
* Veeam Data Platform Foundation v12
* CompTIA Linux+ | Network+ | A+
* ITIL v3 Foundation
* HPE Enterprise Infrastructure (ProLiant, Synergy, Alletra, 3PAR, SimpliVity)

**Azure, Security & DevOps Certification Roadmap:**
`AZ-900` (Fundamentals) ➔ `AZ-104` (Azure Administrator) ➔ `MS-102` / `SC-400` (M365 & Security Governance) ➔ `SC-200` (Security Operations Analyst) ➔ `CKA` (Certified Kubernetes Administrator) ➔ `AZ-400` (DevOps Engineer Expert)

---

*All portfolio projects feature full architecture diagrams, executable automation scripts, decision records, and production-grade verification proofs.*
