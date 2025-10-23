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

## 4. Teste e Validação Final

* **Método:** O fluxo de trabalho foi validado via **Teste Manual Síncrono** na console Lambda, simulando o evento de upload do S3.
* **Resultado:** O teste retornou **SUCESSO** no log do CloudWatch, provando que a **IAM Role (`Lambda-Orchestrator-Role`)** está configurada corretamente e a lógica de orquestração da Função Lambda foi executada com êxito.

### 4.1 Prova Final de Execução (Teste de Sucesso)

A validação final ocorreu via log do CloudWatch, provando que a Função Lambda executou com sucesso a simulação de orquestração do EC2:

![Log de Sucesso da Invocação](prova_sucesso_cloudwatch.png)

---

## 🖼️ Visualização da Arquitetura

O diagrama de arquitetura, criado com o Draw.io, ilustra visualmente o fluxo de processamento de dados orientado a eventos do laboratório:

* **Fluxo:** `S3 (Trigger)` ➡️ `Lambda` ➡️ `DynamoDB`.

![Diagrama da Arquitetura Serverless](diagrama_serverless.png)

---

## 📚 Documentação Técnica Detalhada

O detalhamento das configurações, comandos e conceitos teóricos está organizado na pasta `/docs`:

* [Conceitos Fundamentais da Cloud e Modelos de Serviço](doc/conceitos-cloud-base.md)
* [Segurança da Conta Root e Práticas IAM](doc/iam-security-root.md)
* [Gerenciamento de Identidades e Políticas IAM](doc/iam-identity-management.md)
* [Infraestrutura EC2, EBS, IP Elástico e Monitoramento](doc/ec2-iaas.md)
* [S3, Lambda e o Fluxo de Integração Serverless](doc/s3-lambda-integracao.md)
* [Comandos Essenciais: CLI, SSH e Configuração de Grupos](doc/automacao-cli-e-grupos.md)

---


meu codigo atual
