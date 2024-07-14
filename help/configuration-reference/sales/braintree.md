---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Braintree]'
description: Revise as configurações para a seção [!UICONTROL Braintree] na página [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] do Administrador do Commerce.
exl-id: cf08bc4d-8d88-45e7-af71-f1ff90023766
feature: Configuration, Payments
source-git-commit: 5488a0a991f497059ea39fbbc8a08fd8f546e1ac
workflow-type: tm+mt
source-wordcount: '2603'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Braintree]

>[!IMPORTANT]
>
>**Migração para o Commerce 2.4:**<br/>
>Para versões do Adobe Commerce e do Magento Open Source anteriores à versão 2.4.0, foi recomendado que os comerciantes instalassem e configurassem a extensão de integração de pagamento Braintree oficial do [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=braintree) para substituir a integração principal. A partir da versão 2.4.0, a extensão será incluída na versão principal.
><br/><br/>
>Ao migrar para o Commerce 2.4, os comerciantes precisam desinstalar a extensão distribuída no Marketplace (`paypal/module-braintree` ou `gene/module-braintree`) e atualizar todas as personalizações de código para usar o namespace `PayPal_Braintree` em vez de `Magento_Braintree`. As configurações da extensão agrupada para Commerce e da extensão distribuída no Commerce Marketplace são mantidas. Os pagamentos feitos com essas versões da extensão são capturados, anulados ou reembolsados normalmente.
><br/><br/>
>Se você estiver atualizando para o Commerce 2.4.0 e não usar a extensão de Commerce Marketplace recomendada na versão 2.3.x anterior, o recurso de vários endereços não funcionará com a versão 2.4.0 do Braintree. Quando um comprador seleciona _entregar para vários endereços_ , o método de pagamento Braintree não é exibido. A extensão Commerce Marketplace anteriormente recomendada para 2.3.x tem esse problema de endereço múltiplo.

{{config}}

## [!UICONTROL Basic Braintree Settings]

![Configurações Básicas de Braintree](./assets/payment-methods-braintree-basic-config.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Title] | Exibição da loja | Valor padrão: `Credit Card` (Braintree) |
| [!UICONTROL Environment] | Exibição da loja | Opções: `Sandbox` / `Production` |
| [!UICONTROL Payment Action] | Exibição da loja | Determina a ação tomada pelo Braintree quando um pagamento é processado. Opções: <br/>**`Authorize`**- Os fundos no cartão de crédito do cliente estão autorizados, mas não foram transferidos da conta. Um pedido é criado no Administrador da loja. Posteriormente, você pode capturar a venda e criar uma fatura.<br/>**`Intent Sale`** (anteriormente `Authorize and Capture` em versões anteriores) - Os fundos no cartão de crédito do cliente são autorizados e capturados pelo Braintree, e um pedido e uma fatura são criados no Administrador da loja. |
| [!UICONTROL Sandbox Merchant ID] | Exibição da loja | Esse é o identificador exclusivo de toda a sua conta de gateway de sandbox. Também conhecida como _ID pública_ ou _ID de produção_, sua ID de comerciante é diferente para seus gateways de produção e sandbox. Este campo aparece quando o campo _[!UICONTROL Environment]_está definido como `Sandbox`. |
| [!UICONTROL Sandbox Public Key] | Exibição da loja | Esse é o identificador público específico do usuário que restringe o acesso a dados criptografados. Cada usuário associado ao seu gateway de Braintree de sandbox tem sua própria chave pública de sandbox. Este campo aparece quando o campo _[!UICONTROL Environment]_está definido como `Sandbox`. |
| [!UICONTROL Sandbox Private Key] | Exibição da loja | Esse é o identificador privado específico do usuário que restringe o acesso a dados criptografados. Cada usuário associado ao seu gateway de Braintree de sandbox tem sua própria chave privada para a sandbox. Este campo aparece quando o campo _[!UICONTROL Environment]_está definido como `Sandbox`. |
| [!UICONTROL Merchant ID] | Exibição da loja | Esse é o identificador exclusivo de toda a conta do gateway, incluindo as várias contas de comerciante que podem estar no gateway. Também conhecida como _ID pública_ ou _ID de produção_, sua ID de comerciante é diferente para seus gateways de produção e sandbox. Este campo aparece quando o campo _[!UICONTROL Environment]_está definido como `Production`. |
| [!UICONTROL Public Key] | Exibição da loja | Esse é o identificador público específico do usuário que restringe o acesso a dados criptografados. Cada usuário associado ao gateway Braintree tem sua própria chave pública. Este campo aparece quando o campo _[!UICONTROL Environment]_está definido como `Production`. |
| [!UICONTROL Private Key] | Exibição da loja | Esse é o identificador privado específico do usuário que restringe o acesso a dados criptografados. Cada usuário associado ao seu gateway Braintree tem sua própria chave privada. Este campo aparece quando o campo _[!UICONTROL Environment]_está definido como `Production`. |
| [!UICONTROL Enable Card Payments] | Site | Determina se o método de pagamento por cartão de crédito Braintree está disponível para seus clientes como um método de pagamento. Opções: `Yes` / `No` |
| [!UICONTROL Enable Vault for Card Payments] | Site | Quando ativado, o fornece armazenamento seguro para informações de pagamento do cliente, de modo que os clientes não precisam inserir novamente as informações de cartão de crédito para cada compra. Opções: `Yes` / `No` |
| [!UICONTROL Enable Vault CVV Reverification] | Site | Quando ativada, a validação é feita para a configuração de regras CVV na sua conta Braintree. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Braintree Settings]

