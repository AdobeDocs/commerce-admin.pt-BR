---
title: Operações de ordem programadas
description: Saiba mais sobre as operações de ordem programadas e as configurações de cron de ordens que oferecem suporte a essa funcionalidade.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Operações de ordem programadas

Uso [Cron](../systems/cron.md) ordens de produção para programar as seguintes tarefas de processamento de ordem:

![Grade de pedidos](./assets/orders-grid.png){width="700" zoomable="yes"}

## Definir tempo de vida da ordem de pagamento pendente

A duração das ordens com pagamentos pendentes é determinada pela _Configurações do Cron de Pedidos_ configuração. O valor padrão é definido como 480 minutos, que são oito horas.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda a **[!UICONTROL Sales]** e escolha **[!UICONTROL Sales]** por baixo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Orders Cron Settings]** seção.

   ![Configurações do Cron de Pedidos](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Pending Payment Order Lifetime (minutes)]**, insira o número de minutos antes de um pagamento pendente expirar.

1. Clique em **[!UICONTROL Save Config]**.

## Habilitar atualizações e reindexação de grade programadas

A configuração Definições de Grade programa atualizações para as seguintes grades do Order Management e reindexa os dados conforme programado por [Cron](../systems/cron.md):

- [Pedidos](orders.md#orders-workspace)
- [Faturas](invoices.md)
- [Entregas](shipments.md)
- [Avisos de Crédito](credit-memos.md)

Ao programar essas tarefas, é possível evitar os bloqueios que ocorrem quando os dados são salvos e reduzir o tempo de processamento. Quando ativado, as atualizações ocorrem somente durante o trabalho cron agendado. Para obter melhores resultados, o Cron deve ser configurado para ser executado uma vez a cada minuto.

**_Para habilitar as atualizações e reindexação:_**

Quando [Modo de produção](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (o modo padrão usado no Adobe Commerce na infraestrutura em nuvem) estiver ativado, execute o seguinte comando:

``bin/magento config:set dev/grid/async_indexing 1``

Quando [Modo padrão](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) estiver ativado, conclua as seguintes etapas:

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda a **[!UICONTROL Advanced]** e escolha **[!UICONTROL Developer]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Grid Settings]** seção.

1. Definir **[!UICONTROL Asynchronous Indexing]** para `Enable`.

   ![Configurações da grade](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save Config]**.
