---
title: Enviar um pedido
description: Saiba como preencher as informações de remessa de uma ordem de processamento e visualizar as informações de remessa e rastreamento.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: abd125cc6e61850db55fb31dbcbd9dc38ac0fca5
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Enviar um pedido

Um pedido que foi pago, mas está aguardando remessa, tem o status `Processing`. O registro de remessa contém um histórico detalhado do processo de preenchimento associado ao pedido. Entregas parciais podem ser feitas até que o pedido seja atendido.

1. Na barra lateral _Admin_, selecione **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Na lista _[!UICONTROL Orders]_, encontre o pedido a ser enviado e clique em para abri-lo.

1. No canto superior direito, clique no botão **[!UICONTROL Ship]**.

1. Para atualizar o endereço de entrega ou cobrança, clique no link **[!UICONTROL Edit]** no canto superior direito da seção.

   Faça as alterações necessárias e clique em **[!UICONTROL Save Order Address]**.

1. Para que a transportadora gere um rótulo de remessa, marque a caixa de seleção **[!UICONTROL Create Shipping Label]** e defina as opções:

   - Para adicionar um número de rastreamento, role até a seção _[!UICONTROL Shipping Information]_&#x200B;e clique em **[!UICONTROL Add Tracking Number]**.

   - Siga um destes procedimentos:

      - Selecione o **[!UICONTROL Carrier]** e insira o rastreamento **[!UICONTROL Number]**.

      - Defina **[!UICONTROL Carrier]** como `Custom Value`, insira um **[!UICONTROL Title]** para a transportadora personalizada e insira o rastreamento **[!UICONTROL Number]**.

      - [Exibir informações de rastreamento](#track-the-shipment).

1. Para fazer uma remessa parcial, role até a seção Itens para Remessa e insira o **[!UICONTROL Qty to Ship]** para cada item.

1. Para notificar os clientes por e-mail sobre a entrega, faça o seguinte:

   - Insira quaisquer comentários que você deseja incluir na caixa **[!UICONTROL Shipment Comments]**.

   - Para incluir os comentários no email de notificação enviado ao cliente, marque a caixa de seleção **[!UICONTROL Append Comments]**.

   - Para enviar uma cópia do email de remessa para você mesmo, marque a caixa de seleção **[!UICONTROL Email Copy of Shipment]**.

     O status de um e-mail de fatura é exibido ao lado do número da fatura concluída como enviado ou não enviado.

1. Quando terminar, clique em **[!UICONTROL Submit Shipment]**.

   O status do pedido muda de `Processing` para `Complete`.

>[!NOTE]
>
>Se um pedido for feito como uma &quot;entrega na loja&quot;, as opções de envio não estarão disponíveis. Clique em **[!UICONTROL Notify Order is Ready for Pickup]** para acionar um email para o cliente. O status do pedido é alterado para `Complete`.

## Exibir os detalhes da remessa

1. Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Localize a remessa na lista e clique em para abrir o registro.

1. Se quiser adicionar um comentário à ordem, role até a seção _[!UICONTROL Comments History]_&#x200B;e insira o comentário na caixa.

   - Para enviar o comentário ao cliente por email, marque a caixa de seleção **[!UICONTROL Notify Customer by Email]**.

   - Para postar o comentário na conta do cliente, marque a caixa de seleção **[!UICONTROL Visible on Frontend]**.

1. Clique em **[!UICONTROL Update]**.

## Rastrear a remessa

**Método 1:** Na guia de informações da ordem

1. Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Localize a ordem de remessa na grade e clique em **[!UICONTROL View]**.

1. Role para baixo até a seção _[!UICONTROL Shipping & Handling Information]_&#x200B;e clique em **[!UICONTROL Track Order]**.

   Todas as informações de rastreamento disponíveis são exibidas em uma janela pop-up.

1. Quando estiver pronto, clique em **[!UICONTROL Close Window]**.

**Método 2:** Na guia de remessa da ordem

1. Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Localize a remessa na lista e clique em para abrir o registro.

1. Clique em **[!UICONTROL Track this Shipment]**.

   Todas as informações de rastreamento disponíveis são exibidas em uma janela pop-up.

1. Quando estiver pronto, clique em **[!UICONTROL Close Window]**.
