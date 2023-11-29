---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Tax]'
description: Revise as configurações no [!UICONTROL Sales] &gt; [!UICONTROL Tax] página do Administrador do Commerce.
exl-id: eb929a6c-adb2-45ac-b6ec-6239938355bf
feature: Configuration, Taxes
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1363'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Tax]

>[!NOTE]
>
>As versões 2.4.0 a 2.4.3 do Adobe Commerce e do Magento Open Source incluíam a extensão desenvolvida pelo fornecedor Vertex usada para integração com o [!UICONTROL Vertex Cloud]. A partir da versão 2.4.4, essa extensão não é mais fornecida com a versão principal e deve ser instalada e atualizada do Commerce Marketplace. O Marketplace também fornece acesso à documentação atual fornecida pelo desenvolvedor da extensão.
><br><br>
>Se você tiver a extensão agrupada ativada e configurada, deverá atualizar o arquivo composer.json como parte do processo de atualização 2.4.4 e gerenciar as atualizações de extensão a partir de agora. Consulte [Atualizar módulos e extensões](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) no _Guia de atualização_ para obter mais informações.

{{config}}

## [!UICONTROL Tax Classes]

![Classes de Impostos](./assets/tax-tax-classes.png)<!-- zoom -->

Para obter mais informações sobre como alterar essas configurações, consulte [Classes de imposto](../../stores-purchase/tax-class.md) no _Guia de experiência de compras e lojas_.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Tax Class for Shipping] | Site | Identifica a classe de imposto usada para remessa. As opções incluem todas as classes de imposto do produto disponíveis: `None` / `Taxable Goods` / `Shipping` / `Tax Exempt` |
| [!UICONTROL Tax Class for Gift Options] | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (Somente Adobe Commerce) Identifica a classe de imposto padrão usada para opções de presente. |
| [!UICONTROL Default Tax Class for Product] | Global | Identifica a classe de imposto padrão usada para produtos. |
| [!UICONTROL Default Tax Class for Customer] | Global | Identifica a classe de imposto padrão usada para clientes. |

{style="table-layout:auto"}

## [!UICONTROL Calculation Settings]

![Configurações de Cálculo](./assets/tax-calculation-settings.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | Site | Determina o método usado para calcular o imposto de um pedido. Opções:<br/>**`Unit Price`**- Os cálculos de impostos são baseados no preço unitário de cada produto.<br/>**`Row Total`** - Os cálculos de imposto são baseados no total do item de linha. <br/>**`Total`**- Os cálculos de impostos são baseados no total do pedido.<br/><br/>_** Nota:**_Se uma extensão de cálculo de imposto for instalada do Marketplace, como _Vertex Cloud_, o serviço de extensão é listado como uma opção. |
| [!UICONTROL Tax Calculation Based On] | Site | Determina se o cálculo do imposto é baseado no endereço de entrega, endereço de cobrança ou origem da remessa. Opções: `Shipping Address` / `Billing Address` / `Shipping Origin` |
| [!UICONTROL Catalog Prices] | Site | Determina se os preços de catálogo incluem ou excluem imposto. Opções: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Shipping Prices] | Site | Determina nos preços de envio se o imposto é incluído ou excluído. Opções: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Customer Tax] | Site | Determina se o imposto é aplicado antes ou depois de um desconto. Opções: `Before Discount` / `After Discount` |
| [!UICONTROL Apply Discount on Prices] | Site | Determina se os preços de desconto incluem ou excluem imposto. Opções: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Tax On] | Site | Determina se o imposto se aplica ao preço original ou a um preço personalizado, se disponível. Opções: `Custom price if available` / `Original price only` |
| [!UICONTROL Enable Cross Border Trade] | Site | Quando ativado, aplica preços consistentes entre fronteiras de regiões com diferentes taxas de imposto. Opções: `Yes` / `No` <br/><br/>**_Nota:_**O uso de comércio transfronteiriço ajusta a margem de lucro por taxa de imposto. |

{style="table-layout:auto"}

## [!UICONTROL Default Tax Destination Calculation]

![Cálculo do Destino do Imposto Padrão](./assets/tax-default-tax-destination-calculation.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Default Country] | Exibição da loja | Determina o país no qual os cálculos de imposto são baseados. |
| [!UICONTROL Default State] | Exibição da loja | Determina o estado no qual se baseiam os cálculos de imposto. Um asterisco (*) pode funcionar como curinga para indicar todos os estados dentro do país selecionado. |
| [!UICONTROL Default Post Code] | Exibição da loja | Identifica o CEP ou código postal no qual se baseiam os cálculos de imposto. Um asterisco (*) pode funcionar como curinga para indicar todos os códigos postais dentro do estado selecionado. |

