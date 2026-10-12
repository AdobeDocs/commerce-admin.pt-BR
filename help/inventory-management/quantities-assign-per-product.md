---
title: Atribuir quantidades de estoque por produto
description: Defina quantidades disponíveis e limites por origem em uma página de produto para manter a precisão do estoque de venda do [!DNL Inventory Management].
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
TQID: 'https://experienceleague.adobe.com/0OBXyHUbsWVXmEnWEWd0CGcBNhci57w8HGtDCGCWuOk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%
---
# Atribuir quantidades por produto

Depois de adicionar [origens](sources-assign-per-product.md), atualize as quantidades de estoque do seu produto. Esses valores rastreiam os valores de estoque disponível e em estoque.

Para ocultar o estoque de uma origem das remessas sem remover a origem, defina _[!UICONTROL Source Item Status]_&#x200B;como `Out of Stock`. As opções SSA e remessa acessam apenas as fontes listadas como `In Stock` com a quantidade de estoque disponível.

Todas as quantidades e origens atualizadas são exibidas na grade de produtos.

## Atualizar quantidades

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Localize e abra um produto no modo de edição.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Sources]**.

1. Defina **[!UICONTROL Source Item Status]** como `In Stock`.

1. para atualizar a quantidade de estoque disponível, insira um valor para **[!UICONTROL Qty]**.

1. Para definir uma notificação para quantidades de inventário, siga um destes procedimentos:

   - Quantidade de Notificação Personalizada - Desmarque a caixa de seleção **[!UICONTROL Use Default]** e insira uma quantidade em **[!UICONTROL Notify Qty]**.
   - Quantidade de Notificação Padrão - Marque a caixa de seleção **[!UICONTROL Use Default]**. [!DNL Commerce] verifica e usa a configuração em _[!UICONTROL Advanced Inventory]_&#x200B;ou na configuração de repositório global.

   ![Atualizar Quantidades de Produto por Source](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Siga um destes procedimentos para salvar:

   - Clique em **[!UICONTROL Save]**.

   - No menu **[!UICONTROL Save]** (![Seta do menu](../assets/icon-menu-down-arrow-red.png)), escolha **[!UICONTROL Save & Close]**.


A Grade de Produtos é atualizada com uma lista de todas as origens e quantidades relacionadas. Para produtos com mais de cinco origens atribuídas, passe o mouse sobre a coluna _[!UICONTROL Quantity per Source]_&#x200B;para ver a lista completa.

![Quantidades de produto por origem](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
