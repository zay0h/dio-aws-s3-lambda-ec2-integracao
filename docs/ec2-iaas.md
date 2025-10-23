# 💻 Infraestrutura EC2 (IaaS), EBS e Monitoramento

O Amazon EC2 (Elastic Compute Cloud) representa o modelo **IaaS (Infraestrutura como Serviço)**, oferecendo o controle total sobre o servidor virtual.

## 1. Gerenciamento do Ciclo de Vida da Instância

* **Stopped (Parada):** A instância está desligada. Você **paga pelo armazenamento (EBS)**. O IP Público dinâmico é perdido.
* **Terminated (Encerrada):** A instância é excluída permanentemente. O Volume EBS padrão é deletado (se configurado). **Todos os custos param**.

## 2. Componentes Essenciais

### A. Imagem de Máquina da Amazon (AMI)
* É a imagem pré-configurada da máquina virtual (SO, aplicações).
* É o "molde" a partir do qual a instância é lançada.

### B. Volumes EBS (Elastic Block Store)
* São os discos de armazenamento persistente.
* **Finalidade:** Garante a **persistência dos dados**. O Volume EBS é independente da instância EC2.
* **Snapshots:** São cópias pontuais (*point-in-time*) dos Volumes EBS, essenciais para backup e recuperação.

### C. Elastic IP (IP Elástico)
* É um endereço IP público estático e reservado.
* **Importância:** Crucial para instâncias que precisam ser acessadas de forma consistente por um endereço fixo.

## 3. Monitoramento e Otimização de Custos

### A. Amazon CloudWatch
* Serviço de monitoramento que coleta métricas de desempenho (uso de CPU, rede).
* **Prática:** Configurar alarmes para notificar sobre picos de uso (resiliência operacional) ou ociosidade (otimização de custos).

### B. Security Groups (Grupos de Segurança)
* Atuam como um **firewall virtual** no nível da instância, controlando o tráfego de entrada e saída.
* **Regra de Ouro:** Acesso via SSH (porta 22) deve ser estrito (restrito ao seu IP).
