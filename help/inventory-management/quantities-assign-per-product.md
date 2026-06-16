---
title: Atribuir quantidades de estoque por produto
description: Saiba como atualizar as quantidades de estoque do seu produto e rastrear os valores de estoque disponíveis e em estoque.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/0OBXyHUbsWVXmEnWEWd0CGcBNhci57w8HGtDCGCWuOk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 0%

---

# Atribuir quantidades por produto

Depois de adicionar [origens](sources-assign-per-product.md), atualize as quantidades de estoque do seu produto. Esses valores rastreiam os valores de estoque disponível e em estoque.

Para ocultar o estoque de uma origem das remessas sem remover a origem, defina _[!UICONTROL Source Item Status]_como `Out of Stock`. As opções SSA e remessa acessam apenas as fontes listadas como `In Stock` com a quantidade de estoque disponível.

Todas as quantidades e origens atualizadas são exibidas na grade de produtos.

## Atualizar quantidades

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Localize e abra um produto no modo de edição.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Sources]**.

1. Defina **[!UICONTROL Source Item Status]** como `In Stock`.

1. para atualizar a quantidade de estoque disponível, insira um valor para **[!UICONTROL Qty]**.

1. Para definir uma notificação para quantidades de inventário, siga um destes procedimentos:

   - Quantidade de Notificação Personalizada - Desmarque a caixa de seleção **[!UICONTROL Use Default]** e insira uma quantidade em **[!UICONTROL Notify Qty]**.
   - Quantidade de Notificação Padrão - Marque a caixa de seleção **[!UICONTROL Use Default]**. [!DNL Commerce] verifica e usa a configuração em _[!UICONTROL Advanced Inventory]_ou na configuração de repositório global.

   ![Atualizar Quantidades de Produto por Source](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Siga um destes procedimentos para salvar:

   - Clique em **[!UICONTROL Save]**.

   - No menu **[!UICONTROL Save]** (![Seta do menu](../assets/icon-menu-down-arrow-red.png)), escolha **[!UICONTROL Save & Close]**.


A Grade de Produtos é atualizada com uma lista de todas as origens e quantidades relacionadas. Para produtos com mais de cinco origens atribuídas, passe o mouse sobre a coluna _[!UICONTROL Quantity per Source]_para ver a lista completa.

![Quantidades de produto por origem](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
