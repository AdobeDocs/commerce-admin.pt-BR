---
title: Gerenciar contas de usuário da empresa
description: Saiba mais sobre as contas de usuário da empresa e como elas funcionam na conta da empresa associada.
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 9c16d7a3909598328cc42bbcbf39fc14ae6a9eb9
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Gerenciar contas de usuário da empresa

Na loja, os usuários da empresa são atribuídos pelo administrador da empresa e ficam visíveis na página _[!UICONTROL Company Users]_. Normalmente, esses indivíduos são compradores com diferentes níveis de permissão para acessar serviços e recursos da loja.

O administrador da empresa primeiro configura a [estrutura da empresa](account-company-structure.md) e depois conclui as seguintes tarefas, conforme necessário:

- Criar usuários da empresa e atribuir usuários às equipes

- Defina funções e permissões e atribua usuários a funções

Os usuários da empresa podem ser adicionados, editados, desativados ou excluídos somente pelo administrador da empresa.

- Quando um usuário é removido, o status da conta muda para *inativo* e o cliente não pode mais fazer logon na empresa. Os administradores ainda podem acessar todo o conteúdo associado ao usuário. O administrador da conta pode restaurar o acesso alterando o status da conta de *[!UICONTROL Active]* para [!UICONTROL Company Users].

- Quando uma conta de usuário é excluída, a conta e qualquer conteúdo associado são excluídos da loja. Esta ação não pode ser revertida.

## Adicionar usuários da empresa

1. Na loja, o administrador da empresa faz logon em sua conta.

1. No painel esquerdo, escolhe **[!UICONTROL Company Users]**.

   ![Usuários da empresa](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Clica em **[!UICONTROL Add New User]** e faz o seguinte:

   - Entra no **[!UICONTROL Job Title]** do novo usuário.

   - Escolhe o **[!UICONTROL User Role]** apropriado se as funções e permissões estiverem definidas. Caso contrário, eles poderão retornar posteriormente para atribuir a função.

     ![Adicionar novo usuário](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - Adiciona as informações do usuário nos campos restantes:
      - **[!UICONTROL First Name]** e **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Work Phone Number]**

   Por padrão, o **[!UICONTROL Status]** da conta é `Active`.

1. Quando terminar, clica em **[!UICONTROL Save]**.

1. Repete o processo para criar quantos usuários da empresa forem necessários.

   Os novos usuários são exibidos na lista Usuários da empresa, juntamente com o Administrador da empresa.

Para economizar tempo durante o primeiro pedido, o administrador da empresa pode lembrar cada usuário da empresa de adicionar o endereço padrão de entrega e cobrança da empresa ao seu [catálogo de endereços](../customers/account-dashboard-address-book.md).

## Remover um usuário do [!UICONTROL Company structure]

Os administradores da empresa podem remover um usuário do [!UICONTROL Company Structure].

Após a remoção de uma conta, seu status muda para *inativo*, e o usuário não pode mais fazer logon na loja.
O administrador pode reativar uma conta editando as informações da conta do usuário na página Usuários da empresa.

1. Na loja, o administrador da empresa faz logon em sua conta.

1. No painel esquerdo, escolhe **[!UICONTROL Company Structure]**.

1. Seleciona o usuário da empresa na estrutura da empresa.

1. Cliques **[!UICONTROL Remove from Structure]**.

   ![Excluir usuário](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. Quando for solicitada a confirmação, clique em **[!UICONTROL Remove]**.

   No Administrador, o usuário da empresa permanece listado na grade [Clientes](../customers/customers-all.md), mas com o status `Inactive`.

## Exibir e gerenciar contas de usuário da empresa

Os administradores da empresa podem exibir e gerenciar contas de usuários da empresa usando os filtros de exibição na página [!UICONTROL Company Users].

![Usuários da empresa](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

- Exibir somente usuários inativos selecionando **[!UICONTROL Show Inactive Users]**.
- Exibir somente usuários ativos selecionando **[!UICONTROL Show Active Users]**.
- Exiba todos os usuários selecionando **[!UICONTROL Show All Users]**.

O administrador da empresa pode gerenciar uma conta individual usando o item de linha *[!UICONTROL Actions]* para editar as informações da conta, gerenciar o status da conta ou excluir uma conta.

### Editar informações da conta de usuário da empresa

Os administradores da empresa podem atualizar as informações de perfil da conta do usuário e alterar o status da conta.

1. Na página [!UICONTROL Company Users], encontre a conta de usuário a ser atualizada. Clique em **[!UICONTROL Edit]**.

1. Faça as alterações necessárias nas informações da conta do usuário, incluindo a alteração do status da conta.

1. Aplicar as alterações clicando em **[!UICONTROL Save]**.

>[!NOTE]
>
>Se você editar uma conta de usuário da empresa e notar que faltam informações obrigatórias da conta no perfil, como cargo e número de telefone comercial, isso indica que a conta foi adicionada por um administrador do site do Commerce. Essas contas não podem ser editadas na loja. Para atualizar informações ou alterar o status da conta, entre em contato com o administrador do site.

### Desativar ou excluir uma conta ativa

1. Na página [!UICONTROL Company Users], encontre a conta de usuário a ser atualizada. Clique em **[!UICONTROL Manage]**.

   ![Gerenciar usuário na página Usuários da Empresa](./assets/company-users-manage-storefront.png){width="600" zoomable="yes"}

1. Quando solicitado, desative ou exclua a conta do usuário, conforme necessário.

>[!IMPORTANT]
>
>Excluir uma conta de usuário da empresa remove a conta e todo o conteúdo associado do sistema. Esta ação não pode ser revertida.

## Descrições dos campos de perfil da conta de usuário da empresa

| Campo | Descrição |
|--------------------------------|---------------|
| [!UICONTROL Job Title] | O cargo do usuário da empresa. |
| [!UICONTROL User Role] | A [função](account-company-roles-permissions.md) atribuída ao usuário da empresa. Opções: `Default User` / (outras funções) |
| [!UICONTROL First Name] | O nome do usuário da empresa. |
| [!UICONTROL Last Name] | O sobrenome do usuário da empresa. |
| [!UICONTROL Email] | O endereço de email do usuário da empresa. |
| [!UICONTROL Work Phone Number] | O número de telefone comercial do usuário da empresa. |
| [!UICONTROL Status] | O status da conta de usuário da empresa. Opções: `Active` / `Inactive` |

{style="table-layout:auto"}
