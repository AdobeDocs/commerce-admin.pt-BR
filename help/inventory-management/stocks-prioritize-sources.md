---
title: Priorizar fontes de estoque para um estoque
description: Saiba como organizar as origens de cima para baixo em prioridade, que é usada ao determinar as deduções de remessa e inventário.
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/oPgeuN3-Il-yf3zpG2r4PNAmNbf-4gmz5-GFngM3-Ng
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 0%

---

# Priorizar origens para um estoque

Depois de adicionar [fontes](sources-manage.md) ao [estoque](stocks-manage.md), organize essas fontes de cima para baixo em prioridade para atender pedidos. O Source Selection Algorithm (SSA) fornece uma Prioridade de algoritmo usando essa ordem ao determinar as deduções de entrega e inventário.

A prioridade de origem nos estoques não influencia as fontes atribuídas ao editar inventários de produtos.

Neste exemplo, o Stock do Reino Unido tem origens fora de ordem para um armazenamento e dois depósitos em Londres e um depósito em Berlim.

![Pedido de Source antes da priorização](assets/inventory-priority-before.png){width="350" zoomable="yes"}

O comerciante prefere ter as remessas priorizadas a partir do maior armazém de Berlim, em seguida, o armazém de Londres, o local de transbordamento de Londres e, finalmente, a loja em Londres. Para alterar a ordem, as entradas são arrastadas e soltas na ordem desejada.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**.

1. Abra o estoque no modo _Editar_.

1. Expanda a guia _[!UICONTROL Sources]_, se necessário.

1. Use o ![ícone Classificar](assets/icon-sort.png) para arrastar e soltar as fontes em uma prioridade de cima (primeiro) para baixo (último).

   Esse pedido é importante ao enviar pedidos. SSA recomenda entregas com base na ordem de origens

1. Clique em **[!UICONTROL Save & Continue]** para salvar as alterações.

![Pedido de Source após a priorização](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
