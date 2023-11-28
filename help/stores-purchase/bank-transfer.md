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

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Payment Methods]**.

1. Em _Outros métodos de pagamento_, expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Bank Transfer Payment]** seção.

   ![Pagamento de Transferência Bancária](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se necessário, primeiro limpe o **[!UICONTROL Use system value]** para alterar essas configurações.

1. Para ativar transferências bancárias, defina **[!UICONTROL Enabled]** para `Yes`.

1. Para **[!UICONTROL Title]**, informe um título que identifique o método de pagamento de transferência bancária durante a finalização da compra.

1. Definir **[!UICONTROL New Order Status]** para `Pending` até que o pagamento seja autorizado.

1. Definir **[!UICONTROL Payment from Applicable Countries]** a um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificado na configuração da loja pode usar esse método de pagamento.

   - `Specific Countries` - Após escolher essa opção, a variável _[!UICONTROL Payment from Specific Countries]_é exibida. Para selecionar vários países, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

1. Insira o **[!UICONTROL Instructions]** que os clientes devem seguir para configurar uma transferência bancária.

   Dependendo do país onde seu banco está localizado e das exigências do banco, você pode incluir as seguintes informações:

   - Nome da conta bancária
   - Número da conta bancária
   - Código de roteamento bancário
   - Nome do banco
   - Endereço do banco

1. Definir **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** aos valores necessários para se qualificar para usar este método de pagamento.

   >[!NOTE]
   >
   >Um pedido é qualificado se o total cair entre, ou exatamente corresponder, aos valores totais mínimo ou máximo.

1. Para **[!UICONTROL Sort Order]**, informe um número que determine a posição deste item na lista de métodos de pagamento exibida durante a finalização da compra.

   Esse número é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
