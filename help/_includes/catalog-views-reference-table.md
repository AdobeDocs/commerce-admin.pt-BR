---
title: Tabela de referência de exibições de catálogo
description: Tabela de referência reutilizada para a grade Exibições de catálogo
source-git-commit: bc4baccc4b40fb7ecdc7f489bfaf3c797881db88
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%
---
# Tabela de referência de exibições de catálogo

A grade lista uma linha para cada exibição de catálogo criada quando um catálogo compartilhado é sincronizado com [!DNL Adobe Commerce Optimizer]. A grade é somente leitura além da ação de atribuição de chave. As exibições de catálogo são criadas e removidas automaticamente conforme o conector sincroniza catálogos compartilhados configurados no Adobe Commerce. Se um catálogo for removido, haverá um [período de carência](/help/systems/catalog-view-sync-status.md#configure-the-deletion-grace-period) antes da exibição do catálogo correspondente e da exclusão dos dados.

Para atribuir ou desatribuir chaves de acesso restrito, consulte [Atribuir chaves a uma exibição de catálogo](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view).

| Campo | Descrição |
| --- | --- |
| [!UICONTROL ACO Catalog View ID] | O identificador da exibição de catálogo correspondente em [!DNL Adobe Commerce Optimizer]. Consulte [Resumo do Status de Sincronização da Exibição de Catálogo](/help/systems/catalog-view-sync-status.md#catalog-view-sync-status-summary) para verificar sua integridade de sincronização. |
| [!UICONTROL Store View] | A exibição de loja que a exibição de catálogo representa. Consulte [Exibições de armazenamento](/help/stores-purchase/store-views.md). |
| [!UICONTROL Access Keys] | Os títulos das chaves de acesso restrito atualmente atribuídas à exibição de catálogo. Consulte [Gerenciamento de Chaves de Acesso Restrito](/help/systems/restricted-access-keys.md). |
| [!UICONTROL Actions] | Selecione **[!UICONTROL Edit Restricted Access Keys]** para atribuir ou cancelar a atribuição de chaves para a exibição do catálogo. Consulte [Atribuir chaves a uma exibição de catálogo](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view). |

{style="table-layout:auto"}