![Configurações avançadas do Braintree](./assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Vault Title] | Site | Um título descritivo para referência que identifica o cofre no qual as informações do cartão do cliente estão armazenadas. |
| [!UICONTROL Merchant Account ID] | Site | A ID da Conta do Comerciante que deve ser associada às transações Braintree deste site. Se deixado em branco, a conta padrão do comerciante da conta do Braintree é usada. |
| [!UICONTROL Enable Checkout Express Payments] | Site | Fornece uma experiência de finalização mais rápida com opções de Pagamento Expresso no início do processo de finalização, incluindo PayPal, PayLater, Apple Pay e Google Pay. Opções: `Yes` / `No` |
| [!UICONTROL Skip Fraud Checks on Admin Orders] | Site | Impede que a transação seja enviada para avaliação como parte das verificações de [!DNL Advanced Fraud Tools], em pedidos feitos pelo administrador apenas quando definido como `Yes`.<br/>Opções: `Yes` / `No` |
| [!UICONTROL Bypass Fraud Protection Threshold] | Site | `Advanced Fraud Protection` verificações são ignoradas quando o valor limite é atingido ou excedido. Deixar esse campo em branco desativa essa opção. |
| [!UICONTROL Debug] | Site | Determina se as comunicações entre o sistema Braintree e o armazenamento são gravadas em um arquivo de log. Opções: `Yes` / `No` |
| [!UICONTROL CVV Verification] | Site | Determina se os clientes devem fornecer o código de segurança de três dígitos da parte traseira de um cartão de crédito. Opções: `Yes` / `No` |
| [!UICONTROL Send Card Line Items] | Site | Envie os itens de linha do carrinho para todos os métodos de pagamento. Opções: `Yes` / `No` |
| [!UICONTROL Credit Card Types] | Site | Especifica cada cartão de crédito que você aceita como pagamento por meio do Braintree. Mantenha pressionada a tecla `Ctrl` (ou `Command` no Mac) para selecionar uma combinação de cartões. Opções: `American Express` / `Visa` / `MasterCard` / `Discover` / `JCB` / `Diners` / `Maestro International` |
| [!UICONTROL Sort Order] | Site | Determina a ordem em que o Braintree está listado com outros métodos de pagamento durante o check-out. |

