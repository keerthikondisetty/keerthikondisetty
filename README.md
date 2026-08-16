# Ramya Keerthi Kondisetty

**DevOps · SRE · Platform Engineer** based in Missouri, USA

[LinkedIn](https://www.linkedin.com/in/ramyakeerthikondisetty) · [Email](mailto:ramyakeerthikondisetty@gmail.com) · Open to DevOps, SRE, and platform engineering roles

I build AWS and Kubernetes platforms that make delivery safer and operations less surprising. Over four years in DevOps and SRE, I have worked across infrastructure, CI/CD, observability, incident response, and the day-two work that keeps production dependable.

## Impact

- Supported 27 microservices on EKS serving a field-service mobile application.
- Reduced environment provisioning from one week to about one hour with reusable Terraform.
- Reduced deployment time from half a day to about 30 minutes using GitLab CI and Argo CD.
- Improved mean time to recovery by 30% through better observability and post-incident follow-through.

## One application, end to end

These five repositories follow a single small service through its whole life. Each one stands alone, and together they are the walkthrough I would give of how I build and run something.

| Repository | What it shows |
| --- | --- |
| [devops-demo-app](https://github.com/keerthikondisetty/devops-demo-app) | A webhook receiver and a background worker: signature verification, an idempotent queue, retries, dead-lettering and graceful shutdown on SIGTERM. The same pipeline is written three times, for GitHub Actions, GitLab CI and Jenkins, so the differences are visible side by side. |
| [terraform-aws-infra](https://github.com/keerthikondisetty/terraform-aws-infra) | The AWS environment it runs in. VPC across two AZs, ALB, autoscaling group with no SSH, RDS reachable only from the application security group. |
| [k8s-deploy](https://github.com/keerthikondisetty/k8s-deploy) | The same service on Kubernetes: receiver and worker as separate Deployments, manifests and a Helm chart, verified by deploying to a real cluster rather than by linting the YAML. |
| [monitoring-stack](https://github.com/keerthikondisetty/monitoring-stack) | Prometheus, Alertmanager and Grafana watching it. Alerts on queue *age* rather than depth, each carrying a runbook, unit tested and fired for real in CI. |
| [aws-automation](https://github.com/keerthikondisetty/aws-automation) | The day-two chores: tag auditing and snapshot retention, built around the safeguards that make deletion survivable. |

## Also worth a look

| Repository | What it shows |
| --- | --- |
| [ai-sre-agent](https://github.com/keerthikondisetty/ai-sre-agent) | A read-only incident investigator, scored against faults with known causes. Grades accuracy, calibration and guardrails separately, because a confidently wrong answer is worse than an uncertain one. |
| [finops-autopilot](https://github.com/keerthikondisetty/finops-autopilot) | Cost anomaly detection and rightsizing, designed around knowing when to stay quiet. |
| [eks-gitops-platform](https://github.com/keerthikondisetty/eks-gitops-platform) | The larger one: Karpenter, Cilium, Argo CD app-of-apps, Kyverno admission control and SLI-gated canary rollouts. |
| [platform-toolkit](https://github.com/keerthikondisetty/platform-toolkit) | Python and Bash utilities for semantic versions, safe image retention, retries and locking. |

Every repository has a README that explains the decisions rather than the tool list, and a `make verify` that runs the same checks CI does. Where something has never been applied against a real AWS account, the README says so.

## Core toolkit

- **Cloud and platform:** AWS, EKS, Kubernetes, Docker, Helm, Terraform/OpenTofu, Argo CD
- **Delivery:** GitLab CI, GitHub Actions, Jenkins, Python, Bash
- **Reliability:** Prometheus, Grafana, OpenTelemetry, Datadog, PagerDuty
- **Security:** IAM/IRSA, Vault, Trivy, Snyk, policy-as-code

## Certifications

- AWS Certified Solutions Architect – Associate
- Certified Kubernetes Administrator (CKA)

## A few things I will argue about

Liveness and readiness should point at different endpoints. If liveness checks the database, one database blip restarts every pod, which does nothing for the database and takes the application down too.

A metric that cannot be computed should say so rather than report zero. An unmeasured change failure rate and a genuinely good one look identical on a dashboard, and only one of them is good news.

Anything that deletes should be hard to run by accident. Dry run is the default, and a cleanup that would remove most of what it examined is more likely a bug in the filter than a real backlog.

Queue alerts should be on age, not depth. A burst of a thousand that drains in a minute is a healthy system; ten stuck for an hour is an incident. Depth cannot tell those apart.

## Current focus

I am exploring AI for operations where it can reduce investigation time without taking unsafe action: correlating alerts with recent changes, citing evidence, and proposing a change that a human still reviews.

My operating principle is simple: **make infrastructure boring, make failures explainable, and make recovery routine.**
