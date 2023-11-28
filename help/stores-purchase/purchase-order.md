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

A _ordem de compra_ (PO) permite que os clientes comerciais paguem por compras autorizadas fazendo referência ao número da OC. A ordem de compra é autorizada e emitida antecipadamente pela empresa que está fazendo a compra. Durante o checkout, o cliente escolhe Ordem de compra como método de pagamento. Ao receber sua fatura, a empresa processa o pagamento em seu sistema de contas a pagar e paga a compra.

Antes de aceitar o pagamento por ordem de compra, sempre estabeleça a qualidade de crédito do cliente comercial.

**_Para configurar o pagamento por ordem de compra:_**

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Payment Methods]**.

1. Em _[!UICONTROL Other Payment Methods]_, expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Purchase Order]**seção.

   ![Ordem de Compra](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   Para obter uma descrição detalhada de cada uma dessas configurações, consulte [Ordem de Compra](../configuration-reference/sales/payment-methods.md#purchase-order) no _Guia de referência de configuração_.

   >[!NOTE]
   >
   >Se necessário, primeiro limpe o **[!UICONTROL Use system value]** para alterar essas configurações.

1. Para ativar esse método de pagamento, defina **[!UICONTROL Enabled]** para `Yes`.

1. Para **[!UICONTROL Title]**, informe um título que identifique este método de pagamento durante o check-out.

1. Definir **[!UICONTROL New Order Status]** para `Pending` até que o pagamento seja autorizado.

1. Definir **[!UICONTROL Payment from Applicable Countries]** a um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificado na configuração da loja pode usar esse método de pagamento.
   - `Specific Countries` - Após escolher essa opção, a variável _[!UICONTROL Payment from Specific Countries]_é exibida. Para selecionar vários países, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

1. Definir **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** aos valores necessários para se qualificar para este método de pagamento.

   >[!NOTE]
   >
   >Um pedido é qualificado se o total cair entre, ou exatamente corresponder, aos valores totais mínimo ou máximo.

1. Para **[!UICONTROL Sort Order]**, informe um número que determine a posição deste item na lista de métodos de pagamento exibida durante o check-out.

   Esse número é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
