---
title: Priorizar fontes de estoque para um estoque
description: Saiba como organizar as origens de cima para baixo em prioridade, que é usada ao determinar as deduções de remessa e inventário.
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '210'
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
