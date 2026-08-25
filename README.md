# Ramya Keerthi Kondisetty

**Java · DevOps · Platform Engineer** based in Missouri, USA

[LinkedIn](https://www.linkedin.com/in/ramyakeerthikondisetty) · [Email](mailto:ramyakeerthikondisetty@gmail.com) · Open to Java, DevOps, SRE and platform engineering roles

I write Java services and run the platforms they live on. Four years across Spring Boot, Kafka, JPA and the JVM on one side, and AWS, Kubernetes, OpenShift and CI/CD on the other. Most of what I know came from the gap between those two: the code that was fine until it met a memory limit, a slow vendor, or a second replica.

## Impact

- Supported 27 microservices on EKS serving a field-service mobile application.
- Reduced environment provisioning from one week to about one hour with reusable Terraform.
- Reduced deployment time from half a day to about 30 minutes using GitLab CI and Argo CD.
- Improved mean time to recovery by 30% through better observability and post-incident follow-through.

## Java, and the things that break in production

Nine small services, each about one failure that is easy to get wrong and hard to see. Every number in these READMEs comes from a test or a script in the repository, and CI re-checks them.

| Repository | The thing it is about |
| --- | --- |
| [spring-boot-rest-api](https://github.com/keerthikondisetty/spring-boot-rest-api) | A REST service with the state machine in the enum, optimistic locking, and RFC 7807 errors. 409 on a conflicting update, proven rather than described. |
| [jvm-container-memory](https://github.com/keerthikondisetty/jvm-container-memory) | Why a container exits 137 with no OutOfMemoryError in the log. Measured heap against eight container limits, and the two settings that fix it. |
| [spring-kafka-pipeline](https://github.com/keerthikondisetty/spring-kafka-pipeline) | At-least-once delivery, an idempotent consumer, and a dead letter topic. Three real bugs are written up, including one where the DLT tests passed while nothing worked. |
| [spring-redis-cache](https://github.com/keerthikondisetty/spring-redis-cache) | Cache-aside with the parts people skip: stampede protection, negative caching, jittered TTLs. Thirty simultaneous readers, one database query. |
| [spring-dao-sql-tuning](https://github.com/keerthikondisetty/spring-dao-sql-tuning) | N+1 queries counted exactly: 51, then 3, then 1. Includes the fetch-join pagination trap and what a missing index costs on 200k rows. |
| [soap-to-rest-bridge](https://github.com/keerthikondisetty/soap-to-rest-bridge) | A REST facade over SOAP. Four vendor failures that all arrive as HTTP 500, mapped to four different status codes, with timeouts that are not zero. |
| [openliberty-modernization](https://github.com/keerthikondisetty/openliberty-modernization) | Jakarta EE off WebSphere and into containers. server.xml as the artifact, secrets as mounted files, and liveness against readiness proven by stopping the database. |
| [jenkins-shared-library](https://github.com/keerthikondisetty/jenkins-shared-library) | One Groovy library replacing twenty-odd Jenkinsfiles. Production from tags only, nothing tagged latest, and no cluster credentials on the agent. |
| [spring-boot-observability](https://github.com/keerthikondisetty/spring-boot-observability) | Why averaging p99 across pods is wrong, measured at 36% off, and what one bad label costs: 1 series against 500. |

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

- **Java:** Spring Boot, Spring MVC, JPA/Hibernate, Kafka, Redis, JUnit, Maven, Jakarta EE, Open Liberty
- **Cloud and platform:** AWS, EKS, Kubernetes, OpenShift, Docker, Helm, Terraform/OpenTofu, Argo CD
- **Delivery:** GitLab CI, GitHub Actions, Jenkins, Groovy, Python, Bash
- **Reliability:** Prometheus, Grafana, OpenTelemetry, Datadog, PagerDuty
- **Security:** IAM/IRSA, Vault, Trivy, Snyk, policy-as-code

## Certifications

- AWS Certified Solutions Architect, Associate
- Certified Kubernetes Administrator (CKA)
- Oracle Certified Associate, Java SE 8 Programmer

## A few things I will argue about

Liveness and readiness should point at different endpoints. If liveness checks the database, one database blip restarts every pod, which does nothing for the database and takes the application down too.

A metric that cannot be computed should say so rather than report zero. An unmeasured change failure rate and a genuinely good one look identical on a dashboard, and only one of them is good news.

Anything that deletes should be hard to run by accident. Dry run is the default, and a cleanup that would remove most of what it examined is more likely a bug in the filter than a real backlog.

Queue alerts should be on age, not depth. A burst of a thousand that drains in a minute is a healthy system; ten stuck for an hour is an incident. Depth cannot tell those apart.

You cannot average a percentile. The mean of two pods' p99 is not the p99 of anything, and every dashboard that aggregates replicas from client-side percentiles is quietly wrong. Export buckets and let Prometheus do the quantile.

A JVM heap sized in megabytes ignores the container limit it is running under. That is how you get exit code 137 and nothing in the log that mentions Java at all.

## Current focus

I am exploring AI for operations where it can reduce investigation time without taking unsafe action: correlating alerts with recent changes, citing evidence, and proposing a change that a human still reviews.

My operating principle is simple: **make infrastructure boring, make failures explainable, and make recovery routine.**
