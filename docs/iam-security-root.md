# 🔒 Segurança e Gestão da Conta Root (IAM)

Este módulo abordou as práticas essenciais de segurança para a conta raiz da AWS (Root User).

## 1. Princípio do Mínimo Privilégio na Conta Root

A conta **Root** deve ter seu uso **restrito** apenas às tarefas essenciais. Para o trabalho diário, é obrigatório criar e usar um usuário IAM (Identity and Access Management) com permissões administrativas.

### Tarefas Exclusivas do Usuário Root:

* Gerenciamento e encerramento da conta.
* Alteração da senha da conta Root.
* Visualização de faturas e gerenciamento de métodos de pagamento.
* Habilitar MFA (Autenticação Multifactor) para o usuário Root.
* Restaurar permissões do IAM em casos de emergência.

## 2. Práticas Fundamentais de Segurança para a Conta Root

A segurança da conta Root é a fundação de toda a segurança na nuvem. As seguintes práticas devem ser implementadas imediatamente:

1.  **Habilitar MFA (Autenticação Multifator):** Configure e habilite a MFA imediatamente.
2.  **Criação e Armazenamento Seguro:** As credenciais da conta Root devem ser armazenadas de forma extremamente segura e **offline**.
3.  **Confidencialidade Estrita:** **Jamais** compartilhe as credenciais da conta Root.
4.  **Delegar Operações:** Crie e utilize um **usuário IAM com permissões administrativas** para todas as operações diárias.