## [!UICONTROL Braintree Webhooks Settings]

![Configurações de Webhooks do Braintree](./assets/payment-methods-braintree-webhooks-config.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Webhook] | Site | Para ativar a funcionalidade de webhook para proteção contra fraude, pagamentos ACH, métodos de pagamento locais e disputas. Opções: `Yes` / `No` |
| [!UICONTROL Fraud Protection URL] | Site | Adicione esta URL à sua Conta Braintree como o [!UICONTROL Webhook Destination URL]. **Esta URL deve ser segura e estar acessível publicamente.** |
| [!UICONTROL Fraud Protection Approve Order Status] | Site | Quando a proteção contra fraude é aprovada pelo Braintree, o status do pedido selecionado é atribuído ao pedido do Commerce. Este status é usado para atualizar o status do pedido onde o método de pagamento ACH é usado e quando ele é movido para `SETTLED` em Braintree. |
| [!UICONTROL Fraud Protection Reject Order Status] | Site | Quando a proteção contra fraude é rejeitada pelo Braintree, o status do pedido selecionado é atribuído ao pedido do Commerce. Este status é usado para atualizar o status da ordem em que o método de pagamento da ACH é usado e quando `SETTLEMENT` está `DECLINED` em Braintree. |

{style="table-layout:auto"}

## [!UICONTROL Country Specific Settings]

![Configurações específicas do país](./assets/payment-methods-braintree-country-specific-config.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Payment from Applicable Countries] | Site | Determina se você aceita pagamentos processados por Braintree de todos os países ou somente de países específicos. Opções: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site | Se aplicável, identifica os países específicos dos quais você aceita pagamentos processados por Braintree. |
| [!UICONTROL Country Specific Credit Card Types] | Site | Identifica os cartões de crédito aceitos por país para pagamentos processados por Braintree. Um registro é salvo para cada país. Opções: <br/>**`Country`**- Escolha o país.<br/>**`Allowed Card Types`** - Selecione cada cartão de crédito aceito do país como pagamento por meio do Braintree. <br/>**`Add`**- Adicione uma linha para permitir cartões de crédito de outro país.<br/>**`Action`** - Exclui o registro de cartões de crédito permitidos para o país. |

{style="table-layout:auto"}

## [!UICONTROL ACH through Braintree]

![ACH até Braintree](./assets/payment-methods-braintree-ach-config.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled ACH Direct Debit] | Site | Determina se [!DNL ACH Direct Debit] está incluído como um método de pagamento por meio do Braintree. Opções: `Yes` / `No` |
| [!UICONTROL Enable Vault for ACH Direct Debit] | Site | Os clientes podem compartimentar/armazenar seu método de pagamento de Débito Direto ACH de uso único para uso futuro. Depois que os detalhes do pagamento forem salvos, o cliente poderá usar o método de pagamento Débito Direto ACH sem inserir os dados novamente ou autenticar novamente suas informações de pagamento. Opções: `Yes` / `No` |
| [!UICONTROL Sort Order] | Site | Determina a ordem em que [!DNL ACH Direct Debit] está listado com outros métodos de pagamento durante o check-out. |

{style="table-layout:auto"}

## [!UICONTROL Apple Pay through Braintree]

