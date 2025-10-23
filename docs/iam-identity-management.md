# 🔑 Gerenciamento de Identidades e Acesso (IAM)

O **IAM (Identity and Access Management)** é o serviço central da AWS para gerenciar e controlar quem pode acessar os recursos da plataforma e sob quais condições. É a base para implementar o **Princípio do Mínimo Privilégio**.

## 1. Funções Essenciais do IAM

O IAM permite que a segurança seja gerenciada de forma granular através de:

* **Usuários:** Entidades individuais (pessoas) que interagem com a AWS.
* **Grupos:** Coleções de usuários que compartilham um conjunto de permissões.
* **Roles (Funções):** Identidades que podem ser assumidas por serviços AWS (como a Lambda) ou por usuários. **Cruciais para conceder permissão a serviços.**
* **Políticas:** Documentos que definem as permissões exatas (o que pode ser feito, em qual recurso e sob quais condições).

## 2. O Papel das Políticas de Permissões

As políticas de permissões no IAM são o que definem o nível de acesso. Elas são cruciais para:

* **Controle Fino:** Determinar o que usuários e grupos podem acessar e fazer em diferentes serviços da AWS.
* **Princípio do Mínimo Privilégio:** Garantir que cada identidade (Usuário ou Role) tenha o **mínimo de permissões** necessárias para executar sua função, reduzindo a superfície de ataque.

## 3. IAM Identity Center (Antigo AWS SSO)

O IAM Identity Center simplifica o gerenciamento de acesso para múltiplos usuários, permitindo a autenticação centralizada e o acesso único (Single Sign-On - SSO) a várias contas AWS e aplicativos de terceiros.
