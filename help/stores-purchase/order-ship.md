---
title: Enviar um pedido
description: Saiba como preencher as informações de remessa de uma ordem de processamento e visualizar as informações de remessa e rastreamento.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Enviar um pedido

Uma ordem que foi paga, mas está aguardando entrega, tem o `Processing` status. O registro de remessa contém um histórico detalhado do processo de preenchimento associado ao pedido. Entregas parciais podem ser feitas até que o pedido seja atendido.

1. No _Admin_ barra lateral, selecione **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. No _[!UICONTROL Orders]_localize o pedido a ser enviado e clique em para abri-lo.

1. No canto superior direito, clique na guia **[!UICONTROL Ship]** botão.

1. Para atualizar o endereço de faturamento ou de entrega, clique no link **[!UICONTROL Edit]** no canto superior direito da seção.

   Faça as alterações necessárias e clique em **[!UICONTROL Save Order Address]**.

1. Para que a transportadora gere um rótulo de entrega, selecione o **[!UICONTROL Create Shipping Label]** e defina as opções:

   - Para adicionar um número de rastreamento, role para baixo até a _[!UICONTROL Shipping Information]_e clique em **[!UICONTROL Add Tracking Number]**.

   - Siga um destes procedimentos:

      - Selecione o **[!UICONTROL Carrier]** e insira o rastreamento **[!UICONTROL Number]**.

      - Definir **[!UICONTROL Carrier]** para `Custom Value`, insira um **[!UICONTROL Title]** para a transportadora personalizada e insira o **[!UICONTROL Number]**.

      - [Exibir informações de rastreamento](#track-the-shipment).

1. Para fazer uma entrega parcial, role até a seção Itens para Entrega e informe o **[!UICONTROL Qty to Ship]** para cada item.

1. Para notificar os clientes por e-mail sobre a entrega, faça o seguinte:

   - Insira quaisquer comentários que você deseja incluir no **[!UICONTROL Shipment Comments]** caixa.

   - Para incluir os comentários no email de notificação enviado ao cliente, selecione a **[!UICONTROL Append Comments]** caixa de seleção

   - Para enviar uma cópia do email de remessa para você mesmo, selecione o **[!UICONTROL Email Copy of Shipment]** caixa de seleção

     O status de um e-mail de fatura é exibido ao lado do número da fatura concluída como enviado ou não enviado.

1. Quando terminar, clique em **[!UICONTROL Submit Shipment]**.

   O status do pedido muda de `Processing` para `Complete`.

>[!NOTE]
>
>Se um pedido for feito como uma &quot;entrega na loja&quot;, as opções de envio não estarão disponíveis. Clique em **[!UICONTROL Notify Order is Ready for Pickup]** para acionar um email para o cliente. O status do pedido é alterado para `Complete`.

## Exibir os detalhes da remessa

1. No _Admin_ barra lateral, vá para **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Localize a remessa na lista e clique em para abrir o registro.

1. Se quiser adicionar um comentário à ordem, role para baixo até a _[!UICONTROL Comments History]_e insira o comentário na caixa.

   - Para enviar o comentário ao cliente por email, selecione o **[!UICONTROL Notify Customer by Email]** caixa de seleção

   - Para publicar o comentário na conta do cliente, selecione o **[!UICONTROL Visible on Frontend]** caixa de seleção

1. Clique em **[!UICONTROL Submit Comment]**.

## Rastrear a remessa

**Método 1:** Na guia de informações da ordem

1. No _Admin_ barra lateral, vá para **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Localize a ordem de remessa na grade e clique em **[!UICONTROL View]**.

1. Role para baixo até _[!UICONTROL Shipping & Handling Information]_e clique em **[!UICONTROL Track Order]**.

   Todas as informações de rastreamento disponíveis são exibidas em uma janela pop-up.

1. Quando estiver pronto, clique em **[!UICONTROL Close Window]**.

**Método 2:** Guia Entrega da ordem de origem

1. No _Admin_ barra lateral, vá para **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Localize a remessa na lista e clique em para abrir o registro.

1. Clique em **[!UICONTROL Track this Shipment]**.

   Todas as informações de rastreamento disponíveis são exibidas em uma janela pop-up.

1. Quando estiver pronto, clique em **[!UICONTROL Close Window]**.