![Pagar através do Braintree](./assets/payment-methods-braintree-applepay-config.png)<!-- zoom --> da Apple

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable ApplePay through Braintree] | Site | Determina se o Apple Pay está incluído como um método de pagamento através do Braintree. Opções: `Yes` / `No` <br/><br/> O domínio deve ser [verificado primeiro na Conta do Braintree](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3). |
| [!UICONTROL Enable Vault for ApplePay] | Site | Os clientes podem arquivar/armazenar seu método de pagamento Apple Pay para uso futuro. Depois que os detalhes do pagamento forem salvos, o cliente poderá usar o Apple Pay sem inserir os dados novamente ou autenticar novamente suas informações de pagamento. Opções: `Yes` / `No` |
| [!UICONTROL Payment Action] | Site | Determina a ação tomada pelo Braintree quando um pagamento é processado. Opções: <br/>**`Authorize`**- Os fundos no cartão do cliente são autorizados, mas não transferidos da conta do cliente. Um pedido é criado no Administrador da loja. Posteriormente, você pode capturar a venda e criar uma fatura.<br/>**`Intent Sale`** - Os fundos no cartão do cliente são autorizados e capturados pelo Braintree, e um pedido e uma fatura são criados no Administrador da loja. **_Observação:_** este era `Authorize and Capture` na versão 2.3.x e em versões anteriores. |
| [!UICONTROL Merchant Name] | Exibição da loja | Rótulo exibido aos clientes no pop-up ApplePay. |
| [!UICONTROL Sort Order] | Site | Determina a ordem em que o Apple Pay é listado com outros métodos de pagamento durante o checkout. |

{style="table-layout:auto"}

## [!UICONTROL Local Payment Methods]

![Métodos de pagamento locais](./assets/payment-methods-braintree-local-payment-config.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled Local Payment Methods] | Site | Determina se o Método de Pagamento Local será incluído como um método de pagamento por meio do Braintree. Opções: `Yes` / `No` |
| [!UICONTROL Title] | Site | Rótulo que aparece na seção do método de pagamento de finalização da compra. Valor padrão: `Local Payments` |
| [!UICONTROL Fallback Button Text] | Site | Digite o texto a ser usado para o botão que aparece na página de Braintree de fallback que leva os clientes de volta ao site. Valor padrão: `Complete Checkout` |
| [!UICONTROL Redirect on Fail] | Site | Especifica o URL para o qual os clientes devem ser redirecionados quando as transações do método de pagamento local forem canceladas, reprovadas ou encontrarem erros. Deve ser a página de pagamento do check-out (por exemplo, `https://www.domain.com/checkout#payment`). |
| [!UICONTROL Allowed Payment Method] | Site | Selecione o método de Pagamento local a ser ativado. Opções: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (ainda não suportado) |
| [!UICONTROL Sort Order] | Site | Determina a ordem em que o Método de Pagamento Local será listado com outros métodos de pagamento durante a finalização da compra. |

{style="table-layout:auto"}

>[!NOTE]
>
>A extensão de Braintree agrupada não oferece suporte a todos os métodos de pagamento locais listados na [documentação do desenvolvedor de Braintree](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). Outros métodos de pagamento locais estão em desenvolvimento para serem compatíveis em versões futuras.

## [!UICONTROL GooglePay through Braintree]

![GooglePay por Braintree](./assets/payment-methods-braintree-googlepay-config.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled GooglePay through Braintree] | Site | Determina se o pagamento [!DNL Google Pay] será incluído como um método de pagamento por meio do Braintree. Opções: `Yes` / `No` |
| [!UICONTROL Enable Vault for GooglePay] | Site | Os clientes podem arquivar/armazenar seu método de pagamento Google Pay para uso futuro. Depois que os detalhes do pagamento forem salvos, o cliente poderá usar o Google Pay sem inserir os dados novamente ou autenticar novamente suas informações de pagamento. Opções: `Yes` / `No` |
| [!UICONTROL Payment Action] | Site | Determina a ação tomada pelo Braintree quando um pagamento é processado. Opções: <br/>**`Authorize`**- Os fundos no cartão do cliente são autorizados, mas não transferidos da conta do cliente. Um pedido é criado no Administrador da loja. Posteriormente, você pode capturar a venda e criar uma fatura.<br/>**`Intent Sale`** - Os fundos no cartão do cliente são autorizados e capturados pelo Braintree, e um pedido e uma fatura são criados no Administrador da loja. **_Observação:_** este era `Authorize and Capture` na versão 2.3.x e em versões anteriores. |
| [!UICONTROL Button Color] | Site | Determina a cor do botão [!DNL Google Pay]. Opções: `White` / `Black` |
| [!UICONTROL Merchant ID] | Exibição da loja | A ID fornecida pelo Google deve ser inserida aqui. |
| [!UICONTROL Accepted Cards] | Site | Selecione o tipo de cartões que um cliente pode usar para fazer um pedido usando o [!DNL Google Pay]. |
| [!UICONTROL Sort Order] | Site | Determina a ordem em que o Google Pay é listado com outros métodos de pagamento durante o checkout. |

