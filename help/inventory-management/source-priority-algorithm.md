---
title: Configurar o algoritmo de prioridade do Source
description: Saiba como configurar a prioridade de origem usada para a ordem das fontes atribuídas em seu estoque para fazer recomendações.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
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

1. Na exibição _[!UICONTROL Assign Sources]_, marque a caixa de seleção da origem necessária e clique em **[!UICONTROL Done]**&#x200B;para atribuir uma origem ao estoque.

>[!NOTE]
>
>Ao usar o algoritmo [Prioridade de Distância](distance-priority-algorithm.md) para remessa, se as rotas e os dados não retornarem para o [modo de Computação](distance-priority-algorithm.md) selecionado (direção, ciclismo ou caminhada) para uma remessa, o SSA assumirá como padrão o uso da Prioridade de Source.

![Pedido de Source após a priorização](assets/inventory-stock-priority-after.png)

| Ícones | Descrição |
|----------------------------------------------|----------------------------------------------------------------|
| ![arraste e solte o ícone para definir a prioridade](assets/icon-drag-and-drop-action.png) | Use para arrastar e soltar fontes de acordo com a prioridade. |
| ![clique no ícone para desatribuir uma origem](assets/icon-delete-action.png) | Desatribuindo uma origem a um estoque. |
