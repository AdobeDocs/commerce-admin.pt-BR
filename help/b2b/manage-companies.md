---
title: Gerenciamento da empresa
description: Simplifique a administração e o gerenciamento de organizações B2B com modelos operacionais complexos.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# Gerenciamento da empresa

O gerenciamento de empresas simplifica as operações de negócios para empresas com estruturas organizacionais complexas. Os usuários administradores podem criar uma hierarquia de empresa para refletir uma organização B2B, atribuindo empresas à empresa principal designada. Essa atribuição permite que o administrador da empresa principal exiba e gerencie empresas na organização.

Inicie as tarefas de gerenciamento da empresa na exibição *[!UICONTROL Companies]*. No Administrador, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Grade Gerenciar Empresas B2B](./assets/companies-grid-view.png){width="700" zoomable="yes"}

A coluna *[!UICONTROL Company Type]* indica se uma empresa é gerenciada como parte de uma organização ou como uma empresa separada.

- `Parent` é uma organização comercial com uma ou mais empresas atribuídas. Uma empresa principal não pode ser atribuída como um filho de outra empresa.

- `Child` é uma empresa atribuída a uma organização. Uma empresa pode ser atribuída somente a uma empresa principal.

- `Company` representa uma única empresa. Uma única empresa pode se tornar parte de uma organização tornando-a uma empresa principal ou atribuindo-a a uma empresa principal existente.

Ao editar uma empresa principal ou secundária, expanda *[!UICONTROL Company Hierarchy]* para exibir todas as empresas na organização. Um sinalizador `Current` indica a empresa que você está editando.

![Grade de Hierarquia da Empresa B2B](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

## Exibir e configurar o [!UICONTROL Company Hierarchy]

Na criação inicial da empresa, a grade *[!UICONTROL Company Hierarchy]* está vazia. Também fica em branco se a empresa for uma única empresa.

![Grade de Hierarquia da Empresa B2B](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

Se a empresa for uma empresa principal de uma organização e as contas da empresa de outras empresas na organização já tiverem sido configuradas no Adobe Commerce, os usuários administradores com as permissões apropriadas poderão atribuir empresas e usar a grade *[!UICONTROL Company Hierarchy]* para concluir outras tarefas de gerenciamento da empresa:

- Exibir todas as empresas associadas à empresa primária.
- Na página de detalhes de uma empresa principal, atribua mais empresas à organização.
- Remover uma empresa de uma organização usando a ação *[!UICONTROL Unassign from parent]*.
- Atualize a configuração *[!UICONTROL Advanced Settings]* para aplicar as mesmas configurações a várias empresas.

Para obter instruções detalhadas, consulte [Gerenciar a hierarquia da empresa](manage-company-hierarchy.md).