{style="table-layout:auto"}

## [!UICONTROL Venmo through Braintree]

![Venmo até Braintree](./assets/payment-methods-braintree-venmo-config.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Venmo through Braintree] | Site | Determina se [!DNL Venmo] está incluído como um método de pagamento por meio do Braintree. Opções: `Yes` / `No` |
| [!UICONTROL Enable Vault for Venmo] | Site | Os clientes podem arquivar/armazenar seu método de pagamento Venmo para uso futuro. Depois que os detalhes do pagamento forem salvos, o cliente poderá usar o método de pagamento Venmo sem inserir os dados novamente ou autenticar novamente suas informações de pagamento. Opções: `Yes` / `No` |
| [!UICONTROL Payment Action] | Site | Determina a ação tomada pelo Braintree quando um pagamento é processado. Opções: <br/>**`Authorize`**- Os fundos no cartão do cliente são autorizados, mas não transferidos da conta do cliente. Um pedido é criado no Administrador da loja. Posteriormente, você pode capturar a venda e criar uma fatura.<br/>**`Intent Sale`** - Os fundos no cartão do cliente são autorizados e capturados pelo Braintree, e um pedido e uma fatura são criados no Administrador da loja. **_Observação:_** era _Autorizar e Capturar_ na versão 2.3.x e em versões anteriores. |
| [!UICONTROL Sort Order] | Site | Determina o pedido de listagem do Venmo com outros métodos de pagamento durante o check-out. |

{style="table-layout:auto"}

## [!UICONTROL PayPal through Braintree]

