<div align="center">

# Ramya Keerthi Kondisetty

### DevOps Engineer · Site Reliability Engineer · Platform Engineer

**I build the infrastructure other engineers build on.**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ramyakeerthikondisetty)
[![Email](https://img.shields.io/badge/Email-Get%20in%20touch-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ramyakeerthikondisetty@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-keerthikondisetty-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/keerthikondisetty)

</div>

---

## 👋 About me

I work at the layer where infrastructure becomes a product — multi-account AWS landing zones, GitOps-managed Kubernetes, internal developer platforms, and the supply-chain and observability controls that make all of it safe to operate.

My approach is platform engineering with an SRE mindset:

- **Infrastructure as code with policy gates**, not tribal knowledge. If it isn't in Git with a review and an automated policy check, it isn't the platform.
- **Self-service golden paths**, not ticket queues. A developer should get a governed, observable, deployed service from one form — not from a week of waiting on three teams.
- **SLOs and error budgets**, not uptime claims. Reliability is a number you measure and spend, not an adjective.
- **Real code, not just YAML.** Drift detectors, rightsizing engines, cost analysers, incident tooling — written in Python and Bash, tested, and packaged.

Everything in my portfolio below is built as **one platform in layers**, where each repo consumes the ones before it — because that's how real platform teams work, and it's the part a list of unrelated tutorial repos can never show.

---

## 🛠️ What I work with

**Cloud & Infrastructure as Code**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)
![OpenTofu](https://img.shields.io/badge/OpenTofu-FFDA18?style=for-the-badge&logo=opentofu&logoColor=black)
![Packer](https://img.shields.io/badge/Packer-02A8EF?style=for-the-badge&logo=packer&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=for-the-badge&logo=ansible&logoColor=white)

**CI/CD & Build**

![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab%20CI-FC6D26?style=for-the-badge&logo=gitlab&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Argo CD](https://img.shields.io/badge/Argo%20CD-EF7B4D?style=for-the-badge&logo=argo&logoColor=white)
![Argo Rollouts](https://img.shields.io/badge/Argo%20Rollouts-EF7B4D?style=for-the-badge&logo=argo&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)
![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?style=for-the-badge&logo=sonarqubeserver&logoColor=white)
![Nexus](https://img.shields.io/badge/Nexus%20%2F%20Artifactory-41BF47?style=for-the-badge&logo=jfrog&logoColor=white)
![Renovate](https://img.shields.io/badge/Renovate-1A1F6C?style=for-the-badge&logo=renovate&logoColor=white)
![Make](https://img.shields.io/badge/Make-427819?style=for-the-badge&logo=gnu&logoColor=white)

> Pipelines I build are **OIDC-federated with no static credentials**, gated on policy-as-code rather than review-by-vibes, and deliver progressively — canaries promoted or rolled back automatically on live SLIs, never on a stopwatch.

**Containers, Kubernetes & Packaging**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Amazon EKS](https://img.shields.io/badge/Amazon%20EKS-FF9900?style=for-the-badge&logo=kubernetes&logoColor=white)
![OpenShift](https://img.shields.io/badge/OpenShift-EE0000?style=for-the-badge&logo=redhatopenshift&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=for-the-badge&logo=helm&logoColor=white)
![Kustomize](https://img.shields.io/badge/Kustomize-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Karpenter](https://img.shields.io/badge/Karpenter-FF9900?style=for-the-badge&logoColor=white)
![Crossplane](https://img.shields.io/badge/Crossplane-172231?style=for-the-badge&logoColor=white)
![Cilium](https://img.shields.io/badge/Cilium%20%2F%20eBPF-F8C517?style=for-the-badge&logo=cilium&logoColor=black)
![Backstage](https://img.shields.io/badge/Backstage-9BF0E1?style=for-the-badge&logo=backstage&logoColor=black)

**Secrets Management**

![Vault](https://img.shields.io/badge/HashiCorp%20Vault-FFEC6E?style=for-the-badge&logo=vault&logoColor=black)
![AWS Secrets Manager](https://img.shields.io/badge/AWS%20Secrets%20Manager-DD344C?style=for-the-badge&logoColor=white)
![External Secrets](https://img.shields.io/badge/External%20Secrets%20Operator-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![SOPS](https://img.shields.io/badge/SOPS%20%2F%20age-4B32C3?style=for-the-badge&logo=gnuprivacyguard&logoColor=white)

> No secret is ever committed, baked into an image, or pasted into a CI variable. Workloads pull at runtime from Vault or AWS Secrets Manager; pipelines authenticate by short-lived OIDC identity, not stored keys.

**Security & Supply Chain**

![Sigstore](https://img.shields.io/badge/Sigstore%20%2F%20cosign-003399?style=for-the-badge&logoColor=white)
![Kyverno](https://img.shields.io/badge/Kyverno-2E8555?style=for-the-badge&logo=kubernetes&logoColor=white)
![OPA](https://img.shields.io/badge/OPA%20%2F%20Conftest-7D9199?style=for-the-badge&logoColor=white)
![Trivy](https://img.shields.io/badge/Trivy%20%2F%20Grype-1904DA?style=for-the-badge&logo=trivy&logoColor=white)
![Checkov](https://img.shields.io/badge/Checkov%20%2F%20tfsec-6D4AFF?style=for-the-badge&logoColor=white)
![Syft](https://img.shields.io/badge/Syft%20SBOM-2C3E50?style=for-the-badge&logoColor=white)
![gitleaks](https://img.shields.io/badge/gitleaks-C0392B?style=for-the-badge&logo=git&logoColor=white)

**Observability & Reliability**

![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-425CC7?style=for-the-badge&logo=opentelemetry&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Loki](https://img.shields.io/badge/Loki-F5A800?style=for-the-badge&logo=grafana&logoColor=black)
![Tempo](https://img.shields.io/badge/Tempo-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![ELK](https://img.shields.io/badge/ELK%20Stack-005571?style=for-the-badge&logo=elasticstack&logoColor=white)
![CloudWatch](https://img.shields.io/badge/CloudWatch-FF4F8B?style=for-the-badge&logoColor=white)
![PagerDuty](https://img.shields.io/badge/PagerDuty-06AC38?style=for-the-badge&logo=pagerduty&logoColor=white)

**Process & Collaboration**

![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white)
![Confluence](https://img.shields.io/badge/Confluence-172B4D?style=for-the-badge&logo=confluence&logoColor=white)
![Slack](https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white)

> Change management done properly: every production change traceable from Jira ticket → pull request → pipeline run → deployed revision, with approvals and rollback recorded rather than remembered.

**Languages & Systems**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![YAML](https://img.shields.io/badge/YAML-CB171E?style=for-the-badge&logo=yaml&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

---

## 🚀 Platform portfolio

<div align="center">

[![aws-platform-foundation](https://github-readme-stats.vercel.app/api/pin/?username=keerthikondisetty&repo=aws-platform-foundation&theme=transparent&hide_border=false&border_radius=8)](https://github.com/keerthikondisetty/aws-platform-foundation)
[![eks-gitops-platform](https://github-readme-stats.vercel.app/api/pin/?username=keerthikondisetty&repo=eks-gitops-platform&theme=transparent&hide_border=false&border_radius=8)](https://github.com/keerthikondisetty/eks-gitops-platform)
[![idp-golden-paths](https://github-readme-stats.vercel.app/api/pin/?username=keerthikondisetty&repo=idp-golden-paths&theme=transparent&hide_border=false&border_radius=8)](https://github.com/keerthikondisetty/idp-golden-paths)

</div>

### 🏗️ [aws-platform-foundation](https://github.com/keerthikondisetty/aws-platform-foundation) — the ground floor

A multi-account AWS landing zone in OpenTofu. AWS Organizations with OU structure, Service Control Policies for region lockdown and mandatory encryption, IAM Identity Center with zero IAM users, centralized CloudTrail/Config/GuardDuty, and a Transit Gateway hub. CI runs on **OIDC federation — no long-lived AWS keys anywhere** — with Checkov/tfsec/OPA gating every plan, and a Python Lambda detecting state drift on a schedule.

### ☸️ [eks-gitops-platform](https://github.com/keerthikondisetty/eks-gitops-platform) — the substrate

Production-shaped EKS where the entire cluster state is one Git repo. Karpenter spot-first compute with consolidation, Cilium in eBPF mode replacing kube-proxy, Argo CD app-of-apps, Gateway API, Kyverno admission policy, and Argo Rollouts canaries **promoted or auto-rolled-back on live Prometheus SLIs** rather than on a timer.

### 🧩 [idp-golden-paths](https://github.com/keerthikondisetty/idp-golden-paths) — self-service

An internal developer platform: Backstage software templates that scaffold a repo, wire CI, create the Argo CD Application and open the PR from one form; Crossplane compositions exposing `PostgresInstance`, `ObjectStore` and `Queue` as Kubernetes CRDs with encryption, backup and tagging baked in; and a weighted scorecard grading every service on ownership, SLOs, runbooks, image signing and CVEs.

### 🔐 secure-supply-chain — *in progress*

SLSA provenance, Sigstore keyless signing via GitHub OIDC, SPDX/CycloneDX SBOMs as OCI attestations, and Kyverno `verifyImages` rejecting any unsigned or unattested image at admission.

---

## 🧭 What's next

The platform continues in layers — an **OpenTelemetry observability stack** with SLOs as code and tail-based sampling, a **chaos and DR lab** with measured RTO/RPO, an **agentic AI SRE assistant** that triages alerts and proposes remediation as reviewable pull requests, a **FinOps control loop** that auto-opens rightsizing PRs, and a **DORA delivery-metrics** capstone measuring the whole thing.

---

## 💭 How I think about this work

> **Measured beats impressive.** I'd rather publish *"0 failed requests across 12 node rotations under 500 RPS sustained load"* than an uptime figure nobody can verify.

> **Trade-offs belong in the README.** Every repo documents what I chose, what I gave up, and what I'd do differently. That section is usually more useful than the code.

> **Nothing gets applied by hand.** If it isn't in Git with a review and a policy gate, it isn't the platform.

---

<div align="center">

### 📫 Let's talk

Open to conversations about platform engineering, SRE and cloud infrastructure roles.

[![LinkedIn](https://img.shields.io/badge/linkedin.com%2Fin%2Framyakeerthikondisetty-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ramyakeerthikondisetty)
[![Email](https://img.shields.io/badge/ramyakeerthikondisetty%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ramyakeerthikondisetty@gmail.com)

</div>
