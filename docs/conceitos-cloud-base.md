# 📚 Conceitos Fundamentais da AWS e Cloud Computing

## 1. História e Estrutura Global

* **História:** A AWS nasceu em 2006 da necessidade interna da Amazon por uma infraestrutura de TI mais flexível, inaugurando a era da computação em nuvem.
* **Infraestrutura:** A AWS opera em uma rede global organizada em **Regiões** e **Zonas de Disponibilidade (AZs)**, garantindo resiliência e baixa latência global.

### Regiões vs. Zonas de Disponibilidade (AZs)

| Conceito | Foco Principal |
| :--- | :--- |
| **Regiões** | **Latência** (proximidade do usuário), **Conformidade** e **Custo**. |
| **AZs** | **Alta Disponibilidade** e **Tolerância a Falhas** (Data Centers separados fisicamente). |

## 2. Modelos de Serviço e Custo (IaaS, PaaS, SaaS)

| Modelo | O que o Provedor Gerencia | O que o Usuário Gerencia | Exemplo Prático |
| :--- | :--- | :--- | :--- |
| **SaaS (Use)** | Tudo (Software pronto) | Uso da Aplicação | Gmail, Netflix |
| **PaaS (Construa)** | Ambiente de execução, SO, Infraestrutura | Código e Aplicações | **AWS Lambda** |
| **IaaS (Migre)** | Infraestrutura básica (Rede, Servidores Virtuais) | SO, Aplicações, Dados | **Amazon EC2** |

* **Modelo de Custo:** A AWS utiliza o **OPEX (Despesas Operacionais)** (pagamento por uso).

## 3. Modelo de Responsabilidade Compartilhada

* **Responsabilidade da AWS:** É a **Segurança DA Nuvem** (Hardware, Data Centers).
* **Responsabilidade do CLIENTE:** É a **Segurança NA Nuvem** (Dados, Criptografia, Permissões **IAM**, Configuração de Rede **Security Groups**).