{style="table-layout:auto"}

## [!UICONTROL Price Display Settings]

![Configurações de exibição de preço](./assets/tax-price-display-settings.png)<!-- zoom -->

Para obter mais informações sobre como alterar essas configurações, consulte [Definir configurações de exibição de preço](../../stores-purchase/display-settings.md#configure-price-display-settings) no _Guia de experiência de compras e lojas_.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | Exibição da loja | Determina se os preços dos produtos publicados no catálogo incluem ou excluem imposto, ou mostram duas versões do preço: uma com e outra sem imposto. Opções: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` <br/><br/>**_Nota:_**Se você definir o campo Exibir preços do produto para `Including Tax`, o imposto será exibido somente se houver uma regra de imposto que corresponda à origem do imposto ou se houver um endereço do cliente que corresponda à regra de imposto. Os eventos que podem acionar uma correspondência incluem a criação da conta do cliente, o logon ou o uso da ferramenta de estimativa de Imposto e Remessa no carrinho de compras. |
| [!UICONTROL Display Shipping Prices] | Exibição da loja | Determina se os preços de envio incluem ou excluem imposto, ou mostram duas versões do preço de envio: uma com e outra sem imposto. Opções: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart Display Settings]

![Configurações de exibição do carrinho de compras](./assets/tax-shopping-cart-display-settings.png)<!-- zoom -->

