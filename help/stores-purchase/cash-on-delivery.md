---
title: Dinheiro na entrega (COD)
description: Saiba como configurar o pagamento na entrega como um método de pagamento offline em sua loja.
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Dinheiro na entrega (COD)

O Adobe Commerce e o Magento Open Source permitem que você aceite _dinheiro na entrega_ (COD) pagamentos relativos a compras. Você pode aceitar o pagamento COD somente de países específicos e pode ajustar a configuração com limites totais mínimos e máximos de pedidos.

A transportadora recebe o pagamento do cliente no momento da entrega, que é então transferido a você. Você pode fazer um ajuste para qualquer taxa cobrada pelo serviço da transportadora em seus encargos de remessa e manuseio.

**_Para configurar pagamentos de caixa na distribuição:_**

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Payment Methods]**.

1. Em _Outros métodos de pagamento_, expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Cash On Delivery Payment]** seção.

   ![Pagamento de Dinheiro na Entrega](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   Para obter uma descrição detalhada de cada uma dessas configurações, consulte [Pagamento à vista na entrega](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) no _Guia de referência de configuração_.

   >[!NOTE]
   >
   >Se necessário, primeiro limpe o **[!UICONTROL Use system value]** para alterar essas configurações.

1. Para ativar o pagamento à vista na entrega, defina **[!UICONTROL Enabled]** para `Yes`.

1. Para **[!UICONTROL Title]**, informe um título que identifique o método de pagamento COD durante a finalização da compra.

1. Definir **[!UICONTROL New Order Status]** para `Pending` até que o recebimento do pagamento seja confirmado.

   Se preferir, você pode usar o `Processing` ou `Suspected Fraud` status de novos pedidos com este método de pagamento.

1. Definir **[!UICONTROL Payment from Applicable Countries]** a um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificado na configuração da loja pode usar esse método de pagamento.
   - `Specific Countries` - Após escolher essa opção, a variável _[!UICONTROL Payment from Specific Countries]_é exibida. Para selecionar vários países, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

1. Insira o **[!UICONTROL Instructions]** para aceitar a entrega de um pedido COD.

1. Definir **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** aos valores do pedido que são necessários para se qualificar para o pagamento do COD.

   >[!NOTE]
   >
   >Um pedido é qualificado se o total estiver entre, ou corresponder, ao total mínimo ou máximo do pedido.

1. Para **[!UICONTROL Sort Order]**, informe um número que determine a posição deste item na lista de métodos de pagamento exibida durante a finalização da compra.

   Esse número é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
