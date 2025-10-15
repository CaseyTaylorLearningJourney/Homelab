# 🏠 Homelab | DevSecOps & DevOps Engineering Journey

Welcome!  
This repository documents my hands-on learning, experiments, and projects centered on Kubernetes, DevSecOps, and DevOps engineering. My background is in systems, networking, and security engineering with deep experience in enterprise environments.

## Purpose & Motivation

As a Systems Engineer, I build and maintain complex infrastructure daily—my homelab is where I break, experiment, secure, and automate:

- Learn and validate advanced DevOps and security concepts safely
- Experiment with infrastructure and security automation at scale
- Prototype real-world scenarios before rolling out at work
- Own and operate the full application lifecycle: architect, deploy, secure, scale, and recover

## Core Focus Areas

### Kubernetes & Platform Engineering
- Building, operating, and securing Kubernetes clusters
- Automating deployment, upgrades, and recovery
- Exploring cluster networking, CNI plugins, and service mesh integrations

### DevSecOps Practices
- Shifting security left in every DevOps pipeline and workflow
- Vulnerability management (firewall config, IDS/IPS, automated scanning)
- Secrets management, RBAC, policy automation, and least-privilege enforcement
- Incident response simulation, documentation, and process automation

### DevOps & Automation
- Infrastructure-as-Code with Ansible, Terraform, and GitOps
- CI/CD: progressive delivery, automated testing, secure artifact management
- Observability: monitoring, alerting, logging, and automated response

## Cybersecurity Integration

Security is embedded in everything I do, including:

- **Enterprise Perimeter & Network Defense**  
  Designed and managed access control systems, firewalls, IDS/IPS, and network segmentation  
  Automated DNS hygiene checks and vulnerability scans
- **Process Automation for Security**  
  Automated onboarding/offboarding, provisioned privileged access, and scheduled regular audits/scans
- **Vulnerability Management Programs**  
  Deployed continuous scanning and rapid patch cycles  
  Led corporate security projects to reduce risk surface and respond to threats
- **Security Operations**  
  Built and ran SOC/NOC teams, incident response, and staff security training initiatives
- **Identity & Access Management**  
  RBAC, least-privilege policy, and access review automation  
  Integrated security controls across on-premise, hybrid, and cloud

## Infrastructure Overview

My homelab features **enterprise-grade and business-class gear** built for real-world scale, redundancy, and speed.

### :computer: Hardware

#### Primary Site
- **HP Pro Mini 400 G9 Desktop PC**  
  Intel Core i5-13600T | 64GB RAM | 2×256GB SSD (system)  
  Connected via NFS to storage pool on Z840

- **HP Z840 Workstation**  
  2× Intel Xeon E5-2697 v4 | 256GB RAM  
  4× 250GB SSD (OS, RAID)  
  2× 4TB NVMe (fast VM OS storage)  
  4× 6TB HDD (backups, VM data, ISO storage)

#### Secondary Site
- **Dell PowerEdge R740xd**  
  2× Intel Xeon Gold 6150 | 256GB RAM  
  2× 500GB SSD (OS)  
  2× 4TB SSD (fast VM OS storage)  
  8× 10TB HDD (VM data, ISO storage)

#### Backup & DR
- **Converted Datto Appliance (TrueNAS Core)**  
  Intel Xeon D-1541 | 48GB RAM  
  4× 750GB SSD (OS)
  4× 6TB HDD + 2× 250GB cache SSDs (dedup and backup for both sites)

### Networking

- **Primary Site**
  - Software Controller running on LXC Container
  - Omada ER8411 Router: 16 VLANs, all with strict traffic rules (This is actually brand new. I jumped the gun on adding this to my hardware list. Previous Router was a ER7206, still functional just.... Well 10G, need I say more?)
  - Omada SX3008F Switch: server connectivity

- **Secondary Site**
  - Unifi UDM Pro: 16 VLANs, strictly locked down by traffic rules (Manages Unifi Equipment)
  - Unifi US XG16 & USW Pro Aggregation: aggregation switches for connectivity and failover

### Storage

- CEPH and TrueNAS provide NFS and block storage shared between clusters at the primary site.
- Secondary site has one host leveraging local storage arrays.

## Platforms & Tools

- **Virtualization/Clusters:** Proxmox VE, VMware, KVM/QEMU
- **Operating Systems:** Talos Linux, Ubuntu, AlmaLinux, Windows Server (legacy/testing)
- **Containerization:** Docker, containerd
- **IaC & Automation:** Ansible, Terraform, FluxCD, External Secrets Operator
- **Security/Monitoring:** Firewall appliances, IDS/IPS, Prometheus, Grafana, ELK Stack (testing)
- **Networking:** Enterprise firewalls/switches, VLAN segmentation, Tailscale for site-to-site tunnels

## Current & Upcoming Projects

- Document Talos Kubernetes cluster lifecycle (bootstrap, HA upgrades)
- Integrate vulnerability and compliance scanning in CI/CD pipelines
- Deploy advanced RBAC and policy-as-code for multi-tenant clusters
- Simulate incident response and automate remediation
- Rapid automated environment provisioning with IaC

## Roadmap

- Expand SAST/DAST tool testing in CI/CD
- Validate new security tools for containers, VMs, and hybrid infrastructure
- Document and share lessons (success _and_ failure) openly

## 📬 Get in Touch

Interested in DevSecOps, Kubernetes, automation, networking, or enterprise infrastructure?  
Let's connect, share ideas, and collaborate!

- 💼 LinkedIn: [www.linkedin.com/in/cltaylor0](https://www.linkedin.com/in/cltaylor0)
- 🖥️ GitHub: [CaseyTaylorLearningJourney/Homelab](https://github.com/CaseyTaylorLearningJourney/Homelab)

I'm always open to professional connections, knowledge-sharing, and feedback—reach out anytime!

---

**Topics:**  
Kubernetes | DevSecOps | GitOps | Virtualization | Cloud Security | Enterprise Hardware | Automation

---