Para obter mais informações sobre como alterar essas configurações, consulte [Definir configurações de exibição do carrinho de compras](../../stores-purchase/display-settings.md#step-2-configure-shopping-cart-display-settings) no _Guia de experiência de compras e lojas_.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Display Prices] | Exibição da loja | Determina se os preços do carrinho de compras incluem ou excluem imposto, ou mostram duas versões do preço: uma com e outra sem imposto. Opções: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal|Store View] | Determina se o subtotal do carrinho de compras inclui ou exclui imposto, ou mostra duas versões do subtotal: uma com e outra sem imposto. Opções: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | Exibição da loja | Determina se o valor do frete do carrinho de compras inclui ou exclui imposto, ou mostra duas versões do valor do frete: uma com e outra sem imposto. Opções: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | Exibição da loja | Determina se uma linha extra com o valor total geral sem imposto é exibida no carrinho de compras. Opções: `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | Exibição da loja | Determina se o carrinho de compras inclui um resumo de imposto completo. Opções: `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | Exibição da loja | Determina se o carrinho de compras inclui um subtotal de imposto quando o imposto é zero. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

![Configurações de Exibição de Ordens, NFFs, Avisos de Crédito](./assets/tax-orders-invoices-credit-memos-display-settings.png)<!-- zoom -->

Para obter mais informações sobre como alterar essas configurações, consulte [Configurar definições de exibição de ordem, fatura e aviso de crédito](../../stores-purchase/display-settings.md#step-3-configure-order-invoice-and-credit-memo-display-settings) no _Guia de experiência de compras e lojas_.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Display Prices] | Exibição da loja | Determina se os preços dos documentos de venda incluem ou excluem imposto, ou se cada documento mostra duas versões do preço: uma com e outra sem imposto. Opções: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal] | Exibição da loja | Determina se o subtotal dos documentos de venda inclui ou exclui imposto, ou se cada documento mostra duas versões do subtotal: uma com e outra sem imposto. Opções: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | Exibição da loja | Determina se o valor da remessa nos documentos de venda inclui ou exclui imposto, ou se cada documento mostra duas versões do subtotal: uma com e outra sem imposto. Opções: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | Exibição da loja | Determina se uma linha extra com o valor total geral sem imposto é exibida nos documentos de venda. Opções: `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | Exibição da loja | Determina se o resumo de imposto completo aparece nos documentos de venda. Opções: `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | Exibição da loja | Determina se a seção de subtotal nos documentos de venda aparece quando nenhum imposto é cobrado. Opções: `Yes` / `No` |
| [!UICONTROL Display Gift Wrapping Prices] | Exibição da loja | ![Adobe Commerce](../../assets/adobe-logo.svg) (Somente Adobe Commerce) Determina se os preços de embalagem do presente estão incluídos no subtotal. Opções: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | Exibição da loja | ![Adobe Commerce](../../assets/adobe-logo.svg) (Somente Adobe Commerce) Determina se os preços dos cartões impressos estão incluídos no subtotal. Opções: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Fixed Product Taxes]

![Imposto Fixo do Produto](./assets/tax-fixed-product-taxes.png)<!-- zoom -->

Para obter mais informações sobre como alterar essas configurações, consulte [Imposto fixo sobre o produto (FPT)](../../stores-purchase/fixed-product-tax.md) no _Guia de experiência de compras e lojas_.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable FPT] | Site | Determina se o FPT está disponível. Opções: `Yes` / `No` |
| [!UICONTROL Display Prices in Product Lists] | Site | Controla a exibição de FPT em listas de produtos. Opções:<br/> **`Including FPT Only`** - Os preços exibidos incluem impostos fixos sobre o produto. O valor FPT não é exibido separadamente.<br/>**`Including FPT and FPT description`**- Os preços exibidos incluem impostos fixos sobre o produto. O valor de FPT é exibido separadamente.<br/>**`Excluding FPT. Including FPT description and final price`** - Os preços exibidos não incluem impostos fixos sobre o produto. O valor de FPT é exibido separadamente.<br/>**`Excluding FPT`**- Os preços exibidos não incluem impostos fixos sobre o produto. O valor FPT não é exibido separadamente. |
| Exibir preço na página de exibição do produto | Site | Controla a exibição de FPT na página do produto. Opções:<br/> **`Including FPT Only`** - Os preços exibidos incluem impostos fixos sobre o produto. O valor FPT não é exibido separadamente.<br/>**`Including FPT and FPT description`**- Os preços exibidos incluem impostos fixos sobre o produto. O valor de FPT é exibido separadamente.<br/>**`Excluding FPT. Including FPT description and final price`** - Os preços exibidos não incluem impostos fixos sobre o produto. O valor de FPT é exibido separadamente.<br/>**`Excluding FPT`**- Os preços exibidos não incluem impostos fixos sobre o produto. O valor FPT não é exibido separadamente. |
| [!UICONTROL Display Prices in Sales Modules] | Site | Controla a exibição de FPT no carrinho de compras e durante o check-out. Opções:<br/> **`Including FPT Only`** - Os preços exibidos incluem impostos fixos sobre o produto. O valor FPT não é exibido separadamente.<br/>**`Including FPT and FPT description`**- Os preços exibidos incluem impostos fixos sobre o produto. O valor de FPT é exibido separadamente.<br/>**`Excluding FPT. Including FPT description and final price`** - Os preços exibidos não incluem impostos fixos sobre o produto. O valor de FPT é exibido separadamente.<br/>**`Excluding FPT`**- Os preços exibidos não incluem impostos fixos sobre o produto. O valor FPT não é exibido separadamente. |
| [!UICONTROL Display Prices in Emails] | Site | Controla a exibição de FPT no email. Opções:<br/> **`Including FPT Only`** - Os preços exibidos incluem impostos fixos sobre o produto. O valor FPT não é exibido separadamente.<br/>**`Including FPT and FPT description`**- Os preços exibidos incluem impostos fixos sobre o produto. O valor de FPT é exibido separadamente.<br/>** Excluindo FPT. Incluindo a descrição FPT e o preço final **- Os preços exibidos não incluem impostos fixos sobre o produto. O valor de FPT é exibido separadamente.<br/>**`Excluding FPT`** - Os preços exibidos não incluem impostos fixos sobre o produto. O valor FPT não é exibido separadamente. |
| [!UICONTROL Apply Discounts to FPT] | Site | Determina se os descontos podem ser aplicados ao valor FPT. Opções: `Yes` / `No` |
| [!UICONTROL FPT Tax Configuration] | Site | Determina como o imposto FPT é calculado. Opções: <br/>**`Not Taxed`**- Selecione esta opção se sua jurisdição de tributação não tributar FPT. (Por exemplo, Califórnia.)<br/>**`Taxed`** - Selecione esta opção se sua jurisdição de tributação tributa FPT. (Por exemplo, Canadá.) <br/>**`Loaded and Displayed with Tax`**- Clique nesta opção se FPT for adicionado ao total do pedido antes de aplicar o imposto. (Por exemplo, países da UE.) |
| [!UICONTROL Include FPT in Subtotal] | Site | Determina se o FPT é incluído no subtotal do carrinho de compras. Opções: <br/>**`Yes`**- Inclui FPT no subtotal do carrinho de compras.<br/>**`No`** - O FPT não está incluído no subtotal e é colocado depois do subtotal no carrinho de compras. |

{style="table-layout:auto"}
