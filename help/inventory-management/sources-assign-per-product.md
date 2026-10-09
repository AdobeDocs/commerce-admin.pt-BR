---
title: Atribuir origens de estoque por produto
description: Atribua uma ou mais origens [!DNL Inventory Management] a um produto no Administrador antes de definir quantidades e limites por origem.
exl-id: 7e47be25-633e-4f5d-bb61-0d9e79b6dbad
feature: Inventory, Products
last-update: 2023-10-26
TQID: 'https://experienceleague.adobe.com/Wjx3w6Z-oNALxNRHw65BZDeCzka3BQvtg-m4a9kp-Y8'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
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
source-git-commit: 15f1e2ee152fb047443da68dec2cc69551e6c7a0
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%
---
# Atribuir fontes por produto

Antes de modificar quantidades e configurações, você deve atribuir [origens](sources-manage.md) aos produtos.

{{$include /help/_includes/unassign-source.md}}

## Atribuir origens a um produto

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abra um produto no modo _Editar_.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Sources]**.

   Esta seção permite modificar a origem, atualizar quantidades de inventário e muito mais.

   >[!NOTE]
   >
   >Atualmente, somente produtos simples, configuráveis, virtuais, para download e agrupados são compatíveis com várias fontes. Os produtos do pacote podem ser criados e gerenciados somente com o Source padrão e o Stock.

   ![Seção de fontes de produtos](assets/inventory-product-sources-before.png){width="600" zoomable="yes"}

1. Para adicionar uma origem, clique em **[!UICONTROL Assign Sources]**.

1. Na página _[!UICONTROL Assign Sources]_, marque a caixa de seleção ao lado de cada origem que você deseja atribuir ao produto.

   ![Produto - atribuir fontes](assets/inventory-product-assign-sources.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Done]** para adicionar as fontes.

1. Siga um destes procedimentos para salvar:

   - Clique em **[!UICONTROL Save]**.
   - No menu _[!UICONTROL Save]_(![seta de menu](../assets/icon-menu-down-arrow-red.png)), escolha **[!UICONTROL Save & Close]**.

Depois de atribuir origens, atualize a [quantidade em estoque](quantities-assign-per-product.md) para cada origem de produto.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