![PayPal por Braintree](./assets/payment-methods-braintree-paypal-config.png){width="550" zoomable="yes"}

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable PayPal through Braintree] | Site | Determina se o PayPal é incluído como um método de pagamento por meio do Braintree. Opções: `Yes` / `No` |
| [!UICONTROL Enable PayPal Credit through Braintree] | Site | Determina se o Crédito do PayPal é incluído como um método de pagamento por meio do Braintree. Opções: `Yes` / `No`. Este campo fica visível quando `Enable PayPal through Braintree` está definido como `Yes` |
| [!UICONTROL Enable PayPal PayLater through Braintree] | Site | Determina se o PayPal PayLater deve ser incluído como um método de pagamento através do Braintree. Opções: `Yes` / `No`. Este campo fica visível quando `Enable PayPal through Braintree` está definido como `Yes` |
| [!UICONTROL Title] | Exibição da loja | O rótulo que identifica o PayPal por meio do Braintree para clientes durante o checkout. Valor padrão: `PayPal` |
| [!UICONTROL Vault Enabled] | Site | Quando ativado, fornece armazenamento seguro para informações de pagamento do cliente, para que os clientes não precisem inserir novamente suas informações do PayPal para cada compra. Opções: `Yes` / `No` |
| [!UICONTROL Send Cart Line Items for PayPal] | Site | Envie os itens de linha (itens de pedido) para PayPal juntamente com Cartões-presente, Empacotamento de presente para itens, Empacotamento de presente para pedido, Crédito da loja, Envio e Imposto como itens de linha. Opções: `Yes` / `No` |
| [!UICONTROL Sort Order] | Site | Um número que determina a ordem na qual o PayPal por Braintree é listado com outros métodos de pagamento durante o check-out. |
| [!UICONTROL Override Merchant Name] | Exibição da loja | Um nome alternativo que pode ser usado para identificar o comerciante para cada exibição de loja. |
| [!UICONTROL Payment Action] | Site | Determina a ação tomada pelo PayPal pelo Braintree quando um pagamento é processado. Opções: <br/>**`Authorize`**- Os fundos no cartão do cliente são autorizados, mas não transferidos da conta do cliente. Um pedido é criado no Administrador da loja. Posteriormente, você pode capturar a venda e criar uma fatura.<br/>**`Authorize and Capture`** - Os fundos no cartão do cliente são autorizados e capturados pelo PayPal através do Braintree, e um pedido e uma fatura são criados no Admin da loja. |
| [!UICONTROL Payment from Applicable Countries] | Site | Determina se você aceita pagamentos processados pelo PayPal por Braintree de todos os países ou somente de países específicos. Opções: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site | Se aplicável, identifica os países específicos dos quais você aceita pagamentos processados por Braintree. |
| [!UICONTROL Require Customer's Billing Address] | Site | Determina se o endereço de cobrança do cliente é necessário para enviar um pedido. Opções: `Yes` / `No` |
| [!UICONTROL Debug] | Site | Determina se as comunicações entre o PayPal pelo sistema Braintree e sua loja são gravadas em um arquivo de log. Opções: `Yes` / `No` |
| [!UICONTROL Display on Shopping Cart] | Site | Determina se o botão PayPal aparece no [minicarrinho](../../stores-purchase/cart-configuration.md#mini-cart) e na página [carrinho de compras](../../stores-purchase/cart.md). Opções: `Yes` / `No` |

{style="table-layout:auto"}

>[!NOTE]
>
>**[!DNL PayPal Credit]** ou **[!DNL PayPal PayLater]** pode ser habilitado. Ambos os métodos não podem ser ativados ao mesmo tempo.

### [!UICONTROL Styling]

![Estilo do PayPal](./assets/payment-methods-braintree-paypal-styling.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Location] | Site | Determina onde as mensagens e os botões do PayPal são renderizados na loja. Opções: `Mini-Cart and Cart Page` / `Checkout Page` / `Product Page` |

{style="table-layout:auto"}

**[!UICONTROL Mini-Cart and Cart Page]**

A opção e as configurações desta seção variam de acordo com a configuração no campo _[!UICONTROL Location]_.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL PayPal Button Type] | Site | Define o botão para um dos três tipos: `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button` |

**[!UICONTROL PayPal Button]**

As opções e configurações desta seção variam de acordo com o tipo de botão selecionado no campo _[!UICONTROL PayPal Button Type]_.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Show PayPal Button] | Site | Determina o local do botão PayPal no local selecionado. Opções: `Yes` / `No` |
| [!UICONTROL Button Label] | Site | Determina o rótulo do botão PayPal. Opções: `Paypal` / `Checkout` / `Buy Now` / `Pay` |
| [!UICONTROL Color] | Site | Determina a cor do botão PayPal. Opções: `Blue` / `Black` / `Gold` / `Silver` |
| [!UICONTROL Shape] | Site | Determina a forma do botão PayPal. Opções: `Pill` / `Rectangle` |
| [!UICONTROL Size(Deprecated)] | Site | Determina o tamanho do botão PayPal. Opções: `Medium` / `Large` / `Responsive` |

{style="table-layout:auto"}

>[!NOTE]
>
>O campo de configuração **[!DNL Size(Deprecated)]** está obsoleto e não está sendo usado para estilizar os botões PayPal.

