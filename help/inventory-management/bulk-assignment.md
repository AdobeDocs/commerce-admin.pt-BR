---
title: Atribuição e cancelamento de atribuição de origem de estoque em massa
description: Saiba como usar a ferramenta Atribuir origens para gerenciar atribuições de origem de produtos.
exl-id: 1f1e81a5-fb06-46b7-84ca-7feea4942093
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# Atribuição e cancelamento de atribuição de origem em massa

Use a ferramenta _Atribuir fontes_ para adicionar uma ou mais fontes aos seus produtos. A ferramenta ajuda a criar e atribuir fontes personalizadas ao Estoque padrão ou Estoque personalizado e preparar novos locais e estoque.

Depois de adicionar novas fontes personalizadas, você pode adicionar [quantidades de estoque por produto](quantities-assign-per-product.md) ou por vários produtos por meio do Administrador ou usando o [recurso de importação](inventory-import-export.md).

![Adicionar fontes de estoque para os produtos selecionados](assets/inventory-bulk-assign-sources.gif)

## Atribuir origens e quantidades

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecione os produtos para os quais deseja modificar as origens.

   Procure ou pesquise para encontrar os produtos e marque essas caixas de seleção.

1. Clique no menu **[!UICONTROL Actions]** na parte superior e escolha **[!UICONTROL Assign Inventory Source]**.

1. Clique em **[!UICONTROL OK]** no diálogo de confirmação.

1. Para todas as origens que deseja adicionar aos produtos, marque as caixas de seleção.

1. Clique em **[!UICONTROL Assign Sources]**.

   ![Selecione produtos para adicionar fontes](assets/inventory-bulk-assign-sources-summary.png){width="600" zoomable="yes"}

As origens são adicionadas aos produtos com uma quantidade de inventário de 0. Você pode adicionar [quantidades de estoque](quantities-assign-per-product.md) por origem.

## Cancelar atribuição de origens e quantidades

Ao desatribuir uma origem de um produto, você está indicando que o produto não está mais em estoque nesse local. Esse processo limpa completamente todos os dados de inventário da origem atualmente atribuída ao produto. Se quiser mover o estoque existente para um novo local, considere usar a opção _Transferir estoque_.

{{$include /help/_includes/unassign-source.md}}

É altamente recomendável concluir todos os pedidos e remessas desses produtos antes de remover a origem.

![Cancelar atribuição de origens a produtos selecionados](assets/inventory-bulk-unassign-sources.gif)

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecione os produtos para os quais deseja modificar origens.

   Procure ou pesquise para encontrar os produtos e marque essas caixas de seleção.

1. Clique no menu **[!UICONTROL Actions]** na parte superior e escolha **[!UICONTROL Unassign Inventory Source]**.

1. Clique em **[!UICONTROL OK]** no diálogo de confirmação.

1. Selecione a origem que deseja remover dos produtos.

   A página exibe um alerta de que o cancelamento da atribuição remove todos os dados específicos de origem e quantidade do produto.

1. Clique em **[!UICONTROL Unassign Sources]**.

   ![Remover fontes dos produtos selecionados](assets/inventory-bulk-unassign-sources-summary.png){width="600" zoomable="yes"}
