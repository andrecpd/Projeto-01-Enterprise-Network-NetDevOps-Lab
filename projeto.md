# Enterprise Network & NetDevOps Lab

![Network](https://img.shields.io/badge/Network-Engineering-blue)
![NetDevOps](https://img.shields.io/badge/NetDevOps-Automation-green)
![Ansible](https://img.shields.io/badge/Ansible-Automation-red)
![Python](https://img.shields.io/badge/Python-Automation-yellow)
![Terraform](https://img.shields.io/badge/Terraform-IaC-purple)
![GitHub](https://img.shields.io/badge/GitHub-Version%20Control-black)

## 📌 About the Project

This repository contains a professional **Enterprise Network & NetDevOps laboratory**, designed to simulate a real-world corporate network environment.

The project integrates **network engineering, cybersecurity, SD-WAN, routing, switching, automation, monitoring and Infrastructure as Code**, providing a practical environment for designing, implementing, testing and documenting network solutions.

The laboratory is designed to be deployed using platforms such as **PNETLab, EVE-NG or GNS3**.

---

## 🎯 Project Objectives

The main objectives are:

* Design an enterprise network architecture.
* Implement routing and switching technologies.
* Configure dynamic routing protocols.
* Implement network segmentation using VLANs and VRFs.
* Implement BGP and OSPF.
* Simulate MPLS environments.
* Implement SD-WAN and IPsec VPN.
* Configure enterprise firewalls.
* Automate network operations.
* Apply Infrastructure as Code concepts.
* Implement monitoring and observability.
* Apply Git and GitHub for infrastructure version control.
* Implement NetDevOps and CI/CD concepts.
* Document the entire infrastructure.

---

# 🏗️ Network Architecture

```text
                              INTERNET
                                  |
                             +---------+
                             |   ISP   |
                             +----+----+
                                  |
                           +------+------+
                           |  FIREWALL  |
                           | FortiGate /|
                           | Palo Alto  |
                           +------+------+
                                  |
                    +-------------+-------------+
                    |                           |
                +---+---+                   +---+---+
                | CORE1 |===================| CORE2 |
                +---+---+       OSPF        +---+---+
                    |                           |
                    |                           |
              +-----+-----+               +-----+-----+
              |    DATA   |               |    HQ     |
              |   CENTER  |               |   USERS   |
              +-----+-----+               +-----+-----+
                    |                           |
                Servers                     SD-WAN
                                                |
                              +-----------------+----------------+
                              |                                  |
                         +----+----+                        +----+----+
                         |BRANCH01 |                        |BRANCH02 |
                         +---------+                        +---------+
```

---

# 🌐 Technologies

## Routing

* IPv4
* IPv6
* OSPF
* BGP
* VRF
* Route Redistribution
* Routing Policies

## Switching

* VLAN
* Trunk
* STP
* EtherChannel
* Inter-VLAN Routing
* Layer 2 / Layer 3 Switching

## WAN

* MPLS
* IPsec
* SD-WAN
* WAN Failover
* Routing Policies
* QoS

## Security

* FortiGate
* Palo Alto
* Firewall Policies
* NAT
* VPN
* Network Segmentation
* Hardening
* Least Privilege
* Security Zones

## Automation

* Git
* GitHub
* Ansible
* Python
* Terraform
* REST APIs
* Infrastructure as Code
* CI/CD

## Monitoring

* Zabbix
* Grafana
* SNMP
* Syslog
* Network Telemetry

## Lab Platforms

* PNETLab
* EVE-NG
* GNS3

---

# 📊 IP Addressing Plan

| Segment   | Network         | Purpose                |
| --------- | --------------- | ---------------------- |
| VLAN 10   | 10.10.10.0/24   | Management             |
| VLAN 20   | 10.10.20.0/24   | Users                  |
| VLAN 30   | 10.10.30.0/24   | Servers                |
| VLAN 40   | 10.10.40.0/24   | Voice                  |
| VLAN 50   | 10.10.50.0/24   | Network Services       |
| Branch 01 | 10.20.10.0/24   | Branch Users           |
| Branch 02 | 10.30.10.0/24   | Branch Users           |
| Loopbacks | 10.255.255.0/24 | Router IDs             |
| P2P Links | 10.255.0.0/24   | Routing Infrastructure |

> The IPv4 addressing scheme is dedicated to the laboratory environment.

---

# 🔢 Loopback Addressing

| Device     | Loopback         |
| ---------- | ---------------- |
| R-CORE1    | 10.255.255.1/32  |
| R-CORE2    | 10.255.255.2/32  |
| R-EDGE1    | 10.255.255.3/32  |
| R-BRANCH01 | 10.255.255.11/32 |
| R-BRANCH02 | 10.255.255.12/32 |

---

# 🧪 Laboratory Roadmap

## LAB-00 — Environment Preparation

Preparation of the PNETLab/EVE-NG environment.

Topics:

* Device deployment
* Hostname standardization
* Management addressing
* Loopback configuration
* Basic device hardening

---

## LAB-01 — VLAN & Inter-VLAN Routing

Implementation of:

* VLANs
* Trunks
* Access ports
* SVIs
* Inter-VLAN Routing
* Basic segmentation

---

## LAB-02 — OSPF

Implementation of enterprise dynamic routing.

Topics:

* OSPF Area 0
* Router-ID
* Neighbors
* Loopback advertisement
* Cost
* Route selection
* Convergence
* Redundancy

---

## LAB-03 — BGP

Enterprise connectivity with ISP.

Topics:

* eBGP
* Autonomous Systems
* Prefix Lists
* Route Policies
* Route Filtering
* Local Preference
* MED
* AS Path

---

## LAB-04 — VRF

Network segmentation using Virtual Routing and Forwarding.

Topics:

* VRF creation
* VRF interfaces
* Independent routing tables
* Route leaking
* Traffic isolation

---

## LAB-05 — Firewall

Enterprise security architecture.

Topics:

* Security Zones
* Firewall Policies
* NAT
* Objects
* Services
* Logging
* Management Access
* Least Privilege
* Hardening

---

## LAB-06 — SD-WAN & IPsec

Enterprise WAN architecture connecting HQ and branches.

Topics:

* SD-WAN
* IPsec VPN
* Multiple WAN links
* SLA monitoring
* Application-based routing
* Failover
* Traffic steering

---

## LAB-07 — Ansible

Network automation.

Objectives:

* Inventory management
* Device discovery
* Configuration backup
* Configuration deployment
* Command execution
* Templates
* Variables
* Ansible Vault

---

## LAB-08 — Python

Network automation using Python.

Examples:

```text
Device Inventory
       |
       v
Python
       |
+------+------+
|             |
SSH           API
|             |
Cisco       Firewall
Huawei      SD-WAN
```

Automation examples:

* Interface validation
* BGP status
* OSPF neighbors
* Device reachability
* Configuration backup
* Report generation

---

## LAB-09 — Terraform

Infrastructure as Code.

Future implementations:

* AWS VPC
* Azure VNet
* Subnets
* Routing
* Security Groups
* Network Security Groups
* VPN
* Cloud connectivity

---

## LAB-10 — Monitoring

Network observability.

Technologies:

* Zabbix
* Grafana
* SNMP
* Syslog
* ICMP
* Interface monitoring
* CPU/Memory monitoring
* BGP monitoring
* OSPF monitoring

---

# 📁 Repository Structure

```text
enterprise-network-netdevops-lab/
│
├── README.md
├── .gitignore
│
├── docs/
│   ├── architecture.md
│   ├── addressing-plan.md
│   ├── security.md
│   └── operations.md
│
├── diagrams/
│   ├── topology.drawio
│   └── topology.md
│
├── configs/
│   ├── cisco/
│   ├── huawei/
│   ├── fortigate/
│   └── paloalto/
│
├── labs/
│   ├── LAB-00-setup.md
│   ├── LAB-01-vlan.md
│   ├── LAB-02-ospf.md
│   ├── LAB-03-bgp.md
│   ├── LAB-04-vrf.md
│   ├── LAB-05-firewall.md
│   └── LAB-06-sdwan-ipsec.md
│
├── ansible/
│   ├── inventory/
│   ├── group_vars/
│   ├── host_vars/
│   ├── playbooks/
│   └── templates/
│
├── python/
│   ├── scripts/
│   └── requirements.txt
│
├── terraform/
│   ├── aws/
│   └── azure/
│
└── tests/
```

---

# 🔄 NetDevOps Workflow

The project follows a simplified NetDevOps lifecycle:

```text
        DESIGN
          |
          v
      DOCUMENT
          |
          v
       DEVELOP
          |
          v
        TEST
          |
          v
       REVIEW
          |
          v
        DEPLOY
          |
          v
       MONITOR
          |
          v
       IMPROVE
          |
          +------------+
                       |
                       v
                    Git/GitHub
```

---

# 🔐 Security Principles

This project follows fundamental security principles:

* Least Privilege
* Network Segmentation
* Defense in Depth
* Secure Management
* Configuration Backup
* Change Management
* Logging and Monitoring
* Secure Credential Management
* Regular Hardening
* Vulnerability Management

### ⚠️ Credentials

**Never commit real credentials to this repository.**

Do not upload:

```text
Passwords
API Tokens
Private Keys
VPN PSKs
SNMP Communities
Cloud Credentials
Production Configurations
Customer Information
```

Use mechanisms such as:

* Ansible Vault
* GitHub Secrets
* Environment Variables
* Secure Credential Managers

---

# 📈 Future Improvements

The laboratory will evolve continuously.

Planned implementations:

* [ ] IPv6
* [ ] MPLS L3VPN
* [ ] Segment Routing
* [ ] EVPN/VXLAN
* [ ] BFD
* [ ] QoS
* [ ] Cisco SD-WAN
* [ ] Fortinet SD-WAN
* [ ] Palo Alto
* [ ] Cisco ACI
* [ ] Network APIs
* [ ] RESTCONF
* [ ] NETCONF
* [ ] YANG
* [ ] CI/CD
* [ ] GitHub Actions
* [ ] Automated testing
* [ ] Zabbix
* [ ] Grafana
* [ ] AWS Networking
* [ ] Azure Networking

---

# 🎓 Skills Demonstrated

This project demonstrates practical knowledge in:

**Network Engineering**

* Enterprise Architecture
* Routing & Switching
* BGP
* OSPF
* MPLS
* SD-WAN
* VPN
* IPv4/IPv6
* Network Design

**Cybersecurity**

* Firewalls
* Network Segmentation
* VPN
* Hardening
* Security Policies
* Secure Management

**Automation**

* Python
* Ansible
* Terraform
* APIs
* Git
* GitHub
* CI/CD
* NetDevOps

**Operations**

* Monitoring
* Troubleshooting
* Documentation
* Change Management
* Configuration Management

---

# 👨‍💻 Author

**André — Telecommunications & Network Engineer**

Focus areas:

* Enterprise Networks
* Telecommunications
* Network Architecture
* Cybersecurity
* SD-WAN
* MPLS
* Network Automation
* NetDevOps
* Infrastructure

---

# ⭐ Project Status

🚧 **Under Development**

This laboratory is continuously evolving as new technologies, architectures and automation scenarios are implemented.

---

## Disclaimer

This repository is intended for educational, laboratory and portfolio purposes.

All configurations should be tested in an isolated environment before being considered for production use.
