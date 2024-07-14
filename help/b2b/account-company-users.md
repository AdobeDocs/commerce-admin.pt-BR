---
title: Gerenciar contas de usuário da empresa
description: Saiba mais sobre as contas de usuário da empresa e como elas funcionam na conta da empresa associada.
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Gerenciar contas de usuário da empresa

Os usuários da empresa são atribuídos pelo administrador da empresa e ficam visíveis no Administrador na grade _[!UICONTROL Customers]_pelo tipo de cliente_[!UICONTROL Company User]_. Normalmente, esses indivíduos são compradores com diferentes níveis de permissão para acessar serviços e recursos da loja.

O administrador da empresa primeiro configura a [estrutura da empresa](account-company-structure.md) e depois conclui as seguintes tarefas, conforme necessário:

- Criar usuários da empresa e atribuir usuários às equipes

- Defina funções e permissões e atribua usuários a funções

>[!IMPORTANT]
>
>Os usuários da empresa podem ser adicionados, editados ou removidos somente pelo administrador da empresa. A remoção não pode ser revertida porque o usuário foi removido da estrutura da empresa.

## Adicionar usuários da empresa

1. Na loja, o administrador da empresa faz logon em sua conta.

1. No painel esquerdo, escolhe **[!UICONTROL Company Users]**.

   ![Usuários da empresa](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Clica em **[!UICONTROL Add New User]** e faz o seguinte:

   - Entra no **[!UICONTROL Job Title]** do novo usuário.

   - Escolhe o **[!UICONTROL User Role]** apropriado se as funções e permissões estiverem definidas. Caso contrário, eles poderão retornar posteriormente para atribuir a função.

     ![Adicionar novo usuário](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - Preenche os campos restantes conforme necessário para o usuário:

      - **[!UICONTROL First Name]** e **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Phone Number]**

   Por padrão, o **[!UICONTROL Status]** da conta é `Active`.

1. Quando terminar, clica em **[!UICONTROL Save]**.

1. Repete o processo para criar quantos usuários da empresa forem necessários.

   Os novos usuários são exibidos na lista Usuários da empresa, juntamente com o Administrador da empresa.

Para economizar tempo durante o primeiro pedido, o administrador da empresa pode lembrar cada usuário da empresa de adicionar o endereço padrão de entrega e cobrança da empresa ao seu [catálogo de endereços](../customers/account-dashboard-address-book.md).

## Editar usuários da empresa

1. Na loja, o administrador da empresa faz logon em sua conta.

1. No painel esquerdo, escolhe **[!UICONTROL Company Users]**.

1. Localiza o registro de usuário a ser atualizado e clica em **[!UICONTROL Edit]**.

1. Faz as alterações necessárias.

1. Quando terminar, clica em **[!UICONTROL Save]**.

## Remover um usuário da empresa

1. Na loja, o administrador da empresa faz logon em sua conta.

1. No painel esquerdo, escolhe **[!UICONTROL Company Structure]**.

1. Seleciona o usuário da empresa na estrutura da empresa.

1. Cliques **[!UICONTROL Delete Selected]**.

   ![Excluir usuário](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. Quando for solicitada a confirmação, clique em **[!UICONTROL Delete]**.

No Administrador, o usuário da empresa permanece listado na grade [Clientes](../customers/customers-all.md), mas com o status `Inactive`.

## Descrições dos campos

| Campo | Descrição |
|--------------|---------------|
| [!UICONTROL Job Title] | O cargo do usuário da empresa. |
| [!UICONTROL User Role] | A [função](account-company-roles-permissions.md) atribuída ao usuário da empresa. Opções: `Default User` / (outras funções) |
| [!UICONTROL First Name] | O nome do usuário da empresa. |
| [!UICONTROL Last Name] | O sobrenome do usuário da empresa. |
| [!UICONTROL Email] | O endereço de email do usuário da empresa. |
| [!UICONTROL Phone Number] | O número de telefone do usuário da empresa. |
| [!UICONTROL Status] | O status da conta de usuário da empresa. Opções: `Active` / `Inactive` |

{style="table-layout:auto"}
