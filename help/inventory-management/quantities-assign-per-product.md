---
title: Atribuir quantidades de estoque por produto
description: Saiba como atualizar as quantidades de estoque do seu produto e rastrear os valores de estoque disponíveis e em estoque.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Atribuir quantidades por produto

Depois de adicionar [origens](sources-assign-per-product.md), atualize as quantidades de estoque do seu produto. Esses valores rastreiam os valores de estoque disponível e em estoque.

Para ocultar o inventário de uma origem das entregas sem remover a origem, defina _[!UICONTROL Source Item Status]_para `Out of Stock`. As opções SSA e entrega acessam apenas as origens listadas como `In Stock` com a quantidade disponível no estoque.

Todas as quantidades e origens atualizadas são exibidas na grade de produtos.

## Atualizar quantidades

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Localize e abra um produto no modo de edição.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Sources]** seção.

1. Definir **[!UICONTROL Source Item Status]** para `In Stock`.

1. para atualizar a quantidade de estoque disponível, insira um valor para **[!UICONTROL Qty]**.

1. Para definir uma notificação para quantidades de inventário, siga um destes procedimentos:

   - Quantidade de notificação personalizada - Desmarque a **[!UICONTROL Use Default]** e insira um valor em **[!UICONTROL Notify Qty]**.
   - Quantidade de Notificação Padrão - Selecione a **[!UICONTROL Use Default]** caixa de seleção [!DNL Commerce] O verifica e usa a configuração em _[!UICONTROL Advanced Inventory]_ou configuração de armazenamento global.

   ![Atualizar Quantidades de Produto por Origem](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Siga um destes procedimentos para salvar:

   - Clique em **[!UICONTROL Save]**.

   - No **[!UICONTROL Save]** (![Seta de menu](../assets/icon-menu-down-arrow-red.png)), escolha **[!UICONTROL Save & Close]**.


A Grade de Produtos é atualizada com uma lista de todas as origens e quantidades relacionadas. Para produtos com mais de cinco origens atribuídas, passe o mouse sobre a _[!UICONTROL Quantity per Source]_para ver a lista completa.

![Quantidades de produto por origem](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
