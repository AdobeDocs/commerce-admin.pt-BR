---
title: Criar entregas de várias origens
description: Saiba como comerciantes de várias origens podem criar e enviar remessas.
exl-id: d2995139-0fc3-4379-a4ec-b0d38ed566bb
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Criar entregas de várias origens

Com [!DNL Inventory Management], envie uma ou mais remessas conforme você tem inventário. Para gerar entregas adicionais conforme necessário, repita essas instruções usando quantidades e origens recomendadas ou informadas manualmente. Essas instruções detalham como os comerciantes de várias origens enviam entregas. Os comerciantes de origem única enviam entregas sem essas etapas adicionais (consulte [Criar uma remessa](../stores-purchase/shipments.md#create-a-shipment){target="_blank"} no guia do usuário principal).

Ao criar entregas, use o Algoritmo de Seleção de Origem para recomendações calculadas. Siga e use essas recomendações ou defina as quantias por origem, gerando entregas personalizadas. Você controla o inventário de saída para cada ordem, definindo as quantias a serem deduzidas, enviando uma ou mais entregas e distribuindo em estoque e backorders, à medida que o inventário estiver disponível. Para cada item de linha na ordem, insira uma quantia a ser deduzida da quantidade de origem.

Você pode enviar entregas parciais para:

- Preencher backorders à medida que o estoque chega

- Saldar deduções de estoque entre origens

À medida que você informa entregas, as quantidades de inventário em estoque deduzem as quantias informadas. Efetivamente, as reservas são convertidas em deduções de quantidade real.

## Criar uma remessa

1. No _Admin_ barra lateral, vá para **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Localize a ordem e abra-a no modo de exibição.

1. Se o pedido for pago e faturado e estiver pronto para ser enviado, clique em **[!UICONTROL Ship]**.

1. Conclua a Seleção de origem para enviar produtos por origem:

   - Para exibir as recomendações de entrega, clique em **[!UICONTROL Source Selection Algorithm]** e selecione um algoritmo.

     | Algoritmo | Descrição |
     |--|--|
     | [Prioridade de origem](source-priority-algorithm.md) | Recomenda remessas de origens de acordo com as ordens de origens atribuídas ao estoque. |
     | [Prioridade de distância](distance-priority-algorithm.md) | Recomenda entregas de origens mais próximas ao endereço de entrega com base na distância física ou no menor tempo de entrega. |

     >[!IMPORTANT]
     >
     >Ao usar o algoritmo de Prioridade de Distância para remessa e roteiros, os dados não são retornados para a [Modo de cálculo](distance-priority-algorithm.md) (dirigindo, andando de bicicleta ou a pé) para uma entrega, o SSA assume como padrão a Prioridade de Origem. É recomendável que você também defina o [prioridade para origens por estoque](stocks-prioritize-sources.md).


   - Para  **[!UICONTROL Select a Source to Ship from]**, selecione uma origem para enviar uma remessa.

   - Para cada item de linha, mantenha a quantidade recomendada ou insira uma quantidade específica na **[!UICONTROL Qty to Deduct]**. Este valor especifica o valor que é deduzido do estoque da origem selecionada.

   - Clique em **[!UICONTROL Proceed to Shipment]**.

     ![Selecione uma Origem e informe uma Quantidade](assets/shipment-adobe-shipping-sources.png){width="350" zoomable="yes"}

1. Revise o _[!UICONTROL New Shipment]_e insira quaisquer alterações adicionais, conforme necessário.

   A variável _[!UICONTROL Inventory]_seção exibe a origem, entrega de produtos, quantidade total solicitada e quantidade a ser entregue.

   ![Detalhes do inventário para a entrega, exemplo de entrega parcial](assets/inventory-shipment-details.png){width="350" zoomable="yes"}

1. Clique em **[!UICONTROL Submit Shipment]** para concluir.