**[!UICONTROL PayLater Messaging]**

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Show PayLater Messaging] | Site | Habilita as mensagens do PayLater no local selecionado. Opções: `Yes` / `No`. Quando habilitado, ele exibe mensagens do PayLater para ofertas disponíveis ([restrições se aplicam](https://developer.paypal.com/docs/checkout/pay-later/us/)). |
| [!UICONTROL Message Layout] | Site | Determina o layout de mensagem do PayLater. Opções: `Text` / `Flex` |
| [!UICONTROL Logo] | Site | Determina o tipo de logotipo usado para o botão PayPal. Opções: `Inline` / `Primary` / `Alternative` / `None` |
| [!UICONTROL Logo Position] | Site | Determina a posição do logotipo do botão PayPal. Opções: `Left` / `Right` / `Top` |
| [!UICONTROL Text Color] | Site | Determina a cor do texto do botão PayPal. Opções: `Black` / `White` / `Monochrome` / `Grayscale` |

{style="table-layout:auto"}

Quando essas opções são definidas, você pode visualizar os botões do PayPal e as mensagens do PayLater. Há controles que você pode usar para aplicar as configurações ou redefinir os valores:

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Apply] | Site | Armazena as configurações de estilo selecionadas para mensagens de botões e PayLater e as aplica ao local atual e ao tipo de botão atual. |
| [!UICONTROL Apply to All Buttons] | Site | Armazena as configurações de estilo selecionadas para botões e valores de mensagens do PayLater e as aplica a todos os tipos e locais de botão. |
| [!UICONTROL Reset to Recommended Defaults] | Site | Retorna as configurações de estilo aos valores padrão recomendados para mensagens de botões e PayLater e os aplica a todos os tipos e locais de botões. |

{style="table-layout:auto"}

## Configurações de verificação segura 3d

![Configurações de Verificação Segura da 3D](./assets/payment-methods-braintree-3d-secure-verify-config.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL 3D Secure Verification] | Site | Determina se uma transação deve passar por um processo de verificação extra quando o cliente estiver inscrito em um programa como _Verificado pela VISA_. Opções: `Yes` / `No` |
| [!UICONTROL Always request 3DS] | Site | Desafie a solicitação do 3D Secure sempre para todas as transações. Opções: `Yes` / `No` |
| [!UICONTROL Threshold Amount] | Site | Determina o valor máximo do pedido autorizado para processamento em um único pedido. o Braintree recusará a autorização se o valor do pedido exceder esse valor limite. |
| [!UICONTROL Verify for Applicable Countries] | Site | Determina os países onde o pagamento deve ser verificado. Opções: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Verify for Specific Countries] | Site | Se aplicável, identifica os países específicos a partir dos quais o pagamento por Braintree deve ser verificado. |

{style="table-layout:auto"}

## [!UICONTROL Dynamic Descriptors]

![Descritores dinâmicos](./assets/payment-methods-braintree-dynamic-config.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Name] | Exibição da loja | Há duas partes no descritor Nome, separadas por um asterisco (*). A primeira parte do descritor identifica a empresa ou o DBA e a segunda identifica o produto. Por exemplo: `company*myproduct` <br/><br/>O comprimento das partes Empresa e Produto do descritor pode ser alocado das seguintes maneiras, para um comprimento combinado de até 22 caracteres: <br/>**`Option 1`**- A empresa deve ter três caracteres / O produto pode ter até 18 caracteres<br/>**`Option 2`** - A empresa deve ter sete caracteres / O produto pode ter até 14 caracteres <br/>**`Option 3`**- A empresa deve ter 12 caracteres / O produto pode ter até nove caracteres |
| [!UICONTROL Phone] | Exibição da loja | O descritor de telefone deve ter de dez a 14 caracteres e pode incluir apenas números, traços, parênteses e pontos. Por exemplo: `9999999999` `(999) 999-9999` `999.999.9999` |
| [!UICONTROL URL] | Exibição da loja | O descritor de URL representa seu nome de domínio e pode ter até 13 caracteres. Por exemplo: `company.com` |

{style="table-layout:auto"}
