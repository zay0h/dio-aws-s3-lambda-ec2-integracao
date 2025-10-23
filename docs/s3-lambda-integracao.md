# 🔗 S3, Lambda e o Fluxo de Integração Serverless

Esta seção detalha os serviços **Serverless** (Lambda) e de **Armazenamento** (S3), e como eles se integram com o EC2 para formar a arquitetura completa.

## 1. Amazon S3 (Simple Storage Service)

O S3 é um serviço de armazenamento de objetos altamente durável e escalável.

* **Função no Projeto:** Serve como o ponto de entrada (Bucket de Entrada) para os dados, atuando como o **Gatilho de Eventos** para a função Lambda.
* **Conceito-Chave:** O S3 armazena objetos em **Buckets**.

## 2. AWS Lambda (Function as a Service - FaaS)

A Lambda é o coração do modelo de **PaaS** (ou FaaS) no nosso projeto, atuando como a orquestradora do fluxo.

* **Função no Projeto:** Executar o código de processamento inicial do evento sem a necessidade de gerenciar servidores.
* **Gatilho:** A Lambda é configurada para ser acionada imediatamente após um evento de **`s3:ObjectCreated`** no Bucket de Entrada.

## 3. O Fluxo de Integração da Arquitetura

O fluxo completo demonstra a elasticidade e a separação de responsabilidades na nuvem:

1.  **Ação do Usuário:** Um usuário faz o Upload de um arquivo no **S3 Bucket**.
2.  **Disparo:** O evento de `ObjectCreated` é enviado ao **AWS Lambda**.
3.  **Início do Processamento Pesado:** A Lambda utiliza sua **IAM Role** (Permissão) para iniciar a **Instância EC2**, delegando a tarefa que exige maior poder computacional.
