# Hello world 👋

I'm a freelance **Platform, Cloud, DevOps & Kubernetes Consultant** building secure, automated cloud infrastructure, internal platforms, delivery systems, and AI/ML platforms.

This profile is a catalog of independent reference implementations inspired by real requirements I have encountered through consulting. To protect client confidentiality and intellectual property, the public projects are rebuilt with independently created infrastructure and public or synthetic data—they contain no client code, data, or resources.

[Portfolio](https://www.arguswatcher.net) · [LinkedIn](https://www.linkedin.com/in/simonangelfong/) · [GitHub](https://github.com/simonangel-fong)

---

## 🏅 Certifications

- ✅ Certified Kubernetes Administrator (CKA)
- ✅ AWS Certified Solutions Architect – Associate (SAA)
- ✅ Red Hat Certified System Administrator (RHCSA)
- Certified Kubernetes Security Specialist (CKS) — In progress

---

## What I Help Build

| Capability                 | Typical challenges                                                                                                                              |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **Platform Engineering**   | Standardizing fragmented technology stacks, enabling self-service, enforcing guardrails, and supporting multiple teams on shared infrastructure |
| **Cloud & Kubernetes**     | Designing `AWS`/`Azure` architectures, adopting `EKS`/`AKS`, automating infrastructure, and modernizing workloads                               |
| **Delivery & Reliability** | Implementing `CI/CD` and `GitOps`, controlling release risk, improving observability, and automating incident diagnosis                         |
| **AI/ML Platforms**        | Building portable ML pipelines, provisioning `GPU` infrastructure, tracking experiments, and deploying models reliably                          |

---

## Featured Implementations

### 🏢 Multi-Tenant Kubernetes Platform — EKS

**Challenge:** Help a growing organization standardize independently managed applications on a shared platform while preserving team autonomy, isolation, and governance.

**Implementation:** Built a GitOps-driven `EKS` platform with automated tenant onboarding, workload-specific compute, policy enforcement, secrets integration, TLS/DNS automation, and service-mesh networking.

**Evidence:** A tenant is defined through one configuration file; GitOps creates its platform boundaries and deploys an application to a live endpoint in approximately three minutes.

`AWS EKS` `Terraform` `Argo CD` `Karpenter` `Istio` `External Secrets`

[Case study](https://simonangel-fong.github.io/multi-tenant-cluster-eks/) · [Source code](https://github.com/simonangel-fong/multi-tenant-cluster-eks)

### 🔄 GitOps Release-Risk Control

**Challenge:** Reduce production deployment risk without sacrificing delivery speed or requiring operators to coordinate every release manually.

**Implementation:** Applied controls across three lifecycle phases: pre-release validation, progressive delivery, and post-release monitoring with automated operational notifications.

**Evidence:** The implementation demonstrates early validation, canary and blue-green delivery patterns, automated analysis, rollback controls, and fast release feedback.

`Kubernetes` `Argo CD` `Argo Rollouts` `Grafana` `Slack`

[Live case study](https://gitops.arguswatcher.net/) · [Source code](https://github.com/simonangel-fong/Project_GitOps_Risk_Control_Platform_Repo)

### ⚙️ GPU-Enabled MLOps Platform — Kubeflow on EKS

**Challenge:** Close the gap between ML experimentation and reliable production use by connecting model development, platform infrastructure, and delivery automation.

**Implementation:** Built an end-to-end platform for a substituted computer-vision workload, integrating Kubeflow, MLflow, Katib, DVC, KServe, GPU infrastructure, IaC, and GitOps.

**Evidence:** The platform demonstrates the complete lifecycle from experimentation and training through model tracking, validation, deployment, and inference.

`Kubeflow` `KServe` `MLflow` `Katib` `DVC` `AWS EKS` `Karpenter` `Terraform` `Argo CD`

[Live case study](https://kubeflow-yolo.arguswatcher.net) · [Source code](https://github.com/simonangel-fong/kubeflow-yolo)

### 🔎 Kubernetes AIOps — Automated Incident Diagnosis

**Challenge:** Reduce manual correlation of Kubernetes alerts, pod status, logs, events, and runbooks without giving an AI system unsafe production access.

**Implementation:** Built an event-driven diagnostic pipeline in which an AI agent receives alerts, investigates the cluster through read-only RBAC permissions, and sends findings to operators for review.

**Evidence:** The design separates observation, diagnosis, and remediation authority, keeping human operators in control of production changes.

`Amazon Bedrock AgentCore` `AWS EKS` `CloudWatch` `EventBridge` `Lambda` `Terraform` `GitHub Actions`

[Live case study](https://aiops.arguswatcher.net/) · [Source code](https://github.com/simonangel-fong/aiops-agentcore)

---

## Project Catalog

The projects below explore common engineering questions that arise during platform, cloud, DevOps, and AI/ML engagements.

### Platform Engineering & Kubernetes

| Project                                                                                  | Engineering question                                                                                     | Stack                                          |
| ---------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | ---------------------------------------------- |
| [Kubernetes Deployment Playbook](https://simonangel-fong.github.io/k8s-deploy/)          | How should teams choose among rolling, recreate, canary, blue-green, A/B, and shadow deployments?        | AKS, Argo CD, Argo Rollouts, Istio, Kiali      |
| [Multi-Cloud Kubernetes](https://simonangel-fong.github.io/multi-cloud-cluster/)         | How can one application run across AWS and Azure with unified delivery, traffic control, and monitoring? | EKS, AKS, Terraform, Argo CD, Helm, Cloudflare |
| [Istio Sidecar Mode](https://github.com/simonangel-fong/istio-sidecar)                   | How do ingress, TLS, traffic management, canary delivery, A/B testing, and shadowing work with sidecars? | Istio, AKS, cert-manager                       |
| [Istio Ambient Mode](https://github.com/simonangel-fong/istio-ambient)                   | How do the same service-mesh capabilities work with ztunnel and waypoint proxies instead of sidecars?    | Istio, AKS, cert-manager                       |
| [EKS Argo CD Capability](https://github.com/simonangel-fong/argocd-eks-capability)       | How can the EKS-managed Argo CD capability support cluster delivery?                                     | EKS, Argo CD                                   |
| [AKS Argo CD with Helm](https://github.com/simonangel-fong/argocd-aks-helm)              | How can Argo CD be installed and managed consistently on AKS?                                            | AKS, Argo CD, Helm                             |
| [KServe GPU Inference](https://github.com/simonangel-fong/llm-kserve-eks)                | How can an LLM inference service run on GPU-backed Kubernetes infrastructure?                            | EKS, KServe, GPU nodes, Argo CD, Open WebUI    |
| [IP Exhaustion Mitigation](https://github.com/simonangel-fong/runbook-eks-ip-exhaustion) | How can pod IP exhaustion in Amazon EKS be mitigated without causing downtime to existing workloads?     | EKS, VPC                                       |

### Cloud Architecture & Automation

| Project                                                                                                                   | Engineering question                                                                   | Stack                                   |
| ------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | --------------------------------------- |
| [Automated Architecture Benchmark — EKS](https://github.com/simonangel-fong/Project-Automated-Architecture-Benchmark-EKS) | How much does each architecture decision improve behavior under identical load on EKS? | EKS, Terraform, GitHub Actions          |
| [Automated Architecture Benchmark — ECS](https://github.com/simonangel-fong/Project-Automated-Architecture-Benchmark-ECS) | How much does each architecture decision improve behavior under identical load on ECS? | ECS, Terraform, GitHub Actions          |
| [Hybrid Cloud Data Warehouse](https://github.com/simonangel-fong/Portfolio-Project-Toronto-Shared-Bike-Repo)              | How can an on-premises data warehouse integrate with serverless AWS services?          | PostgreSQL, AWS Lambda, API Gateway, S3 |
| [VM-Based GitOps](https://github.com/simonangel-fong/ansible-gitops-vm)                                                   | How can GitOps practices extend to virtual-machine environments?                       | Ansible, Jenkins, EC2                   |
| [Multi-Environment Jenkins Pipeline](https://github.com/simonangel-fong/jenkins-multi-environment)                        | How can one pipeline provision and deploy multiple AWS environments consistently?      | Jenkins, Terraform, AWS                 |
| [Docker Multi-Stage Build](https://github.com/simonangel-fong/docker-multi-stage-build)                                   | How much can multi-stage builds reduce Spring Boot and FastAPI container image sizes?  | Docker                                  |

### AI/ML Platform Engineering

| Project                                                                                        | Engineering question                                                                                  | Stack                                                |
| ---------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------- |
| [SageMaker YOLO Pipeline](https://github.com/simonangel-fong/sagemaker-yolo)                   | How can training, experiment tracking, quality gating, and serverless inference be automated on AWS?  | SageMaker, MLflow, Lambda, CloudFront, S3, Terraform |
| [Toronto Shared Bike MLOps](https://github.com/simonangel-fong/Project-Toronto-Shared-Bike-ML) | How can a forecasting model move through an automated training and deployment workflow?               | SageMaker, Terraform                                 |
| [KubeTriage](https://github.com/simonangel-fong/Project-KubeTriage)                            | How can an AI agent summarize Kubernetes logs and likely root causes while retaining human oversight? | Argo CD, n8n, Kagent, Alertmanager                   |
| [Ollama CPU vs GPU](https://github.com/simonangel-fong/llm-ollama-ec2)                         | How does CPU and GPU inference performance differ across retrieval, generation, and memory tasks?     | Ollama, NVIDIA GPU, EC2, Terraform                   |

### CI/CD & Delivery Patterns

| Project                                                                                            | Engineering question                                                              | Stack                          |
| -------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | ------------------------------ |
| [Jenkins CI Pipeline with ECR](https://github.com/simonangel-fong/jenkins-ci-ecr)                  | How can an in-cluster Jenkins pipeline build and publish container images to ECR? | Jenkins, Docker, ECR           |
| [Multi-Environment Jenkins Pipeline](https://github.com/simonangel-fong/jenkins-multi-environment) | How can infrastructure changes move consistently across multiple environments?    | Jenkins, Terraform, AWS        |
| [Argo CD Notifications](https://github.com/simonangel-fong/argocd-notification)                    | How can inline and manifest-based notifications trigger Slack and GitHub Actions? | Argo CD, Slack, GitHub Actions |

---

## Core Toolkit

**Cloud:** AWS, Microsoft Azure, Cloudflare  
**Platforms:** Kubernetes, Amazon EKS, Azure AKS, Kubeflow, Karpenter, Istio  
**Infrastructure:** Terraform, Helm, Kustomize, Ansible, Docker  
**Delivery:** Argo CD, Argo Rollouts, GitHub Actions, Jenkins  
**Observability:** Prometheus, Grafana, Alertmanager  
**Development:** Python, Bash, Git, FastAPI

---

## Let's Talk

I can help with platform architecture, Kubernetes adoption, GitOps, cloud infrastructure automation, release engineering, and AI/ML platform development.

I'm available for **freelance and consulting engagements**.

[Portfolio](https://www.arguswatcher.net) · [LinkedIn](https://www.linkedin.com/in/simonangelfong/) · [GitHub](https://github.com/simonangel-fong)
