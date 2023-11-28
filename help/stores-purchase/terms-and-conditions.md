---
title: Termos e condições para finalização da compra
description: Saiba mais sobre a funcionalidade de termos e condições que pode ser configurada para sua loja.
exl-id: 59ba6385-3cc6-43e8-b984-5c26516bba88
feature: Checkout, Compliance
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---

# Termos e condições para finalização da compra

Quando manual _Termos e condições_ Se a funcionalidade do estiver ativada, os clientes deverão concordar com os termos e condições da venda antes que a compra seja finalizada. Os Termos e condições da venda geralmente incluem informações de divulgação que podem ser exigidas por lei para sites B2C ou B2B, e descreve os direitos do comprador e do vendedor. A mensagem dos Termos e condições é exibida após as informações de pagamento, antes da mensagem _Fazer pedido_ botão.

![Termos e condições na finalização da compra](./assets/storefront-checkout-step2-terms-conditions.png){width="700" zoomable="yes"}

## Etapa 1: Ativar termos e condições para check-out

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Checkout]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Checkout Options]** seção.

   ![Opções de check-out](../configuration-reference/sales/assets/checkout-checkout-options.png){width="600" zoomable="yes"}

1. Verifique se **[!UICONTROL Enable Onepage Checkout]** está definida como `Yes`.

1. Definir **[!UICONTROL Enable Terms and Conditions]** para `Yes`.

1. Clique em **[!UICONTROL Save Config]**.

## Etapa 2: adicionar suas próprias informações de termos e condições

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Terms and Conditions]**.

   ![Grade de Termos e condições](./assets/terms-conditions.png){width="600" zoomable="yes"}

1. No canto superior direito, clique em **[!UICONTROL Add New Condition]**.

1. Insira o **[!UICONTROL Condition Name]** para referência interna.

   ![Nova Condição](./assets/terms-conditions-new.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Status]** para `Enabled`.

1. Definir **[!UICONTROL Applied]** a um dos seguintes:

   - `Automatically` - As condições são automaticamente aceitas no check-out.
   - `Manually` - Os clientes precisam aceitar manualmente as condições para fazer um pedido.

1. Definir **[!UICONTROL Show Content as]** a um dos seguintes:

   - `Text` - Exibe o conteúdo dos termos e condições como texto não formatado.
   - `HTML` - Exibe o conteúdo como HTML que pode ser formatado.

1. Selecionar cada **[!UICONTROL Store View]** onde você deseja que estes Termos e Condições sejam usados.

1. Role para baixo e preencha as informações a serem exibidas:

   - Insira o **[!UICONTROL Checkbox Text]** para ser usado como o texto do link dos Termos e condições. Por exemplo, `I understand and accept the terms and conditions of the sale`.

   - No **[!UICONTROL Content]** , insira o texto completo dos termos e condições da venda.

1. (Opcional) Insira o **[!UICONTROL Content Height (css)]** em pixels para determinar a altura da caixa de texto em que a declaração de termos e condições é exibida durante a finalização da compra.

   Por exemplo, para tornar a caixa de texto de 1 polegada de altura em uma tela de 96 dpi, digite `96`. Uma barra de rolagem será exibida se o conteúdo ultrapassar a altura da caixa.

1. Clique em **[!UICONTROL Save Condition]**.
