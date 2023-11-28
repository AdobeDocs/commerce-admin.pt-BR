---
title: Funções e permissões da empresa
description: Saiba mais sobre as funções e permissões que um administrador de empresa pode aplicar aos usuários da empresa, permitindo vários níveis de acesso a informações e recursos de pedidos.
exl-id: 9fe20d6a-2c9c-4618-a395-805d64dcf0de
feature: B2B, Companies, Roles/Permissions
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Funções e permissões da empresa

As funções para usuários da empresa são configuradas com vários níveis de permissão para acessar informações e recursos de vendas. Por padrão, o administrador da empresa é um _superusuário_ com permissões totais. A variável [Acesso negado](../content-design/pages.md#access-denied) será exibida se o usuário não tiver permissão para acessar a página.

![Página Funções e permissões com a função padrão](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

O sistema tem uma função Usuário Padrão predefinida, que pode ser usada _como está_ ou modifique para atender às suas necessidades. É possível criar quantas funções forem necessárias para corresponder à estrutura da empresa e às responsabilidades organizacionais, como as seguintes:

- **Usuário padrão** — O usuário padrão tem acesso total a atividades relacionadas a vendas e cotações e acesso somente para visualização a informações de perfil e crédito da empresa.

- **Comprador Sênior** — Um comprador sênior pode ter acesso a todos os recursos de vendas e cotações e ter permissões somente para visualização para o Perfil da empresa, Usuário e equipes, Informações de pagamento e Crédito da empresa.

- **Comprador assistente** — Um adquirente assistente pode ter permissão para efetuar um pedido utilizando _Check-out com Cotação_ e para exibir pedidos, cotações e informações no perfil da empresa.

## Gerenciar funções e permissões

1. O administrador da empresa faz logon em sua conta de armazenamento.

1. No painel esquerdo, escolhe **[!UICONTROL Roles and Permissions]**.

1. Conclui qualquer uma das tarefas a seguir.

### Criar uma função

1. Cliques **[!UICONTROL Add New Role]**.

   ![Adicionar nova função](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"}

1. Insere um descritivo **[!UICONTROL Role Name]**.

1. Em _[!UICONTROL Role Permissions]_, executa um dos seguintes procedimentos:

   - Marca a caixa de seleção de cada recurso ou atividade que os usuários com a função atribuída têm permissão para acessar.

   - Seleciona o **[!UICONTROL All]** e desmarca a caixa de seleção de cada recurso ou atividade que os usuários atribuídos à função não têm permissão para acessar.

1. Cliques **[!UICONTROL Save Role]**.

1. Cria quantas funções forem necessárias repetindo essas etapas.

### Modificar uma função

1. Para modificar a função, o administrador da empresa clica em **[!UICONTROL Edit]** no _[!UICONTROL Actions]_coluna.

1. Faz as alterações necessárias nas configurações de nome e permissão.

1. Ao concluir, clique em **[!UICONTROL Save Role]**.

### Duplicar uma função

1. Para duplicar a função, o administrador da empresa clica em **[!UICONTROL Duplicate]** no _[!UICONTROL Actions]_coluna.

1. Faz as alterações necessárias nas configurações de nome e permissão.

1. Ao concluir, clique em **[!UICONTROL Save Role]**.

### Excluir uma função

1. O administrador da empresa encontra a função a ser excluída na lista de funções.

   Somente as funções sem usuários atribuídos podem ser excluídas.

1. Cliques **[!UICONTROL Delete]** no _[!UICONTROL Actions]_coluna.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

## Ações

| Ação | Descrição |
|-----------| ----------- |
| [!UICONTROL Duplicate] | Cria uma cópia da função selecionada. O nome da função duplicada tem `- Duplicated` adicionado ao final. |
| [!UICONTROL Edit] | Altere o nome e/ou o conjunto de permissões. |
| [!UICONTROL Delete] | Exclua a função. Somente as funções sem usuários atribuídos podem ser excluídas. |

{style="table-layout:auto"}

## Permissões de função

- Todos
   - Vendas
      - Permitir check-out (fazer pedido)
         - Usar o método Pagar por Conta
      - Exibir Pedidos
         - Exibir ordens de usuários subordinados
- Aspas
   - Exibir
      - Solicitação, Editar, Excluir
      - Check-out com cotação
      - Exibir cotações de usuários subordinados
- Aprovações de pedidos
   - Exibir Minhas Ordens de Compra
      - Exibição para subordinados
      - Exibir para todas as empresas
   - Aprovar OCs automaticamente criadas nesta função
   - Aprovar Ordens de Compra sem outras aprovações
   - Exibir regras de aprovação
      - Criar, editar e excluir
- Perfil da empresa
   - Informações da conta (Exibir)
      - Editar
   - Endereço legal
      - Editar
   - Contatos (Exibir)
   - Informações de Pagamento (Exibir)
   - Informações sobre Remessa (Exibir)
- Gerenciamento de usuários da empresa
   - Exibir funções e permissões
      - Gerenciar funções e permissões
   - Exibir usuários e equipes
      - Gerenciar usuários e equipes
- Crédito da empresa
   - Exibir

## Atribuir uma função a um usuário da empresa

Após definir as funções necessárias, o administrador da empresa atribui uma função a cada usuário da empresa.

1. Faz logon na conta da empresa como administrador da empresa.

1. No painel esquerdo, escolhe **[!UICONTROL Company Users]**.

   ![Usuários da empresa](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Localiza o usuário na lista e clica em **[!UICONTROL Edit]**.

1. Escolhe o apropriado **[!UICONTROL User Role]** para o usuário.

   ![Editar Usuário - escolha uma função de usuário](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. Cliques **[!UICONTROL Save]**.
