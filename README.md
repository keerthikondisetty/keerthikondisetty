# Ramya Keerthi Kondisetty

**DevOps · Site Reliability · Platform Engineering**

I build the infrastructure other engineers build on — multi-account AWS landing zones, GitOps-managed Kubernetes, internal developer platforms, and the supply-chain and observability controls that make them safe to run.

My focus is platform work with an SRE mindset: infrastructure as code with policy gates rather than tribal knowledge, self-service golden paths rather than ticket queues, and SLOs and error budgets rather than uptime claims.

---

### What I work on

- **Cloud foundations** — AWS Organizations, SCPs, IAM Identity Center, Transit Gateway hub networking, OIDC-federated CI with zero static credentials
- **Kubernetes platforms** — EKS with Karpenter spot-first compute, Cilium eBPF networking, Argo CD app-of-apps, Gateway API, Kyverno admission policy, Argo Rollouts canaries gated on Prometheus SLIs
- **Developer platforms** — Backstage software templates and Crossplane infrastructure-as-CRDs, so a new service is one form instead of a multi-team ticket flow
- **Supply chain security** — SLSA provenance, Sigstore keyless signing, SPDX/CycloneDX SBOMs, enforced at admission
- **Reliability engineering** — OpenTelemetry, SLOs as code, multi-burn-rate alerting, chaos experiments and DR drills with measured RTO/RPO
- **Automation in real code** — Python and Bash tooling for day-2 operations: drift detection, rightsizing, cost analysis, incident context

### Tools I reach for

`AWS` · `Terraform / OpenTofu` · `Kubernetes (EKS)` · `Argo CD` · `Crossplane` · `Backstage`
`Karpenter` · `Cilium / eBPF` · `Kyverno` · `OpenTelemetry` · `Prometheus / Grafana`
`Python` · `Bash` · `Go` · `GitHub Actions` · `Docker` · `Sigstore / Syft / Trivy`

---

### Platform portfolio

These repos are built as one platform in layers — each consumes the ones before it, rather than standing alone.

| Repo | What it is |
|---|---|
| [aws-platform-foundation](https://github.com/keerthikondisetty/aws-platform-foundation) | Multi-account AWS landing zone in OpenTofu — Organizations, SCPs, immutable audit logging, transit gateway hub, OIDC-federated CI, Python drift detector |
| [eks-gitops-platform](https://github.com/keerthikondisetty/eks-gitops-platform) | Production-shaped EKS — Karpenter spot-first compute, Cilium eBPF networking, Argo CD app-of-apps, Kyverno enforcement, SLI-gated canary rollouts |
| [idp-golden-paths](https://github.com/keerthikondisetty/idp-golden-paths) | Internal developer platform — Backstage software templates, Crossplane infrastructure-as-CRDs, weighted service scorecard |
| `secure-supply-chain` | SLSA provenance, Sigstore keyless signing, SBOM attestation, and Kyverno image verification at admission *(in progress)* |

More on the way: OpenTelemetry observability platform, chaos and DR lab, an agentic AI SRE assistant, a FinOps control loop, and DORA delivery metrics measured across the whole platform.

---

### How I think about this work

- **Measured beats impressive.** I'd rather publish "0 failed requests across 12 node rotations under 500 RPS" than an uptime figure nobody can check.
- **Trade-offs belong in the README.** Every repo documents what I chose, what I gave up, and what I'd do differently — that section is usually more useful than the code.
- **Nothing gets applied by hand.** If it isn't in Git with a review and a policy gate, it isn't the platform.

📫 Reach me at **ramyakeerthikondisetty@gmail.com**
