---
title: Atribuir origens de estoque por produto
description: Saiba como atribuir uma origem de inventário a um produto.
exl-id: 7e47be25-633e-4f5d-bb61-0d9e79b6dbad
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Atribuir fontes por produto

Antes de modificar quantidades e configurações, você deve atribuir [origens](sources-manage.md) aos produtos.

{{$include /help/_includes/unassign-source.md}}

## Atribuir origens a um produto

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abrir um produto no _Editar_ modo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Sources]** seção.

   Esta seção permite modificar a origem, atualizar quantidades de inventário e muito mais.

   >[!NOTE]
   >
   >Atualmente, somente produtos simples, configuráveis, virtuais, para download e agrupados são compatíveis com várias fontes. Os produtos do pacote podem ser criados e gerenciados somente com a Origem padrão e o Estoque.

   ![Seção Fontes de produto](assets/inventory-product-sources-before.png){width="600" zoomable="yes"}

1. Para adicionar uma origem, clique em **[!UICONTROL Assign Sources]**.

1. No _[!UICONTROL Assign Sources]_selecione a caixa de seleção ao lado de cada origem que você deseja atribuir ao produto.

   ![Produto - fontes de atribuição](assets/inventory-product-assign-sources.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Done]** para adicionar as fontes.

1. Siga um destes procedimentos para salvar:

   - Clique em **[!UICONTROL Save]**.
   - No _[!UICONTROL Save]_ (![seta de menu](../assets/icon-menu-down-arrow-red.png)), escolha **[!UICONTROL Save & Close]**.

Depois de atribuir origens, atualize o [quantidade em estoque](quantities-assign-per-product.md) para cada origem de produto.
