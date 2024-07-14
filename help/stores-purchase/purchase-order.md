---
title: Ordens de compra
description: Saiba como configurar ordens de compra como um método de pagamento offline em sua loja.
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Ordens de compra

Uma _ordem de compra_ (OC) permite que clientes comerciais paguem por compras autorizadas fazendo referência ao número da OC. A ordem de compra é autorizada e emitida antecipadamente pela empresa que está fazendo a compra. Durante o checkout, o cliente escolhe Ordem de compra como método de pagamento. Ao receber sua fatura, a empresa processa o pagamento em seu sistema de contas a pagar e paga a compra.

Antes de aceitar o pagamento por ordem de compra, sempre estabeleça a qualidade de crédito do cliente comercial.

**_Para configurar o pagamento por ordem de compra:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Payment Methods]**.

1. Em _[!UICONTROL Other Payment Methods]_, expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Purchase Order]**.

   ![Ordem de Compra](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   Para obter uma descrição detalhada de cada uma dessas configurações, consulte [Ordem de Compra](../configuration-reference/sales/payment-methods.md#purchase-order) no _Guia de Referência de Configuração_.

   >[!NOTE]
   >
   >Se necessário, primeiro desmarque a caixa de seleção **[!UICONTROL Use system value]** para alterar essas configurações.

1. Para ativar esse método de pagamento, defina **[!UICONTROL Enabled]** como `Yes`.

1. Para **[!UICONTROL Title]**, insira um título que identifique este método de pagamento durante o check-out.

1. Defina **[!UICONTROL New Order Status]** como `Pending` até que o pagamento seja autorizado.

1. Defina **[!UICONTROL Payment from Applicable Countries]** como um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificados na sua configuração de loja podem usar esta forma de pagamento.
   - `Specific Countries` - Depois que você escolher essa opção, a lista _[!UICONTROL Payment from Specific Countries]_será exibida. Para selecionar vários países, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

1. Defina **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** para os valores necessários para se qualificar para este método de pagamento.

   >[!NOTE]
   >
   >Um pedido é qualificado se o total cair entre, ou exatamente corresponder, aos valores totais mínimo ou máximo.

1. Para **[!UICONTROL Sort Order]**, insira um número que determine a posição deste item na lista de métodos de pagamento exibidos durante o check-out.

   Esse número é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
