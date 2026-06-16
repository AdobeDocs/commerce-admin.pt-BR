---
title: Configurações de exibição de preço
description: Saiba mais sobre a exibição de impostos no catálogo, carrinho de compras, pedidos, faturas e avisos de crédito que oferecem suporte à experiência de compra do cliente.
exl-id: 6f97c474-ef6e-4ca6-899d-812c58b993ca
feature: Checkout, Invoices, Taxes
TQID: https://experienceleague.adobe.com/XIcN-vl8owiToGhM3Et2euyNWgnJdsgSl6urwJcRdLE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 519
ht-degree: 0%

---

# Configurações de exibição de preço

As configurações de exibição de preço determinam se os preços do produto e do envio incluem ou excluem imposto, ou mostram duas versões do preço: uma com e outra sem imposto.

Se o preço do produto incluir imposto, o imposto será exibido somente se houver uma regra de imposto que corresponda à origem do imposto ou se um endereço do cliente corresponder à regra de imposto. Os eventos que podem acionar uma correspondência incluem quando um cliente cria uma conta, faz logon ou gera uma estimativa de imposto e remessa do carrinho de compras.

>[!IMPORTANT]
>
>Mostrar preços que incluem e excluem imposto pode ser confuso para o cliente. Para evitar o disparo de uma mensagem de aviso, consulte as [diretrizes](international-tax-guidelines.md) para o seu país e as [configurações recomendadas](taxes.md#warning-messages) para evitar mensagens de aviso.

![Configurações de exibição de preço](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

Para obter uma descrição detalhada de cada uma dessas configurações, consulte [Configurações de Preço de Exibição](../configuration-reference/sales/tax.md#price-display-settings) no _Guia de Referência de Configuração_.

## Definir configurações de exibição de preço

Quando a configuração do cálculo de impostos, taxas e classes é concluída, os impostos são calculados de acordo com essas configurações. No entanto, a exibição de impostos no catálogo, carrinho de compras, pedidos, faturas e avisos de crédito também deve ser configurada para oferecer suporte à experiência do cliente na loja.

É uma prática recomendada exibir preços com os impostos associados (incluindo impostos ou ambos, incluindo impostos e excluindo impostos) para que os clientes saibam como esses cálculos são aplicados antes de fazer um pedido.

### Etapa 1: definir configurações de exibição de preços de catálogo

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Tax]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Price Display Settings]**.

1. Para **[!UICONTROL Display Product Prices in Catalog]**, escolha uma das seguintes opções:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

   >[!NOTE]
   >
   >Se você definir esta opção como `Including Tax`, o imposto aparecerá somente se houver uma regra de imposto que corresponda à origem do imposto ou se houver um endereço de cliente que corresponda à regra de imposto. Os eventos que podem acionar uma correspondência incluem a criação da conta do cliente, o logon ou o uso da ferramenta de estimativa de Imposto e Remessa no carrinho de compras.

1. Para **[!UICONTROL Display Shipping Prices]**, escolha uma das seguintes opções:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

Se você optar por exibir ambos os preços (com e sem imposto), a loja terá a seguinte aparência:

![Exemplo de exibição de preço incluindo impostos na vitrine](./assets/catalog-prices-tax.png){width="700" zoomable="yes"}

### Etapa 2: definir configurações de exibição do carrinho de compras

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Shopping Cart Display Settings]**.

   ![Configurações de Exibição do Carrinho de Compras](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Display Prices]**, escolha uma das seguintes opções:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Para **[!UICONTROL Display Subtotal]**, escolha uma das seguintes opções:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Para **[!UICONTROL Display Shipping Amount]**, escolha uma das seguintes opções:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Para **[!UICONTROL Display Gift Wrapping Prices]**, escolha uma das seguintes opções:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Para **[!UICONTROL Display Printed Card Prices]**, escolha uma das seguintes opções:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Para cada uma dessas opções restantes, alterne para `Yes` ou `No` de acordo com sua preferência:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

### Etapa 3: definir configurações de exibição de ordem, fatura e aviso de crédito

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]**.

   ![Configurações de Exibição de Pedidos, Faturas, Avisos de Crédito](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Display Prices]**, escolha uma das seguintes opções:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Para **[!UICONTROL Display Subtotal]**, escolha uma das seguintes opções:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Para **[!UICONTROL Display Shipping Amount]**, escolha uma das seguintes opções:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Para **[!UICONTROL Display Gift Wrapping Prices]**, escolha uma das seguintes opções:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Para **[!UICONTROL Display Printed Card Prices]**, escolha uma das seguintes opções:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Para cada uma dessas opções restantes, alterne para `Yes` ou `No` de acordo com sua preferência:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
