---
title: Frete gratuito
description: Saiba como configurar uma opção de envio gratuito para sua loja.
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Frete gratuito

_Frete gratuito_ O é uma das promoções mais eficazes que você pode oferecer. Ele pode se basear em uma compra mínima ou pode ser configurado como um [regra de preço do carrinho](../merchandising-promotions/price-rules-cart.md) que é aplicado quando um conjunto de condições é atendido. Se ambos se aplicarem à mesma ordem, a definição de configuração terá prioridade sobre a regra do carrinho.

>[!NOTE]
>
>Verifique a configuração da sua transportadora para quaisquer configurações adicionais que possam ser necessárias para frete gratuito.

## Etapa 1: configurar frete grátis

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Delivery Methods]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Free Shipping]** seção.

   >[!NOTE]
   >
   >Se necessário, primeiro desmarque a opção **[!UICONTROL Use system value]** para alterar as configurações a seguir, conforme descrito.

1. Definir **[!UICONTROL Enabled]** para `Yes`.

1. Para **[!UICONTROL Title]**, insira um título que identifique o método de envio gratuito durante a finalização da compra e uma **[!UICONTROL Method Name]** para descrevê-lo.

1. Para **[!UICONTROL Minimum Order Amount]**, insira o valor total mínimo que se qualifica para frete gratuito.

   >[!TIP]
   >
   >Para usar o frete grátis com [taxas de tabela](shipping-table-rate.md), torne o _[!UICONTROL Minimum Order Amount]_tão alto que nunca é atendido. O uso desse valor alto impede que o frete grátis entre em vigor, a menos que seja acionado por uma regra de preço.

1. Definir **[!UICONTROL Include Tax to Amount]**:

   - `Yes` - Inclui o imposto ao calcular o Valor mínimo do pedido (Subtotal + Imposto - Desconto).
   - `No` - Não inclui imposto ao calcular o Valor mínimo do pedido (Subtotal - Desconto).

   ![Envio gratuito](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Displayed Error Message]**, insira a mensagem a ser exibida se o frete gratuito ficar indisponível.

1. Definir **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificado na configuração da loja pode usar frete grátis.

   - `Specific Countries` - Após escolher esse valor, a variável _[!UICONTROL Ship to Specific Countries]_é exibida. Selecione cada país na lista onde a remessa gratuita pode ser usada.

1. Definir **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Sempre mostra o método de envio gratuito, mesmo quando não aplicável.
   - `No` - Mostra o método de envio gratuito somente quando aplicável.

1. Para **[!UICONTROL Sort Order]**, informe o número que determina a posição da remessa gratuita na lista de métodos de entrega durante a finalização da compra.

   `0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.

1. Clique em **[!UICONTROL Save Config]**.

## Etapa 2: Ativar frete grátis na configuração da operadora

Conclua qualquer configuração necessária para cada transportadora que você planeja usar para o frete gratuito. Por exemplo, se o [Configuração da UPS](ups.md) estiver concluído, atualize as seguintes configurações para habilitar e configurar o frete gratuito.

1. No _[!UICONTROL Delivery Methods]_configuração, expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL UPS]**seção.

1. Definir **[!UICONTROL Free Method]** para `UPS Ground` ou outro tipo que você deseja designar para frete grátis.

1. Para exigir um pedido mínimo de frete grátis, defina **[!UICONTROL Enable Free Shipping Threshold]** para `Enable`.

   Se você optar por usar uma ordem mínima, informe a quantia necessária para **[!UICONTROL Free Shipping Amount Threshold]**.

1. Clique em **[!UICONTROL Save Config]**.
