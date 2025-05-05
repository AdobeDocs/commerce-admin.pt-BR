---
title: Adicionar usuários a uma conta da empresa
description: Saiba como adicionar um cliente existente a uma conta de empresa.
exl-id: ee2f9c27-37d6-4997-8285-1c4c84f8d04c
feature: B2B, Companies, Customers
role: Admin, User
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# Adicionar usuários a uma conta da empresa

Quando habilitado na configuração do, o administrador da empresa adiciona e gerencia usuários da empresa na loja. No entanto, as contas de usuários da empresa também podem ser adicionadas e gerenciadas no Administrador.

Se necessário, você pode atribuir um usuário a mais de uma empresa. Por exemplo, se os compradores B2B oferecerem suporte a várias empresas, você poderá adicionar suas contas de usuário a todas as empresas com as quais fazem negócios. Na loja, os compradores atribuídos a várias empresas podem alternar entre as contas da empresa selecionando entre as empresas disponíveis no menu *[!UICONTROL Company]*.

![Associar à Empresa](./assets/company-assign-multi-switcher.png){width="700"}

>[!NOTE]
>
>Se um indivíduo já tiver uma conta pessoal em sua loja e depois for trabalhar para uma empresa, não atribua a conta individual da pessoa à empresa. Em vez disso, crie uma conta de usuário da empresa para a pessoa com um endereço de email da empresa.

## Adicionar um usuário da empresa

Quando você adiciona um usuário da empresa, a primeira empresa associada à conta do usuário é a empresa padrão.

1. Na barra lateral Admin, vá para **[!UICONTROL Customers > All Customers]**.

1. Clique em **[!UICONTROL Add new customer]**.

1. Configure a nova conta.

   1. Especifique o status inicial da conta definindo a alternância **[!UICONTROL Customer Active]**.

      Ative-a para ativar imediatamente a conta ou desative-a para criar uma conta inativa.

   1. Selecione o escopo do site na lista **[!UICONTROL Associate to Website]**.

   1. Clique em **[!UICONTROL Associate to Company]** para exibir as empresas disponíveis.

      ![Associar à Empresa](./assets/company-assign-customer-account.png){width="675"}

      Se necessário, filtre a lista digitando as primeiras letras do nome da empresa na caixa de entrada.

   1. Na lista, selecione uma ou mais empresas às quais deseja atribuir o cliente e clique em **[!UICONTROL Done]**.

      Os usuários da empresa são adicionados automaticamente ao grupo de clientes (ou [catálogo compartilhado](catalog-shared.md)) para cada empresa associada à sua conta.

   1. Insira as informações de conta de usuário necessárias: **[!UICONTROL First Name]**, **[!UICONTROL Last Name]** e **[!UICONTROL Email]**.

   1. Permitir que representantes de vendas façam logon na loja em nome do cliente habilitando **[!UICONTROL Allow remote shopping assistance]**.

   1. Aplicar as alterações clicando em **[!UICONTROL Save Customer]**.

      ![Grade de clientes com atribuições de empresa](./assets/company-assign-user-assignments.png){width="675"}

O [!UICONTROL Customers grid] mostra uma linha separada para cada empresa à qual o usuário está atribuído. As colunas a seguir são atualizadas.

- A coluna _[!UICONTROL Customer Type]_&#x200B;é atualizada para mostrar a função atribuída ao usuário.

  Se esta for a primeira vez que o cliente é atribuído a uma empresa, a coluna _[!UICONTROL Customer Type]_&#x200B;é atualizada de&#x200B;_[!UICONTROL Individual user]_ para _[!UICONTROL Company User]_.

- A coluna _[!UICONTROL Group]_&#x200B;é alterada para o nome do grupo de clientes (ou catálogo compartilhado) atribuído à empresa.

- A coluna _[!UICONTROL Company]_&#x200B;exibe o nome da empresa à qual o perfil de cliente está associado.

## Atribuir um usuário a uma ou mais contas da empresa

Quando você atribui um novo usuário, a primeira empresa associada à conta do usuário é a empresa padrão.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Encontre o cliente na grade e clique em **[!UICONTROL Edit]** na coluna _[!UICONTROL Action]_.

1. No painel esquerdo, escolha **[!UICONTROL Account Information]**.

1. Na lista **[!UICONTROL Associate to Company]**, selecione uma ou mais empresas a serem atribuídas ao usuário da empresa e clique em **[!UICONTROL Done]**.

1. Aplicar as alterações clicando em **[!UICONTROL Save Customer]**.

## Remover atribuição da empresa de uma conta de usuário

Remover uma empresa de um perfil de usuário revoga o acesso do usuário a essa empresa. Os dados do usuário permanecem acessíveis no Administrador. Se você remover todas as atribuições da empresa, o _[!UICONTROL Customer Type]_&#x200B;muda para *[!UICONTROL Individual user]*, desabilitando recursos B2B para a conta.

1. Na grade Cliente, em Admin, edite o perfil do cliente a ser atualizado.

1. Na seção *[!UICONTROL Account Information], remova uma empresa atribuída do campo **[!UICONTROL Associate to Company]** clicando em **[!UICONTROL X]** no rótulo de nome da empresa.

1. Aplicar as alterações clicando em **[!UICONTROL Save Customer]**.

>[!NOTE]
>
>Se um usuário da empresa for atribuído como administrador da empresa, não será possível excluir a associação da empresa desse usuário até que você atualize a conta da Empresa para atribuir um novo administrador de empresa.
