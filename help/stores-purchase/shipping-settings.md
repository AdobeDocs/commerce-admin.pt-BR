---
title: Configurações de envio
description: Saiba como definir as configurações de envio que definem o ponto de origem e a política de envio para sua loja.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Configurações de envio

A configuração de entrega estabelece o ponto de origem de todas as remessas, sua política de entrega e o manuseio de remessas para vários endereços.

## Ponto de origem

O ponto de origem é usado para calcular o encargo de remessas feitas de sua loja ou depósito e também determina a alíquota de imposto dos produtos vendidos. Ao calcular [impostos da UE](international-tax-guidelines.md#eu-tax-configuration), verifique se o [Cálculo de Destino de Imposto Padrão](../configuration-reference/sales/tax.md) para cada exibição de loja corresponde ao ponto de origem das Configurações de Remessa.

![Origem](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Shipping Settings]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Origin]** e conclua o seguinte:

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (e linha 2, se necessário)

1. Clique em **[!UICONTROL Save Config]**.

## Política de remessa

Uma política de envio deve explicar as regras de negócios e as diretrizes de remessa da sua empresa. Por exemplo, se você tiver regras de preço que acionam o frete grátis, poderá explicar os termos em sua política de frete.

![Política De Envio Durante O Check-Out](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

Para exibir sua política de remessa durante a finalização da compra, preencha os Parâmetros de política de remessa na configuração. O texto é exibido quando os clientes clicam em _Ver nossa política de remessa_ durante o check-out.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Shipping Settings]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Shipping Policy Parameters]**.

1. Defina **[!UICONTROL Apply Custom Shipping Policy]** como `Yes`.

1. Cole ou insira seu **[!UICONTROL Shipping Policy]** na caixa de texto.

   >[!NOTE]
   >
   >Se você usar um processador de texto para compor o texto, certifique-se de salvar o documento como um arquivo .txt para remover quaisquer caracteres de controle do texto. Em seguida, copie e cole o texto na caixa de texto Política de remessa.

   ![Parâmetros da Política de Remessa](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save Config]**.

## Vários endereços

As opções de entrega de vários endereços permitem que os clientes entreguem uma ordem a vários endereços durante a finalização da compra e determinam o número máximo de endereços para os quais uma ordem pode ser entregue.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Multishipping Settings]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Options]**.

   ![Opções de Envio de Vários Endereços](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Allow Shipping to Multiple Addresses]** como `Yes`.

1. Insira o **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**.

1. Clique em **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![Adobe Commerce B2B](../assets/b2b.svg) (Adobe Commerce B2B) Para pedidos com vários endereços de remessa, o método de pagamento [Pagamento na Conta](../b2b/enable-basic-features.md#configure-payment-on-account), mesmo se habilitado, não estará disponível durante o check-out.
