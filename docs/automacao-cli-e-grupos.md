# ⚙️ Comandos Essenciais, Automação e Rede

Este guia foca nos comandos práticos de acesso e nas práticas de configuração de segurança de rede.

## 1. Automação e Gerenciamento via AWS CLI

A utilização da **AWS Command Line Interface (CLI)** é essencial para automação e gestão em escala.

* **Comando de Configuração:** `aws configure` (Utilizado para fornecer as credenciais de acesso).
* **Comando de Automação:** `bash scriptIAM.sh usuarios.csv` (Executa scripts para criar usuários/grupos a partir de um arquivo CSV, demonstrando eficiência).

## 2. Acesso Seguro à Instância EC2 (SSH)

O acesso via SSH (Secure Shell) utiliza o par de chaves e exige permissões corretas no arquivo:

* **1. Permissão da Chave:** `chmod 400 nome-da-chave.pem` (Define a permissão de leitura exclusiva para a chave privada).
* **2. Conexão SSH:** `ssh -i nome-da-chave.pem usuário@IP-Público-EC2` (Inicia a sessão segura usando a chave).

## 3. Configuração de Rede: Security Groups (SGs)

O **Security Group** é o firewall virtual que controla o tráfego da instância EC2.

* **Regra de Entrada (Inbound):** Define o tráfego que é permitido **acessar** a instância.
    * **SSH:** Porta **TCP 22** deve ser aberta.
    * **Melhor Prática:** Restringir o IP de origem ao máximo (evitar `0.0.0.0/0`).
* **Regra de Saída (Outbound):** Define para onde o tráfego da instância pode ir.
