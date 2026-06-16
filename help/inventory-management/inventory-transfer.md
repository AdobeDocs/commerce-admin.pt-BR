---
title: Transferir inventário para origem
description: Saiba como comerciantes de várias origens podem transferir o estoque de produtos de um local de origem para outro.
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/HV6GQjHa88xgcSAi-LXhyqe7k2QW95VzQ8eG2mGlJ8I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 282
ht-degree: 0%

---

# Transferir inventário para origem

Dependendo das necessidades comerciais e do status do local, os comerciantes de várias origens geralmente transferem o inventário de produtos de um local de origem para outro. Por exemplo, você pode fechar um local de depósito ou não enviar mais produtos específicos de um local, movendo todas as operações desses produtos para um novo local.

Essa opção permite selecionar um ou mais produtos, a origem de origem para transferir o inventário e a origem de destino para receber quantidades:

- As quantidades de estoque, o Status do Item do Source (Em Estoque/Fora de Estoque) e a Quantidade de Notificação para a origem selecionada são movidos por produto.

- Se um produto não tiver essa origem, ele será ignorado.

- Todo o inventário de produtos da origem é movido. Você não pode transferir uma quantidade parcial.

>[!NOTE]
>
>Se as origens e os destinos estiverem em estoques diferentes, isso afetará a Quantidade Venável agregada e as reservas de ordens em andamento.

Também é possível cancelar a atribuição da origem ao transferir quantidades de inventário.

{{$include /help/_includes/unassign-source.md}}

![Transferir estoque para outra origem](assets/inventory-bulk-transfer-source.gif)

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecione os produtos para os quais deseja modificar origens.

   Procure ou pesquise para encontrar produtos e marcar as caixas de seleção para transferência.

1. Clique no menu **[!UICONTROL Actions]** na parte superior e escolha **[!UICONTROL Transfer Inventory to Source]**.

1. Clique em **[!UICONTROL OK]** no diálogo de confirmação.

1. Para transferir produtos para um novo destino, selecione a origem (_[!UICONTROL from]_).

1. para transferir produtos para um novo destino, selecione a origem de destino (_[!UICONTROL to]_).

1. Para remover a origem dos produtos, marque a caixa de seleção opcional **[!UICONTROL Unassign from origin source after transfer]**.

   ![Selecionar origem e destino para transferência](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Transfer Inventory]**.

   Todas as quantidades de produtos são deduzidas da origem e adicionadas à origem de destino. A Quantidade e a Quantidade Venável são atualizadas automaticamente.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
