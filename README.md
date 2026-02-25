🏗️ Terraform + Ansible Infrastructure Automation
📖 Technical Overview

Este projeto implementa automação de infraestrutura utilizando Terraform para provisionamento de recursos e Ansible para configuração e gerenciamento de servidores, seguindo os princípios de Infrastructure as Code (IaC) e práticas modernas de DevOps.

A arquitetura separa claramente responsabilidades:

Terraform → Provisioning Layer (Day 0)

Ansible → Configuration Management Layer (Day 1 / Day 2)

Terraform é responsável pela criação e gerenciamento do ciclo de vida da infraestrutura utilizando arquivos declarativos em HCL (HashiCorp Configuration Language), enquanto o Ansible executa automação procedural para configuração do sistema operacional, instalação de pacotes e deploy de aplicações.

🧠 Infrastructure as Code (IaC)

Infrastructure as Code consiste em gerenciar e provisionar infraestrutura por meio de arquivos de configuração versionáveis em vez de processos manuais ou interfaces gráficas, garantindo consistência, rastreabilidade e automação do ambiente.

Principais características aplicadas neste projeto:

Declarative Infrastructure Definition

Version Control Integration

Idempotent Configuration

Automated Provisioning

Environment Reproducibility

⚙️ Workflow Architecture

Fluxo técnico da automação:

Developer → Terraform Plan → Terraform Apply → Infrastructure Provisioned
                                                  ↓
                                           Dynamic Inventory / SSH
                                                  ↓
                                             Ansible Playbook
                                                  ↓
                                         Configured Environment
Etapas:

Terraform inicializa providers e backend (terraform init)

Terraform calcula mudanças de estado (terraform plan)

Recursos são provisionados (terraform apply)

Outputs são utilizados como entrada para Ansible

Ansible conecta via SSH (agentless) e executa playbooks

Ambiente final é configurado automaticamente

Terraform mantém o state file, que representa o estado atual da infraestrutura e permite detectar drift e aplicar mudanças incrementais.

🔗 Integração Terraform + Ansible

A integração entre as ferramentas pode ocorrer através de:

Provisioners (remote-exec / local-exec)

Dynamic inventory

Outputs do Terraform

Scripts de automação

Pipelines CI/CD

Terraform é otimizado para provisionamento de infraestrutura “from zero to ready”, enquanto Ansible é ideal para configuração contínua e operações pós-deploy.

🧱 Architecture Components

Exemplo de recursos normalmente provisionados:

Virtual Machines / Cloud Instances

Network Configuration

Security Groups / Firewall Rules

Storage Resources

SSH Access Configuration

Após provisionamento:

Package Installation

System Hardening

Application Deployment

Service Configuration

Environment Setup

🛠️ Technologies Used

Terraform (HCL)

Ansible (YAML)

Linux

SSH

Cloud Infrastructure

Infrastructure as Code

Configuration Management

📂 Repository Structure
Terraform_Ansible/
│
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
│   └── provider.tf
│
├── ansible/
│   ├── inventory
│   ├── playbook.yml
│   └── roles/
│
└── README.md
