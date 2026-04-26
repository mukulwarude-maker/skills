# LinkedIn Keywords Bank

Use this as a reference vocabulary when analyzing a LinkedIn profile for keyword and semantic-entity coverage.

**When building the keyword / semantic-entity coverage analysis:**
1. First extract keywords from the provided JD.
2. Cross-reference with these categories to spot obvious omissions.
3. Only suggest keywords the candidate plausibly has experience with — do not suggest adding "Kubernetes" if they've never touched it.
4. Remember: LinkedIn's LLM-ranked search rewards **contextual use** of keywords (in headlines, bullets, About text) more than listing them in the Skills section alone.

---

## How to Use the Semantic Neighbor Principle

LinkedIn's 360Brew model understands semantic relationships. A profile that mentions "EKS clusters", "container orchestration", and "Helm charts" will rank for "Kubernetes" even if the word "Kubernetes" appears only twice. The model knows these are neighbors.

**When reviewing a profile:**
- Don't just count exact keyword matches
- Check for semantic neighbor coverage — if the JD says "Kubernetes", look for: EKS/GKE/AKS, Helm, container orchestration, pod management, cluster autoscaling, service mesh
- A profile with 4 semantic neighbors but missing the exact keyword is more discoverable than a profile that lists "Kubernetes" once in the skills section and nowhere else

---

## DevOps / SRE / Platform Engineering

### CI/CD & Automation
Jenkins, GitHub Actions, GitLab CI, CircleCI, ArgoCD, Spinnaker, Flux, Tekton, Drone CI, Travis CI, Bamboo, TeamCity, Blue-Green Deployment, Canary Deployment, Rolling Update, Feature Flags, Continuous Integration, Continuous Deployment, Continuous Delivery, Pipeline as Code, Release Automation, Deployment Automation

### Containers & Orchestration
Docker, Kubernetes (K8s), Amazon EKS, Google GKE, Azure AKS, OpenShift, Helm, Kustomize, Istio, Linkerd, Service Mesh, CRI-O, containerd, Pod, ReplicaSet, StatefulSet, DaemonSet, Ingress, HPA (Horizontal Pod Autoscaler), VPA (Vertical Pod Autoscaler), Cluster Autoscaler, Karpenter, KEDA, Rancher, K3s

### Infrastructure as Code (IaC)
Terraform, Ansible, CloudFormation (AWS CFN), Pulumi, Crossplane, Packer, Vagrant, Chef, Puppet, SaltStack, AWS CDK, Terragrunt, Atlantis, OpenTofu, Bicep (Azure), CDK for Terraform

### Cloud Platforms
**AWS:** EC2, S3, Lambda, EKS, ECS, Fargate, IAM, VPC, RDS, Aurora, DynamoDB, CloudFront, Route 53, API Gateway, CloudWatch, CloudTrail, SQS, SNS, Kinesis, Glue, Redshift, Athena, Secrets Manager, SSM (Systems Manager), CodePipeline, CodeBuild, CodeDeploy, AWS Organizations, Control Tower, Service Control Policies (SCPs), FinOps, Cost Explorer, Trusted Advisor

**GCP:** Compute Engine, GKE, Cloud Functions, Cloud Run, BigQuery, Cloud Storage, Pub/Sub, Cloud SQL, Spanner, IAM, VPC, Cloud Load Balancing, Cloud Armor, Artifact Registry, Cloud Build, Workflows

**Azure:** AKS, Azure Functions, Azure DevOps, Azure Pipelines, App Service, Cosmos DB, Azure Active Directory (AAD / Entra ID), Blob Storage, Application Gateway, APIM, Azure Monitor, Log Analytics, Container Registry (ACR), Azure Policy, Management Groups

**Multi-cloud / FinOps:** HashiCorp Cloud Platform (HCP), Infracost, Kubecost, CAST AI, OpenCost

### Monitoring, Observability & Reliability
Prometheus, Grafana, Datadog, New Relic, Splunk, ELK Stack (Elasticsearch, Logstash, Kibana), Fluentd, Fluent Bit, Loki, Tempo, OpenTelemetry, Jaeger, Zipkin, PagerDuty, OpsGenie, VictoriaMetrics, Thanos, Cortex, SLO (Service Level Objective), SLI (Service Level Indicator), SLA (Service Level Agreement), Error Budget, MTTR (Mean Time to Restore), MTTD (Mean Time to Detect), MTTI (Mean Time to Identify), Incident Management, On-Call Rotation, Runbook, Post-Mortem / Blameless Post-Mortem

### Security / DevSecOps
HashiCorp Vault, SonarQube, Trivy, Snyk, Aqua Security, Prisma Cloud, Wiz, Checkov, SAST, DAST, SCA (Software Composition Analysis), RBAC, ABAC, SSO, SAML 2.0, OAuth 2.0, OIDC, mTLS, OPA (Open Policy Agent), Gatekeeper, Falco, CIS Benchmarks, Secrets Management, KMS (Key Management Service), PKI, Zero Trust, Least Privilege, Image Scanning, SBOM (Software Bill of Materials), Supply Chain Security, SLSA Framework, FIPS 140-2, SOC 2, ISO 27001

### Scripting & Programming
Python, Bash / Shell scripting, Go (Golang), YAML, JSON, HCL, Jinja2, Groovy, Ruby, PowerShell, TypeScript, JavaScript (Node.js), Perl, Makefile

