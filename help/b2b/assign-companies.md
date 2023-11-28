---
title: Gerenciar a hierarquia da empresa
description: Crie e gerencie hierarquias da empresa para oferecer suporte a organizações B2B com modelos operacionais complexos.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 10b01db562777ef2fcc224177d7a83c0a6fc90e7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Gerenciar o [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponível somente para participantes do programa Beta"}

Os administradores podem criar um [!UICONTROL Company Hierarchy] atribuindo empresas relacionadas a uma empresa-mãe designada, que é a empresa na parte superior da hierarquia organizacional.

Criar uma empresa primária editando uma empresa que não foi atribuída a uma existente [!UICONTROL Company Hierarchy]e atribuindo empresas relacionadas.

![Grade de Hierarquias da Empresa](./assets/company-detail-view.png){width="700"}

Depois que uma empresa é atribuída a uma hierarquia, a variável [!UICONTROL Company type] na **Empresas** a grade identifica a empresa como uma `Parent` ou  `Child` empresa.  Se a variável [!UICONTROL Company Type] é `Company`, a empresa não faz parte de uma hierarquia de empresa e pode tornar-se uma empresa-mãe ou ser atribuída a uma empresa-mãe existente.

>[!NOTE]
>
>Para obter detalhes sobre o [!UICONTROL Company Hierarchy] consulte [Hierarquia da empresa](account-company-create.md#company-hierarchy) descrições de campo.

No Administrador, você gerencia atribuições da empresa editando uma empresa e usando o [!UICONTROL Company Hierarchy] seção do [!UICONTROL Company] página para atribuir ou cancelar atribuição de empresas.

## Atribuir empresas a uma empresa principal

1. No _Admin_ barra lateral, navegue até **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Grade de Empresas](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Na grade Empresas, abra a página de detalhes da empresa para criar as atribuições.

   - Para atribuir empresas adicionais a uma empresa-mãe existente, selecione a **[!UICONTROL Edit]** ação para a empresa-mãe.
   - Para criar uma nova empresa pai, selecione a **[!UICONTROL Edit]** ação para a empresa designada como a matriz.

     Não é possível criar uma nova empresa pai a partir de uma empresa pai ou filho existente.

   ![Nova Empresa](./assets/company-update.png){width="700" zoomable="yes"}

1. Na página Detalhes da empresa, expanda a variável **[!UICONTROL Company Hierarchy]** e selecione **[!UICONTROL Assign Companies]**.

   ![Nova Empresa](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

   Ao expandir essa visualização, você pode ver as atribuições da empresa existentes, se houver. A empresa-mãe sempre aparece na parte superior do _[!UICONTROL Company Hierarchy]_grade com um `current company indicator` mostrado na linha da empresa que está sendo editada.

1. As empresas disponíveis para atribuição estão listadas na grade. Selecione as empresas a serem atribuídas e selecione **[!UICONTROL Assign Selected Companies]**.

1. Você pode **Selecionar tudo nesta página** ou um item específico da linha da empresa e clique em **[!UICONTROL Assign Selected Companies]**.

   ![Nova Empresa](./assets/assign-selected-companies.png){width="700" zoomable="yes"}

1. Quando solicitado, conclua a atribuição da empresa selecionando **[!UICONTROL Assign]**.

## Cancelar atribuição de empresas a uma empresa principal

1. No _Admin_ barra lateral, navegue até **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Grade de Empresas](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Na página Empresas, abra a página de detalhes da empresa principal selecionando o **[!UICONTROL Edit]** ação.

   ![Nova Empresa](./assets/company-update.png){width="700" zoomable="yes"}

1. Exibir a lista de empresas atribuídas expandindo o **[!UICONTROL Company Hierarchy]** lista suspensa.

1. Na grade da hierarquia da empresa, cancele a atribuição de uma empresa selecionando o **[!UICONTROL Select]** para a empresa e escolha **[!UICONTROL Unassign from parent]**.

   ![Nova Empresa](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

1. Quando solicitado, remova a empresa atribuída da hierarquia selecionando **[!UICONTROL Unassign]**.
