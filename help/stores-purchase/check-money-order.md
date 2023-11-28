---
title: Cheques e ordens de pagamento
description: Saiba como configurar ordens de pagamento em cheque e dinheiro como um método de pagamento offline em sua loja.
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Cheques e ordens de pagamento

O Adobe Commerce e o Magento Open Source permitem que você aceite pagamentos em cheque ou ordem de pagamento. A variável _Cheque/Ordem de pagamento_ o método de pagamento está habilitado para sua loja por padrão. Você pode aceitar cheques e ordens de pagamento somente de países específicos e pode ajustar a configuração com limites totais mínimos e máximos de ordens.

**_Para configurar o pagamento por cheque ou ordem de pagamento:_**

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Payment Methods]**.

1. Em _[!UICONTROL Other Payment Methods]_, expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Check / Money Order]**seção.

   ![Cheque/Ordem de pagamento](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   Para obter uma descrição detalhada de cada uma dessas configurações, consulte [Cheque/Ordem de pagamento](../configuration-reference/sales/payment-methods.md#check--money-order) no _Guia de referência de configuração_.

   >[!NOTE]
   >
   >Se necessário, primeiro limpe o **[!UICONTROL Use system value]** para alterar essas configurações.

1. Para aceitar pagamento por cheque ou ordem de pagamento, defina **[!UICONTROL Enabled]** para `Yes`.

1. Para **[!UICONTROL Title]**, insira um título que identifique o método de pagamento em cheque/ordem de pagamento em dinheiro durante o check-out.

1. Se os pedidos normalmente aguardam aprovação, aceite o padrão **[!UICONTROL New Order Status]** as `Pending"` até ser aprovado.

   Se preferir, você pode usar o `Processing` ou `Suspected Fraud` status de novos pedidos com este método de pagamento.

1. Definir **[!UICONTROL Payment from Applicable Countries]** a um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificado na configuração da loja pode usar esse método de pagamento.
   - `Specific Countries` - Após escolher essa opção, a variável _[!UICONTROL Payment from Specific Countries]_é exibida. Para selecionar vários países, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

1. Para **[!UICONTROL Make Check Payable To]**, insira o nome da parte à qual o cheque deve ser pago.

1. Para **[!UICONTROL Send Check To]**, insira o endereço ou a caixa postal onde os cheques são enviados.

1. Definir **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** aos valores do pedido necessários para se qualificar para este método de pagamento.

   >[!NOTE]
   >
   >Um pedido é qualificado se o total cair entre, ou exatamente corresponder, aos valores totais mínimo ou máximo.

1. Para **[!UICONTROL Sort Order]**, informe um número que determine a posição deste item na lista de métodos de pagamento exibida durante a finalização da compra.

   Esse número é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