### Networking
TCP/IP, DNS, HTTP/HTTPS, TLS/SSL, Load Balancer, Reverse Proxy, Nginx, HAProxy, Envoy Proxy, Traefik, CDN (Content Delivery Network), VPN, Site-to-Site VPN, Direct Connect, Transit Gateway, VPC Peering, PrivateLink, Subnet, CIDR, Security Groups, NACL (Network ACL), WAF (Web Application Firewall), DDoS Protection, BGP, SD-WAN

### Databases & Storage
PostgreSQL, MySQL, MariaDB, MongoDB, Redis, Memcached, Apache Cassandra, Elasticsearch, Amazon S3, Amazon EFS, Amazon EBS, NFS, Ceph, Persistent Volume, Storage Class, Database Backup, Disaster Recovery, RTO (Recovery Time Objective), RPO (Recovery Point Objective), Replication, Read Replicas, Sharding, Connection Pooling (PgBouncer), Database Migration

### Methodology & Practice
Agile, Scrum, Kanban, SAFe, SRE (Site Reliability Engineering), DevOps, GitOps, Platform Engineering, Internal Developer Platform (IDP), Infrastructure as Code, Immutable Infrastructure, Blue/Green Deployment, Canary Release, Feature Flagging, Chaos Engineering (Chaos Monkey, Gremlin, LitmusChaos), Incident Response, Blameless Culture, FinOps, Shift-Left Security, Developer Experience (DevEx / DX), Automation-First, Everything as Code

---

## Software Engineering (Backend / Full Stack)

### Languages & Runtimes
Python, Java (Spring Boot, Micronaut), Go (Golang), Node.js (Express, NestJS), Rust, C++, C#, .NET, Ruby on Rails, PHP (Laravel), Scala, Kotlin

### APIs & Integration
REST API, GraphQL, gRPC, WebSocket, SOAP, OpenAPI (Swagger), API Gateway, Webhooks, Event-Driven Architecture, Pub/Sub, Apache Kafka, RabbitMQ, NATS, AWS EventBridge, Apache Flink

### Architecture Patterns
Microservices, Monolith to Microservices Migration, Event Sourcing, CQRS, Saga Pattern, DDD (Domain-Driven Design), Hexagonal Architecture, SOLID Principles, 12-Factor App

### Frontend (for full-stack)
React, Next.js, Vue.js, Angular, TypeScript, Tailwind CSS, Webpack, Vite

---

## Data / ML Engineering

### Data Engineering
Apache Spark, Apache Kafka, Flink, Airflow, dbt (data build tool), Great Expectations, Fivetran, Stitch, Snowflake, Databricks, Delta Lake, Apache Hudi, Apache Iceberg, Data Lakehouse, ETL, ELT, Data Pipeline, Data Orchestration, Data Quality, Medallion Architecture

### Machine Learning / MLOps
TensorFlow, PyTorch, scikit-learn, Hugging Face, LangChain, RAG (Retrieval-Augmented Generation), MLflow, Kubeflow, BentoML, Seldon, Feature Store, Model Registry, A/B Testing, Shadow Mode Testing, Canary Deployment (ML), Data Drift, Model Monitoring, LLM, Vector Database (Pinecone, Weaviate, Qdrant), Embeddings, Fine-tuning, RLHF

---

## Leadership & Soft Skills (Senior Profiles)

These keywords signal seniority and leadership. Use them when reviewing senior profiles — their absence is a gap worth flagging.

### Technical Leadership
Mentored engineers, Technical roadmap, Architecture decisions, RFC (Request for Comments), ADR (Architecture Decision Record), Technical direction, System design, Design review, Code review, Engineering standards, On-call ownership, Incident commander

### Organizational Impact
Cross-functional collaboration, Stakeholder alignment, Executive communication, Engineering culture, Hiring and interviewing, Onboarding, Developer productivity, Cost reduction, Platform reliability, Engineering excellence

### Scale Indicators
Users served (e.g., "platform serving 50M requests/day"), Services owned (e.g., "owned 40+ microservices"), Team size ("led a team of 12 engineers"), Infrastructure size ("managed 2,000+ nodes across 3 regions"), Cost impact ("reduced AWS spend by $400K/year")

---

## How to Present Missing Keywords in a Review

When presenting keyword gaps:

1. **JD keywords first.** If the JD says "Terraform" and the profile doesn't mention it anywhere, that's the primary miss.
2. **Then semantic neighbors.** If "Terraform" is in the JD and "IaC" or "CloudFormation" is also in the JD but the profile only mentions "Ansible", flag the gap.
3. **Include both full name and abbreviation** where applicable: "Kubernetes (K8s)", "Infrastructure as Code (IaC)", "Site Reliability Engineering (SRE)".
4. **Don't suggest fabrication.** Only suggest keywords the candidate plausibly has experience with. If they've never done chaos engineering, don't recommend adding "LitmusChaos" to their Skills section. That will fail in the interview.
5. **Distinguish Skills section vs contextual use.** A keyword only in the Skills section ranks lower than a keyword used contextually in the About and Experience sections. Suggest moving important keywords into bullets.

---

## Non-DevOps Profiles

This bank is DevOps / SRE / Platform / Data / ML focused. For a purely frontend, product manager, or domain-specialist (finance, HR, marketing) profile:

- Use the JD as the primary keyword source
- Note explicitly in the review that your keyword coverage is based on the JD alone, not an extensive domain bank
- Flag this limitation in the Discoverability section so the user understands the analysis boundary
