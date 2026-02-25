Terraform + Ansible Automation Project
🚀 Overview

Este repositório demonstra a automação completa de infraestrutura utilizando Terraform e Ansible, seguindo os princípios de Infrastructure as Code (IaC) e práticas modernas de DevOps.

O objetivo do projeto é provisionar recursos de infraestrutura de forma automatizada e, em seguida, realizar a configuração dos servidores e aplicações utilizando Ansible.

A combinação das duas ferramentas permite uma automação ponta a ponta:

Terraform → Provisionamento da infraestrutura

Ansible → Configuração e gerenciamento dos servidores

Terraform é amplamente utilizado para definir recursos em código declarativo e gerenciar o ciclo de vida da infraestrutura, enquanto o Ansible é focado em automação de configuração e deploy de aplicações.

🧠 Infrastructure as Code (IaC)

Infrastructure as Code é uma abordagem que permite gerenciar infraestrutura utilizando arquivos de configuração em vez de processos manuais, garantindo consistência, automação e versionamento do ambiente.

Benefícios:

Ambientes reproduzíveis

Automação de deploy

Controle de versão

Escalabilidade

Redução de erros humanos

🏗️ Architecture

Fluxo de automação:

Terraform → Criação da infraestrutura (VM, rede, cloud resources)
        ↓
Ansible → Configuração do sistema operacional e aplicações

Terraform cria os recursos e pode acionar o Ansible para finalizar a configuração, formando um workflow completo de automação.

🛠️ Technologies Used

Terraform

Ansible

Linux

Cloud Infrastructure

SSH

YAML

HCL (HashiCorp Configuration Language)

📂 Project Structure (Example)
Terraform_Ansible/
│
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   └── outputs.tf
│
├── ansible/
│   ├── inventory
│   └── playbook.yml
│
└── README.md
⚙️ How It Works

1️⃣ Terraform provisiona a infraestrutura
2️⃣ Outputs são utilizados pelo Ansible
3️⃣ Ansible configura servidores automaticamente
4️⃣ Ambiente pronto para uso

Essa abordagem permite automação completa desde a criação até a configuração do ambiente.

🎯 Use Cases

Deploy automático de ambientes cloud

Configuração de servidores Linux

Provisionamento de infraestrutura DevOps

Laboratórios de estudo

Ambientes de desenvolvimento e produção

📈 DevOps Skills Demonstrated

Infrastructure as Code (IaC)

Automação de Provisionamento

Configuration Management

Integração Terraform + Ansible

Cloud Automation

Linux Administration
