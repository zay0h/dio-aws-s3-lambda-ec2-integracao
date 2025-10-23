# ☁️ DIO Lab: Integração de Serviços AWS (S3, Lambda e EC2)

## 📄 Descrição do Projeto

Este repositório documenta o laboratório prático de integração de serviços AWS, simulando um fluxo de processamento de dados. O projeto foi estruturado para consolidar o conhecimento teórico e prático em **Infraestrutura (EC2), Armazenamento (S3) e Computação Serverless (Lambda)**, com foco em segurança IAM e automação CLI.

---

## 💡 Principais Insights e Aprendizados

### 1. Visão Holística de Serviços (IaaS vs. PaaS)

Compreendi o papel estratégico de cada serviço na arquitetura de nuvem:
* **IaaS (EC2):** Proporciona controle total do S.O., sendo ideal para processamento pesado.
* **PaaS/FaaS (Lambda):** Serviço gerenciado, perfeito para orquestrar o fluxo de dados sem a carga de gerenciar servidores.
* **EBS, IP Elástico, Security Groups:** Componentes vitais para a persistência de dados, acesso e segurança da infraestrutura EC2.

### 2. Fundamentos Essenciais da Segurança

A segurança é central, focando no princípio do mínimo privilégio:
* **IAM Roles:** Essenciais para autorizar a comunicação entre serviços (ex: a Lambda precisa de permissão para iniciar o EC2).
* **Conta Root:** Restrição do uso apenas para tarefas críticas, com MFA obrigatório.
* **Security Groups:** Atuam como *firewalls virtuais* no nível da instância, sendo a primeira linha de defesa.

### 3. Gerenciamento e Automação

* **AWS CLI:** Utilizado para automatizar tarefas de IAM (criação de usuários/grupos) via linha de comando, mostrando eficiência em escala.
* **Ciclo de Vida EC2:** A distinção entre `Stop` e `Terminate` é crucial para a otimização de custos e a persistência do volume EBS.
* **Monitoramento:** A importância do CloudWatch para manter a resiliência operacional e evitar desperdício de recursos.

---

## 📚 Documentação Técnica Detalhada

O detalhamento das configurações, comandos e conceitos teóricos está organizado na pasta `/docs`:

* [Conceitos Fundamentais da Cloud e Modelos de Serviço](docs/conceitos-cloud-base.md)
* [Segurança da Conta Root e Práticas IAM](docs/iam-security-root.md)
* [Gerenciamento de Identidades e Políticas IAM](docs/iam-identity-management.md)
* [Infraestrutura EC2, EBS, IP Elástico e Monitoramento](docs/ec2-iaas.md)
* [S3, Lambda e o Fluxo de Integração Serverless](docs/s3-lambda-integracao.md)
* [Comandos Essenciais: CLI, SSH e Configuração de Grupos](docs/automacao-cli-e-grupos.md)

---
