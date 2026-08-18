<div align="center">

# 👋 Hi, I'm Rizwan Zafar

### 🚀 DevOps & Platform Infrastructure Engineer

**Cloud Infrastructure • Kubernetes • Automation • CI/CD • Observability • Networking**

<br>

[![GitHub](https://img.shields.io/badge/GitHub-rizwan441-181717?style=for-the-badge&logo=github)](https://github.com/rizwan441)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Rizwan%20Zafar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](YOUR_LINKEDIN_URL)
[![AWS](https://img.shields.io/badge/AWS-Cloud-232F3E?style=for-the-badge&logo=amazonaws)](https://aws.amazon.com/)
[![Azure](https://img.shields.io/badge/Azure-Cloud-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)](https://azure.microsoft.com/)

<br><br>

```text
┌──────────────────────────────────────────────────────────────┐
│                                                              │
│  rizwan@devops:~$ whoami                                     │
│                                                              │
│  DevOps & Platform Infrastructure Engineer                   │
│                                                              │
│  rizwan@devops:~$ focus                                      │
│                                                              │
│  Kubernetes • Linux • AWS • Azure • Docker • CI/CD           │
│  Terraform • Ansible • GitOps • Observability • Networking   │
│                                                              │
│  rizwan@devops:~$ status                                     │
│                                                              │
│  ● AUTOMATING    ● MONITORING    ● DEBUGGING    ● BUILDING   │
│                                                              │
└──────────────────────────────────────────────────────────────┘


🧑‍💻 About Me

I'm a DevOps & Platform Infrastructure Engineer focused on building,
automating, monitoring, and troubleshooting production infrastructure.

My work spans Linux, cloud platforms, Kubernetes/OpenShift, Docker,
CI/CD, infrastructure automation, networking, observability, and
distributed systems.

I enjoy going beyond deployment:

Build → Deploy → Observe → Debug → Secure → Automate → Improve
⚙️ Core Engineering Areas
Area	Technologies
☁️ Cloud	AWS • Azure
☸️ Containers	Kubernetes • OpenShift • Docker
🔄 CI/CD	GitHub Actions • Jenkins
🏗️ IaC	Terraform • Ansible
📊 Observability	Prometheus • Grafana • Alertmanager
🌐 Networking	L2/L3 • VLAN • STP • Routing • Nginx • UFW
🗄️ Data	PostgreSQL • Redis • MySQL • MongoDB • ClickHouse
📨 Messaging	NATS JetStream
🐧 Systems	Linux • Bare Metal • Systemd
🔐 Operations	Security • Troubleshooting • Production Debugging
---

# 🚀 Featured Engineering Projects

<div align="center">

### 🟢 Production & Infrastructure Engineering

</div>

---

## 🚀 1.18 Billion Record Carrier DID Lookup Platform

> High-scale telecom data platform designed around in-memory lookups,
> PostgreSQL persistence, event streaming, caching, and observability.

### 📊 Scale

```text
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│              CARRIER DID LOOKUP PLATFORM                   │
│                                                             │
│                  1,180,000,000+ Records                     │
│                                                             │
│              Target: Sub-Millisecond Lookup                 │
│                                                             │
│              Operational RAM Ceiling: ~128 GB               │
│                                                             │
└─────────────────────────────────────────────────────────────┘
🏗️ Architecture
                         ┌───────────────┐
                         │    Clients    │
                         └───────┬───────┘
                                 │
                                 ▼
                       ┌───────────────────┐
                       │   Lookup Service  │
                       │        Go         │
                       └─────────┬─────────┘
                                 │
                                 ▼
                       ┌───────────────────┐
                       │  In-Memory Index  │
                       │  Fast Lookups     │
                       └─────────┬─────────┘
                                 │
              ┌──────────────────┼──────────────────┐
              │                  │                  │
              ▼                  ▼                  ▼
        PostgreSQL            Redis          NATS JetStream
      Source of Truth         Cache             Events
              │
              ▼
         ClickHouse
        Analytics/Data
🔧 Technology Stack

Go PostgreSQL 16 Redis 7 NATS JetStream ClickHouse
Docker Prometheus Grafana Linux

🧠 Engineering Work
Designed infrastructure considerations for 1.18B+ records
Analyzed memory requirements for large in-memory datasets
Identified an operational ~128 GB RAM ceiling
Designed for sub-millisecond lookup requirements
Separated PostgreSQL persistence from the high-speed serving layer
Used Redis for caching
Used NATS JetStream for event-driven communication
Used ClickHouse for analytical workloads
Investigated CPU/RSS behavior and OOM risks
Diagnosed PostgreSQL deadlocks including SQLSTATE 40P01
Implemented deterministic ordering and retry strategies
📊 Infrastructure Monitoring Platform
Centralized Monitoring Across a Hybrid Server Fleet

                         ┌──────────────────┐
                         │     Grafana      │
                         │    Dashboards    │
                         └────────▲─────────┘
                                  │
                                  │
                         ┌────────┴─────────┐
                         │    Prometheus    │
                         │     Metrics      │
                         └────────▲─────────┘
                                  │
                ┌─────────────────┼─────────────────┐
                │                 │                 │
                ▼                 ▼                 ▼
          Node Exporter        cAdvisor          Endpoints
                │                 │                 │
                ▼                 ▼                 ▼
          Bare Metal           Docker           Services
                │
                ▼
          Hybrid Server Fleet
⚙️ What I Built
Centralized Prometheus + Grafana + Alertmanager
Host-level monitoring
Container monitoring
Database monitoring
Endpoint monitoring
Automated dashboard generation
Python-based dashboard source of truth
GitOps-oriented deployment workflow
Post-deployment health validation
UFW-based network segmentation
Automated host onboarding
🔍 Production Troubleshooting

Investigated a monitoring problem where cAdvisor container metrics
could disappear after containers stopped.

Used:

last_over_time()

and:

container_last_seen

to build more reliable container-health detection.

🔧 Technology Stack

Prometheus Grafana Alertmanager cAdvisor
Node Exporter Docker Python ClickHouse UFW

☸️ Kubernetes & OpenShift Infrastructure
                      Git Repository
                            │
                            ▼
                     CI/CD Pipeline
                            │
                 ┌──────────┴──────────┐
                 ▼                     ▼
           Docker Build             Tests
                 │                     │
                 └──────────┬──────────┘
                            ▼
                    Harbor Registry
                            │
                            ▼
                       Kubernetes
                            │
              ┌─────────────┼─────────────┐
              ▼             ▼             ▼
            Helm         Services       Ingress
              │
              ▼
                       Production
Focus Areas
Kubernetes deployments
OpenShift administration
Helm deployments
Docker containerization
Container networking
Macvlan networking
Service troubleshooting
Production rollout validation
Health checks
Deployment automation
🧰 Platform Stack

Kubernetes OpenShift Docker Helm Harbor
Linux Ansible Terraform

🔄 CI/CD & GitOps
Developer
    │
    ▼
Git Push
    │
    ▼
┌──────────────────────┐
│     CI Pipeline      │
├──────────────────────┤
│ Tests                │
│ Static Analysis      │
│ Docker Build         │
│ Image Tagging        │
│ Registry Push        │
└──────────┬───────────┘
           │
           ▼
    Harbor Registry
           │
           ▼
     Deployment
           │
           ▼
    Health Validation
           │
           ▼
       Production
🛠️ Technologies

GitHub Actions Jenkins Docker Harbor
Kubernetes Helm Ansible Terraform GitOps

🔥 Production Troubleshooting

One of my strongest engineering interests is finding the actual root
cause instead of simply restarting services.

Application
     │
     ▼
Container
     │
     ▼
Process
     │
     ▼
Systemd
     │
     ▼
Network
     │
     ▼
Kernel
     │
     ▼
Hardware
Examples
PostgreSQL deadlock investigation
OOM risk detection
Container monitoring failures
Linux networking troubleshooting
Nginx performance investigation
UFW firewall behavior
Kubernetes troubleshooting
Docker networking issues
L2/L3 network fault isolation
<div align="center">
⚡ Build → Automate → Observe → Debug → Improve
</div> ```

