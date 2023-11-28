---
title: Checkout de subtotal zero
description: Saiba como configurar um subtotal zero como um método de pagamento offline em sua loja.
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Checkout de subtotal zero

_Checkout de subtotal zero_ pode ser usado para pedidos com um subtotal de zero que são tributados após a aplicação de um desconto. Por exemplo, o check-out de subtotal zero pode ser usado nas seguintes situações:

- Um desconto cobre todo o preço da compra, sem custo adicional para o frete.

- O cliente adiciona um [baixável](../catalog/product-create-downloadable.md) ou [virtual](../catalog/product-create-virtual.md) ao carrinho de compras, e o preço é igual a zero.

- O preço de um [simples](../catalog/product-create-simple.md) o produto for zero e a variável [frete grátis](shipping-free.md) está disponível.

- A [código do cupom](../merchandising-promotions/price-rules-cart-coupon.md) cobre o preço total dos produtos e do transporte.

Para economizar tempo, as ordens de subtotal zero podem ser definidas para faturar automaticamente.

**_Para configurar o check-out de subtotal zero:_**

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Payment Methods]**.

1. Em _[!UICONTROL Other Payment Methods]_, expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Zero Subtotal Checkout]**seção.

   ![Checkout de Subtotal Zero](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se necessário, primeiro limpe o **[!UICONTROL Use system value]** para alterar essas configurações.

1. Para ativar o check-out de subtotal zero, defina **[!UICONTROL Enabled]** para `Yes`.

1. Para **[!UICONTROL Title]**, insira um título que identifique o método de Subtotal zero durante o check-out.

1. Se os pedidos normalmente aguardam aprovação, aceite o padrão **[!UICONTROL New Order Status]** as `Pending"` até que o pedido seja aprovado.

   Se preferir, você pode usar o `Processing` ou `Suspected Fraud` status de novos pedidos com este método de pagamento.

1. Definir **[!UICONTROL Automatically Invoice All Items]** para `Yes` se você quiser faturar automaticamente todos os itens que tenham um saldo zero.

   Essa opção só estará disponível se a variável **[!UICONTROL New Order Status]** está definida como `Processing`.

   >[!NOTE]
   >
   >Se _[!UICONTROL New Order Status]_está definida como `Processing` e_[!UICONTROL Automatically Invoice All Items]_ está definida como `No`, você também deve atribuir **[!UICONTROL Order Status]** = `Processing` para o **[!UICONTROL Order State]** = `Pending` e **[!UICONTROL Default Status]** = `No` mapeamento no [Status do pedido](order-status.md#custom-order-status) página.

1. Definir **[!UICONTROL Payment from Applicable Countries]** a um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificado na configuração da loja pode usar esse método de pagamento.
   - `Specific Countries` - Após escolher essa opção, a variável _[!UICONTROL Payment from Specific Countries]_é exibida. Para selecionar vários países, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

1. Para **[!UICONTROL Sort Order]**, informe um número que determine a posição deste item na lista de métodos de pagamento exibida durante a finalização da compra.

   Esse número é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
