---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Checkout]'
description: Revise as configurações no [!UICONTROL Sales] &gt; [!UICONTROL Checkout] página do Administrador do Commerce.
exl-id: a912beb0-37a9-407b-83bd-dc6cd0554dc4
feature: Configuration, Checkout
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Checkout]

{{config}}

## [!UICONTROL Checkout Options]

>[!NOTE]
>
>[!BADGE 2.4.6-p1]{type=Informative tooltip="Atualizações em 2.4.6-p1"}[!BADGE 2.4.7-beta1]{type=Informative tooltip="Atualizações na versão 2.4.7-beta1"}[2.4.7-beta2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html) e [2.4.6-p3](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html) Versões do que fornecem aprimoramentos de segurança para a funcionalidade descrita. Se você estiver usando uma dessas versões, revise as notas de versão.

![Opções de check-out](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://docs.magento.com/user-guide/sales/checkout-options.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Onepage Checkout] | Exibição da loja | Determina se [Check-out de uma página](../../stores-purchase/checkout-process.md#checkout-options) é o formato de check-out padrão. Opções: `Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | Exibição da loja | Determina se os convidados podem passar [check-out sem registro](../../stores-purchase/checkout-guest.md) para uma conta com seu armazenamento. Opções: `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | Exibição da loja | Determina se os clientes devem concordar com os [Termos e condições](../../stores-purchase/terms-and-conditions.md) da venda antes de efetuar uma compra. Opções: `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | Exibição da loja | Determina o local do endereço de cobrança durante a finalização da compra. Opções: `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | Exibição da loja | Determina o número máximo de itens que podem aparecer no _Resumo do pedido_ durante o check-out. O padrão é `10`. |
| [!UICONTROL Enable Address Search] | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (Somente no Adobe Commerce) Determina se os clientes podem usar [pesquisa de endereço](../../stores-purchase/checkout-address-search.md) funcionalidade para as etapas Entrega e Revisão e Pagamentos. Quando isso estiver ativado, use Limite de número de endereços do cliente para definir o número de endereços salvos necessários para ativar essa funcionalidade durante a finalização da compra. Opções: `Yes` / `No` |
| Limite de Número de Endereços do Cliente | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (Somente no Adobe Commerce) Quando a pesquisa de endereço está ativada, determina o número de endereços salvos necessários para ativar essa funcionalidade durante o check-out. Quando o número de endereços salvos do cliente atingir ou exceder esse número, somente o endereço padrão será renderizado no _Envio_ e _Revisão e Pagamentos_ etapas. O cliente pode usar uma função de pesquisa para alterar o endereço selecionado. O padrão é `10`. |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart]

![Carrinho de compras](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://docs.magento.com/user-guide/sales/cart-configuration.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | Site | Determina o [tempo de vida de um preço cotado](../../stores-purchase/cart-configuration.md#quote-lifetime), em dias. |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | Exibição da loja | Determina se a variável [página do carrinho de compras aparece](../../stores-purchase/cart-configuration.md#redirect-to-cart) imediatamente após um produto ser adicionado ao carrinho. Opções: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | Exibição da loja | Determina o número de itens no carrinho de compras antes que o pager seja acionado. Valor padrão: `20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | Exibição da loja | Indica se [itens de venda cruzada](../../catalog/related-products-up-sells-cross-sells.md#cross-sells) são exibidos no carrinho de compras, fornecendo opções de venda adicionais aos clientes. Opções: `Yes` (padrão) / `No` |
| [!UICONTROL Grouped Product Image] | Exibição da loja | Determina o [miniatura](../../stores-purchase/cart-configuration.md#cart-thumbnails) imagem que aparece para um [produto agrupado](../../catalog/product-create-grouped.md) no carrinho. Opções: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | Exibição da loja | Determina o [miniatura](../../stores-purchase/cart-configuration.md#cart-thumbnails) imagem que aparece para um produto configurável no carrinho de compras. Opções: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | Exibição da loja | Determina a idade máxima da cotação em minutos quando visualizada do carrinho de compras. |
| [!UICONTROL Enable Clear Shopping Cart] | Site | Determina se o carrinho de compras exibe a opção para que os usuários limpem o conteúdo do carrinho em uma única ação. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL My Cart Link]

![Meu link do carrinho](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | Site | Determina o valor que aparece entre parênteses após o link Meu carrinho. Opções: `Display number of items in cart` / `Display item quantities` |

{style="table-layout:auto"}

## Mini carrinho

![Mini carrinho](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | Exibição da loja | Determina se o mini carrinho aparece nas páginas da loja quando o ícone do carrinho no cabeçalho é clicado. A exibição do minicarrinho depende do tema. Opções: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | Exibição da loja | Determina o número de itens que podem aparecer no minicarrinho antes que a barra de rolagem seja acionada. Padrão: `5` |
| [!UICONTROL Maximum Number of Items to Display] | Exibição da loja | Determina o número máximo de itens que podem aparecer no minicarrinho. Padrão: `10` |

{style="table-layout:auto"}

## [!UICONTROL Payment Failed Emails]

![Emails de pagamento com falha](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://docs.magento.com/user-guide/sales/checkout-payment-failed-emails.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | Exibição da loja | Identifica o contato da loja que recebe emails de Pagamento com Falha. Receptor padrão: `General Contact` |
| [!UICONTROL Payment Failed Email Sender] | Exibição da loja | Identifica o contato da loja que aparece como o remetente da mensagem de emails Payment Failed. Remetente padrão: `General Contact` |
| [!UICONTROL Payment Failed Template] | Exibição da loja | Identifica o modelo usado para emails de Pagamento com Falha. Modelo padrão: `Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | Exibição da loja | Fornece o endereço de email de qualquer pessoa para receber uma cópia de um email de Pagamento com Falha. Separe vários endereços com uma vírgula. |
| [!UICONTROL Send Payment Failed Copy Method] | Exibição da loja | Indica o método de email usado para enviar a cópia. Opções: <br />**`Bcc`**- Envia uma cópia de cortesia às cegas incluindo o recipient no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.<br />**`Separate Email`** - Envia a cópia como um email separado. |

{style="table-layout:auto"}
