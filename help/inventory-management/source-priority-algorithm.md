---
title: Configurar o algoritmo de prioridade do Source
description: Saiba como configurar a prioridade de origem usada para a ordem das fontes atribuídas em seu estoque para fazer recomendações.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
TQID: https://experienceleague.adobe.com/TB4THYjkzbNvEbsjNzOewNtYS6JoRvLDiQQCovSMkbI
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 0%

---

# Configurar o algoritmo de prioridade do Source

Os estoques personalizados incluem uma lista atribuída de fontes para vender e enviar o inventário de produtos disponível por meio de sua loja. Esse algoritmo usa a ordem das fontes atribuídas no estoque para fazer recomendações.

Quando executado, o algoritmo:

- Funciona pela ordem configurada de fontes no nível de estoque, começando na parte superior

- Recomenda uma quantidade para entrega e origem por produto com base na ordem na lista, na quantidade disponível e na quantidade solicitada

- Continua na lista até que a remessa do pedido seja preenchida

- Ignora fontes desabilitadas se encontradas na lista

Para configurar, organize essas origens de cima para baixo em prioridade para atender pedidos. O Source Selection Algorithm (SSA) fornece uma Prioridade de algoritmo usando essa ordem ao determinar as deduções de entrega e inventário. Consulte [Priorizando fontes para um estoque](stocks-prioritize-sources.md).

## Configurar a prioridade das fontes

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. Abra um estoque no modo de edição e navegue até a área _[!UICONTROL Sources]_.

1. Clique em **[!UICONTROL Assign Sources]**.

1. Na exibição _[!UICONTROL Assign Sources]_, marque a caixa de seleção da origem necessária e clique em **[!UICONTROL Done]**para atribuir uma origem ao estoque.

>[!NOTE]
>
>Ao usar o algoritmo [Prioridade de Distância](distance-priority-algorithm.md) para remessa, se as rotas e os dados não retornarem para o [modo de Computação](distance-priority-algorithm.md) selecionado (direção, ciclismo ou caminhada) para uma remessa, o SSA assumirá como padrão o uso da Prioridade de Source.

![Pedido de Source após a priorização](assets/inventory-stock-priority-after.png)

| Ícones | Descrição |
|----------------------------------------------|----------------------------------------------------------------|
| ![arraste e solte o ícone para definir a prioridade](assets/icon-drag-and-drop-action.png) | Use para arrastar e soltar fontes de acordo com a prioridade. |
| ![clique no ícone para desatribuir uma origem](assets/icon-delete-action.png) | Desatribuindo uma origem a um estoque. |
