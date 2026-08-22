# 🚀 Enterprise Network & NetDevOps Lab

![Network Engineering](https://img.shields.io/badge/Network-Engineering-blue)
![NetDevOps](https://img.shields.io/badge/NetDevOps-Automação-green)
![Ansible](https://img.shields.io/badge/Ansible-Automação-red)
![Python](https://img.shields.io/badge/Python-Automação-yellow)
![Terraform](https://img.shields.io/badge/Terraform-IaC-purple)
![GitHub](https://img.shields.io/badge/GitHub-Versionamento-black)

## 📌 Sobre o Projeto

Este repositório apresenta um **laboratório completo de Redes Corporativas e NetDevOps**, desenvolvido para simular uma infraestrutura Enterprise real.

O projeto integra conceitos de:

* Engenharia de Redes
* Routing e Switching
* Segurança de Redes
* Firewall
* SD-WAN
* MPLS
* Automação
* NetDevOps
* Infrastructure as Code
* Monitoramento
* Cloud Networking

O laboratório será desenvolvido utilizando plataformas como **PNETLab, EVE-NG ou GNS3**, permitindo reproduzir os cenários em um ambiente controlado.

---

# 🎯 Objetivos

O principal objetivo deste projeto é desenvolver e documentar uma infraestrutura corporativa completa, aplicando boas práticas de engenharia de redes.

### Objetivos técnicos

* Projetar uma arquitetura Enterprise.
* Implementar VLANs e segmentação de rede.
* Implementar Routing e Switching.
* Configurar OSPF.
* Configurar BGP.
* Implementar VRF.
* Estudar e implementar MPLS.
* Implementar VPN IPsec.
* Implementar SD-WAN.
* Configurar firewalls.
* Implementar políticas de segurança.
* Automatizar tarefas utilizando Ansible.
* Desenvolver scripts utilizando Python.
* Utilizar Terraform para Infrastructure as Code.
* Implementar monitoramento com Zabbix e Grafana.
* Utilizar Git e GitHub para controle de versões.
* Aplicar conceitos de NetDevOps e CI/CD.
* Documentar toda a infraestrutura.

---

# 🏗️ Arquitetura da Rede

```text
                              INTERNET
                                  |
                            +-----------+
                            |    ISP    |
                            +-----+-----+
                                  |
                           +------+------+
                           |  FIREWALL  |
                           | FortiGate /|
                           | Palo Alto  |
                           +------+------+
                                  |
                   +--------------+--------------+
                   |                             |
              +----+----+                   +----+----+
              |  CORE1  |===================|  CORE2  |
              +----+----+       OSPF        +----+----+
                   |                             |
                   |                             |
              +----+----+                   +----+----+
              |   DATA   |                   |    HQ    |
              |  CENTER  |                   |  USERS   |
              +----+----+                   +----+----+
                   |                             |
               SERVIDORES                     SD-WAN
                                                |
                              +-----------------+----------------+
                              |                                  |
                         +----+----+                        +----+----+
                         |FILIAL 01|                        |FILIAL 02|
                         +---------+                        +---------+
```

---

# 🌐 Tecnologias

## Routing

* IPv4
* IPv6
* OSPF
* BGP
* VRF
* Redistribuição de rotas
* Políticas de roteamento

## Switching

* VLAN
* Trunk
* STP
* EtherChannel
* Inter-VLAN Routing
* Switching Layer 2
* Switching Layer 3

## WAN

* MPLS
* IPsec
* SD-WAN
* Failover
* QoS
* Políticas de roteamento

## Segurança

* FortiGate
* Palo Alto
* Firewall Policies
* NAT
* VPN
* Segmentação
* Hardening
* Controle de acesso
* Princípio do menor privilégio

## Automação

* Git
* GitHub
* Ansible
* Python
* Terraform
* APIs
* Infrastructure as Code
* CI/CD
* NetDevOps

## Monitoramento

* Zabbix
* Grafana
* SNMP
* Syslog
* ICMP
* Telemetria

## Plataformas de Laboratório

* PNETLab
* EVE-NG
* GNS3

---

# 📊 Plano de Endereçamento

| Segmento         | VLAN | Rede            | Finalidade                     |
| ---------------- | ---: | --------------- | ------------------------------ |
| Management       |   10 | 10.10.10.0/24   | Gerenciamento                  |
| Usuários         |   20 | 10.10.20.0/24   | Usuários HQ                    |
| Servidores       |   30 | 10.10.30.0/24   | Data Center                    |
| Voz              |   40 | 10.10.40.0/24   | Telefonia IP                   |
| Serviços de Rede |   50 | 10.10.50.0/24   | DNS/DHCP/NTP                   |
| Filial 01        |  110 | 10.20.10.0/24   | Usuários                       |
| Filial 02        |  120 | 10.30.10.0/24   | Usuários                       |
| Loopbacks        |    — | 10.255.255.0/24 | Identificação dos equipamentos |
| Links P2P        |    — | 10.255.0.0/24   | Infraestrutura de roteamento   |

> As redes utilizadas neste projeto são destinadas exclusivamente ao laboratório.

---

# 🔢 Endereçamento das Loopbacks

| Equipamento | Loopback         |
| ----------- | ---------------- |
| R-CORE1     | 10.255.255.1/32  |
| R-CORE2     | 10.255.255.2/32  |
| R-EDGE1     | 10.255.255.3/32  |
| R-FILIAL01  | 10.255.255.11/32 |
| R-FILIAL02  | 10.255.255.12/32 |

As loopbacks serão utilizadas principalmente para:

* Router-ID;
* BGP;
* OSPF;
* Gerenciamento;
* Monitoramento;
* Identificação dos equipamentos.

---

# 🧪 Laboratórios

## LAB-00 — Preparação do Ambiente

Preparação da infraestrutura no PNETLab/EVE-NG.

### Atividades

* Criar os equipamentos.
* Definir nomes dos dispositivos.
* Configurar gerenciamento.
* Configurar endereçamento.
* Configurar loopbacks.
* Realizar hardening básico.
* Criar a documentação inicial.

---

# LAB-01 — VLAN e Inter-VLAN Routing

Implementação da segmentação da rede corporativa.

### VLANs

```text
VLAN 10  → Management
VLAN 20  → Usuários
VLAN 30  → Servidores
VLAN 40  → Voz
VLAN 50  → Serviços
```

### Atividades

* Criar VLANs.
* Configurar portas Access.
* Configurar Trunks.
* Configurar SVI.
* Configurar gateways.
* Implementar Inter-VLAN Routing.
* Validar conectividade.
* Implementar segmentação.

---

# LAB-02 — OSPF

Implementação do protocolo OSPF no Core.

### Objetivos

* Configurar OSPF Area 0.
* Definir Router-ID.
* Estabelecer vizinhanças.
* Anunciar loopbacks.
* Analisar tabela de roteamento.
* Trabalhar com custo OSPF.
* Simular falhas.
* Validar convergência.

### Validações

```text
Vizinhança OSPF
Tabela de rotas
Estado das interfaces
Reachability
Convergência
```

---

# LAB-03 — BGP

Implementação de conectividade entre a empresa e um ISP.

### Autonomous Systems

```text
Empresa → AS 65001
ISP     → AS 65100
```

### Atividades

* Configurar eBGP.
* Anunciar prefixos corporativos.
* Criar Prefix Lists.
* Criar políticas de roteamento.
* Filtrar rotas.
* Trabalhar com Local Preference.
* Trabalhar com AS Path.
* Analisar tabela BGP.

### Objetivo

Implementar uma conexão com ISP seguindo boas práticas de segurança e controle de rotas.

---

# LAB-04 — VRF

Implementação de segmentação utilizando VRF.

### Objetivos

* Criar VRFs.
* Associar interfaces.
* Criar tabelas de roteamento independentes.
* Isolar ambientes.
* Implementar Route Leaking quando necessário.
* Validar isolamento entre redes.

---

# LAB-05 — Firewall

Implementação da arquitetura de segurança.

### Zonas

```text
             INTERNET
                 |
              UNTRUST
                 |
              FIREWALL
          /       |       \
      TRUST     SERVER    MGMT
```

### Tecnologias

* FortiGate
* Palo Alto

### Atividades

* Criar objetos.
* Criar grupos de objetos.
* Criar Security Policies.
* Configurar NAT.
* Configurar VPN.
* Configurar logs.
* Implementar regras de menor privilégio.
* Implementar hardening.
* Validar acessos permitidos e bloqueados.

---

# LAB-06 — SD-WAN + IPsec

Implementação de uma arquitetura WAN corporativa.

```text
                       HQ
                        |
                 +------+------+
                 |   SD-WAN   |
                 +------+------+
                    /       \
                   /         \
              INTERNET      MPLS
                 /             \
          FILIAL 01          FILIAL 02
```

### Atividades

* Criar túneis IPsec.
* Simular múltiplos links.
* Configurar SLA.
* Configurar failover.
* Definir prioridade de aplicações.
* Criar políticas de encaminhamento.
* Simular falha de WAN.
* Validar recuperação automática.

---

# LAB-07 — Ansible

Automação da infraestrutura de rede.

### Objetivos

* Criar inventário.
* Coletar informações.
* Executar comandos.
* Fazer backup.
* Aplicar configurações.
* Utilizar templates.
* Utilizar variáveis.
* Utilizar Ansible Vault.

Estrutura:

```text
ansible/
├── inventory/
├── group_vars/
├── host_vars/
├── playbooks/
└── templates/
```

---

# LAB-08 — Python

Automação utilizando Python.

### Projetos

```text
Validação de interfaces
       ↓
Validação de BGP
       ↓
Validação de OSPF
       ↓
Teste de conectividade
       ↓
Backup de configuração
       ↓
Geração de relatório
```

---

# LAB-09 — Terraform

Implementação de Infrastructure as Code.

### Ambientes

```text
terraform/
├── aws/
└── azure/
```

### Futuras implementações

* AWS VPC
* Azure VNet
* Subnets
* Routing
* Security Groups
* NSG
* VPN
* Cloud Networking

---

# LAB-10 — Monitoramento

Implementação de observabilidade da infraestrutura.

### Ferramentas

* Zabbix
* Grafana
* SNMP
* Syslog

### Monitoramento

```text
CPU
Memória
Interfaces
Tráfego
Latência
Packet Loss
BGP
OSPF
VPN
Firewall
Disponibilidade
```

---

# 📁 Estrutura do Repositório

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

# 🔄 Fluxo NetDevOps

O projeto seguirá um ciclo de desenvolvimento semelhante ao utilizado em ambientes corporativos:

```text
              PROJETO
                 |
                 ↓
           DOCUMENTAÇÃO
                 |
                 ↓
            DESENVOLVIMENTO
                 |
                 ↓
               TESTE
                 |
                 ↓
              REVIEW
                 |
                 ↓
              DEPLOY
                 |
                 ↓
            MONITORAMENTO
                 |
                 ↓
             MELHORIA
                 |
                 └──────────→ Git / GitHub
```

---

# 🔐 Segurança

Este laboratório seguirá princípios de segurança como:

* Princípio do menor privilégio.
* Segmentação de rede.
* Defesa em profundidade.
* Gerenciamento seguro.
* Controle de acesso.
* Hardening.
* Backup de configurações.
* Monitoramento.
* Gestão de vulnerabilidades.
* Controle de mudanças.

## ⚠️ Credenciais

**Nunca inserir credenciais reais no GitHub.**

Não publicar:

```text
Senhas
Tokens
Chaves privadas
PSK de VPN
Credenciais de Cloud
SNMP Communities reais
Configurações de produção
Informações de clientes
```

Utilizar:

* Ansible Vault
* GitHub Secrets
* Variáveis de ambiente
* Cofres de credenciais

---

# 📈 Roadmap

* [x] Arquitetura inicial
* [x] Plano de endereçamento
* [ ] LAB-00 — Preparação
* [ ] LAB-01 — VLAN
* [ ] LAB-02 — OSPF
* [ ] LAB-03 — BGP
* [ ] LAB-04 — VRF
* [ ] LAB-05 — Firewall
* [ ] LAB-06 — SD-WAN/IPsec
* [ ] LAB-07 — Ansible
* [ ] LAB-08 — Python
* [ ] LAB-09 — Terraform
* [ ] LAB-10 — Zabbix/Grafana
* [ ] IPv6
* [ ] MPLS L3VPN
* [ ] Segment Routing
* [ ] EVPN/VXLAN
* [ ] Cisco ACI
* [ ] RESTCONF
* [ ] NETCONF
* [ ] YANG
* [ ] GitHub Actions
* [ ] CI/CD
* [ ] Testes automatizados

---

# 🎓 Competências Demonstradas

Este projeto demonstra conhecimentos práticos em:

### Engenharia de Redes

* Arquitetura Enterprise
* Routing
* Switching
* BGP
* OSPF
* MPLS
* SD-WAN
* VPN
* IPv4/IPv6
* Network Design

### Segurança

* Firewall
* FortiGate
* Palo Alto
* NAT
* VPN
* Segmentação
* Hardening
* Security Policies

### Automação

* Python
* Ansible
* Terraform
* APIs
* Git
* GitHub
* CI/CD
* NetDevOps

### Operação

* Monitoramento
* Troubleshooting
* Documentação
* Controle de mudanças
* Gerenciamento de configuração

---

# 👨‍💻 Autor

**André — Engenheiro de Telecomunicações, Redes e TI**

Áreas de atuação:

* Engenharia de Redes
* Telecomunicações
* Network Architecture
* Cybersecurity
* SD-WAN
* MPLS
* Network Automation
* NetDevOps
* Infrastructure

---

# 🚧 Status do Projeto

**Em desenvolvimento**

Este laboratório será evoluído continuamente com novas arquiteturas, tecnologias, automações e cenários de troubleshooting.

---

## ⚠️ Aviso

Este projeto possui finalidade **educacional, de laboratório e portfólio profissional**.

Todas as configurações devem ser testadas em ambiente isolado antes de serem utilizadas em ambientes de produção.
