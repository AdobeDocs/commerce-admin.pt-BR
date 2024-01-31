---
title: Gerenciamento da empresa
description: Simplifique a administração e o gerenciamento de organizações B2B com modelos operacionais complexos.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Gerenciamento da empresa

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponível somente para participantes do programa Beta"}

O gerenciamento de empresas simplifica as operações de negócios para empresas com estruturas organizacionais complexas. Os usuários administradores podem criar uma hierarquia de empresa para refletir uma organização B2B, atribuindo empresas à empresa principal designada. Essa atribuição permite que o administrador da empresa principal exiba e gerencie empresas na organização.

Iniciar tarefas de gerenciamento da empresa a partir do *[!UICONTROL Companies]* exibição. No Administrador, acesse  **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Grade de empresas gerenciadas B2B](./assets/companies-grid-view.png){width="700" zoomable="yes"}

No *[!UICONTROL Companies grid]*, o *[!UICONTROL Company Type]* indica se uma empresa é gerenciada como parte de uma organização ou como uma empresa separada.

- `Parent` é uma organização comercial com uma ou mais empresas atribuídas. Uma empresa principal não pode ser atribuída como um filho de outra empresa.

- `Child` é uma empresa atribuída a uma organização. Uma empresa pode ser atribuída somente a uma empresa principal.

- `Company` representa uma única empresa. Uma única empresa pode se tornar parte de uma organização tornando-a uma empresa principal ou atribuindo-a a uma empresa principal existente.

Ao editar uma empresa principal ou secundária, expanda *[!UICONTROL Company Hierarchy]* para exibir todas as empresas na organização. A `Current` indica a empresa que você está editando.

![Grade de Hierarquia da empresa B2B](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}


## Visualize e configure o [!UICONTROL Company Hierarchy]

Na criação inicial da empresa, a variável [!UICONTROL Company Hierarchy] a grade está vazia. Também fica em branco se a empresa for uma única empresa.

![Grade de Hierarquia da Empresa B2B](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

Para empresas-mãe, os usuários administradores com as permissões apropriadas podem realizar as seguintes tarefas:

- Crie a hierarquia da empresa criando uma nova organização pai ou atualizando uma existente.
- Gerencie uma organização existente para adicionar ou remover empresas.

Para obter detalhes, consulte [Gerenciar a hierarquia da empresa](assign-companies.md).
