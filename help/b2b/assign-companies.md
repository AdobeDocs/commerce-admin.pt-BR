---
title: Gerenciar a hierarquia da empresa
description: Saiba como gerenciar organizações B2B com modelos operacionais complexos criando hierarquias da empresa
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Gerenciar o [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponível somente para participantes do programa Beta"}

Os administradores podem criar um [!UICONTROL Company Hierarchy] atribuindo empresas relacionadas a uma empresa principal designada, que é a empresa na parte superior da organização. Se a variável [!UICONTROL Company Type] é `Company`, a empresa não faz parte de uma organização e pode tornar-se uma empresa-mãe ou ser atribuída a uma empresa-mãe existente.

No Administrador, você gerencia atribuições da empresa editando uma empresa e atualizando o [!UICONTROL Company Hierarchy] configuração para atribuir ou cancelar atribuição de empresas.

![Grade de Hierarquias da Empresa](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>Para obter detalhes sobre o [!UICONTROL Company Hierarchy] consulte [Hierarquia da empresa](account-company-create.md#company-hierarchy) descrições de campo.

## Atribuir empresas a uma organização

1. No _Admin_ barra lateral, navegue até **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Grade de Empresas](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. No [!UICONTROL Companies] abra a página de detalhes da empresa para criar as atribuições.

   - Para atribuir empresas adicionais a uma empresa-mãe existente, selecione a **[!UICONTROL Edit]** ação para a empresa-mãe.
   - Para criar uma empresa principal, selecione a **[!UICONTROL Edit]** ação para a empresa designar como a empresa principal.

     Não é possível criar uma empresa principal a partir de uma empresa principal ou secundária existente.

1. Na página de detalhes da empresa, expanda **[!UICONTROL Company Hierarchy]**.

   ![Grade de Hierarquias da Empresa](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   A grade mostra as atribuições de empresa existentes, se houver. A empresa principal está sempre posicionada na parte superior do [!UICONTROL Company Hierarchy] grade. A variável `[!UICONTROL Current]` indica a empresa que está sendo editada.

1. Adicionar empresas à organização principal.

   - Escolha em uma lista de empresas disponíveis ao selecionar **[!UICONTROL Assign Companies]**.

   - **Selecionar tudo nesta página** ou selecione um ou mais itens de linha específicos da empresa.

   - Selecionar **[!UICONTROL Assign Selected Companies]**.

   - Conclua a atribuição da empresa selecionando **[!UICONTROL Assign]**.

     ![Atribuir empresas à organização](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## Cancelar atribuição de empresas a uma empresa principal

1. No _Admin_ barra lateral, navegue até **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Grade de Empresas](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. No [!UICONTROL Companies] grade, abra a página de detalhes da empresa para a empresa principal selecionando **[!UICONTROL Edit]**.

1. Exibir a lista de empresas atribuídas expandindo **[!UICONTROL Company Hierarchy]**.

1. No [!UICONTROL Company Hierarchy] grade, cancele a atribuição de uma empresa usando o **[!UICONTROL Select]** controle de ação a escolher **[!UICONTROL Unassign from parent]**.

   ![Cancelar Atribuição de Empresas de uma organização principal](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. Quando solicitado, remova a empresa atribuída da hierarquia selecionando **[!UICONTROL Unassign]**.
