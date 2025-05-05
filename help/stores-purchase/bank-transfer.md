---
title: Transferências bancárias
description: Saiba como configurar transferências bancárias como um método de pagamento offline em sua loja.
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# Transferências bancárias

O Adobe Commerce e o Magento Open Source permitem que você aceite o pagamento transferido de uma conta bancária de cliente e depositado em sua conta bancária de comerciante.

**_Para configurar pagamentos de transferência bancária:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Payment Methods]**.

1. Em _Outros Métodos de Pagamento_, expanda ![Seletor de Expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Bank Transfer Payment]**.

   ![Pagamento por Transferência Bancária](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se necessário, primeiro desmarque a caixa de seleção **[!UICONTROL Use system value]** para alterar essas configurações.

1. Para ativar transferências bancárias, defina **[!UICONTROL Enabled]** como `Yes`.

1. Para **[!UICONTROL Title]**, insira um título que identifique o método de pagamento por transferência bancária durante o check-out.

1. Defina **[!UICONTROL New Order Status]** como `Pending` até que o pagamento seja autorizado.

1. Defina **[!UICONTROL Payment from Applicable Countries]** como um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificados na sua configuração de loja podem usar esta forma de pagamento.

   - `Specific Countries` - Depois que você escolher essa opção, a lista _[!UICONTROL Payment from Specific Countries]_&#x200B;será exibida. Para selecionar vários países, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

1. Insira o **[!UICONTROL Instructions]** que seus clientes devem seguir para configurar uma transferência bancária.

   Dependendo do país onde seu banco está localizado e das exigências do banco, você pode incluir as seguintes informações:

   - Nome da conta bancária
   - Número da conta bancária
   - Código de roteamento bancário
   - Nome do banco
   - Endereço do banco

1. Defina **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** com os valores necessários para qualificar-se para usar este método de pagamento.

   >[!NOTE]
   >
   >Um pedido é qualificado se o total cair entre, ou exatamente corresponder, aos valores totais mínimo ou máximo.

1. Para **[!UICONTROL Sort Order]**, insira um número que determine a posição deste item na lista de métodos de pagamento exibidos durante o check-out.

   Esse número é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
