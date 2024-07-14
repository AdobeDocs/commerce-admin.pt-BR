---
title: Operações de ordem programadas
description: Saiba mais sobre as operações de ordem programadas e as configurações de cron de ordens que oferecem suporte a essa funcionalidade.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Operações de ordem programadas

Use os trabalhos [Cron](../systems/cron.md) para agendar as seguintes tarefas de processamento de ordem:

![Grade de pedidos](./assets/orders-grid.png){width="700" zoomable="yes"}

## Definir tempo de vida da ordem de pagamento pendente

A duração de pedidos com pagamentos pendentes é determinada pela configuração _Configurações de Cron de Pedidos_. O valor padrão é definido como 480 minutos, que são oito horas.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda a seção **[!UICONTROL Sales]** e escolha **[!UICONTROL Sales]** abaixo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Orders Cron Settings]**.

   ![Configurações do Cron de Pedidos](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Pending Payment Order Lifetime (minutes)]**, insira o número de minutos antes de um pagamento pendente expirar.

1. Clique em **[!UICONTROL Save Config]**.

## Habilitar atualizações e reindexação de grade programadas

A configuração de Configurações de Grade agenda atualizações das seguintes grades de gerenciamento de ordens e reindexa os dados conforme agendado por [Cron](../systems/cron.md):

- [Pedidos](orders.md#orders-workspace)
- [Faturas](invoices.md)
- [Entregas](shipments.md)
- [Avisos de Crédito](credit-memos.md)

Ao programar essas tarefas, é possível evitar os bloqueios que ocorrem quando os dados são salvos e reduzir o tempo de processamento. Quando ativado, as atualizações ocorrem somente durante o trabalho cron agendado. Para obter melhores resultados, o Cron deve ser configurado para ser executado uma vez a cada minuto.

**_Para habilitar as atualizações e a reindexação:_**

Quando o [Modo de produção](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (o modo padrão usado no Adobe Commerce na infraestrutura de nuvem) estiver habilitado, execute o seguinte comando:

``bin/magento config:set dev/grid/async_indexing 1``

Quando o [Modo padrão](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) estiver habilitado, conclua as seguintes etapas:

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda a seção **[!UICONTROL Advanced]** e escolha **[!UICONTROL Developer]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Grid Settings]**.

1. Defina **[!UICONTROL Asynchronous Indexing]** como `Enable`.

   ![Configurações de Grade](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save Config]**.
