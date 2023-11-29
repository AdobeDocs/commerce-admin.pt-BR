---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Google API]'
description: Revise as configurações no [!UICONTROL Sales] &gt; [!UICONTROL Google API] página do Administrador do Commerce.
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Exibição da loja | Habilita [!DNL Google Analytics] para sua loja. Opções: `Yes` / `No` |
| [!UICONTROL Account Type] | Exibição da loja | ![Adobe Commerce](../../assets/adobe-logo.svg) (Somente no Adobe Commerce) Determina as opções de configuração de acordo com o tipo de conta do Google Analytics. Opções: Universal Analytics (padrão) / Google Tag Manager |
| [!UICONTROL Account Number] | Exibição da loja | O número da conta, ou código de rastreamento, que foi atribuído quando você criou o [!DNL Google Analytics] conta. |
| [!UICONTROL Anonymize IP] | Exibição da loja | Determina se as informações de identificação são removidas dos endereços IP exibidos no [!DNL Google Analytics] resultados. |
| [!UICONTROL Enable Content Experiments] | Exibição da loja | Ativa [Experimentos de conteúdo do Google](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207), que pode ser usada para testar até dez versões diferentes da mesma página. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics - Tipo de conta do Google Tag Manager](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

Quando **[!UICONTROL Account Type]** está definida como `Google Tag Manager`, há campos adicionais exibidos.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | Exibição da loja | O identificador exclusivo do [!DNL Google Tag Manager] recipiente. Normalmente, esse valor começa com `GTM-`. Esta ID está em seu [!DNL Google Tag Manager] conta. Se [!DNL Google Tag Manager] já estiver instalado e configurado para a loja, a ID do contêiner aparecerá automaticamente neste campo. |
| [!UICONTROL List property for the catalog page] | Exibição da loja | Identifica o [!DNL Google Tag Manager] propriedade associada à página do catálogo. Valor padrão: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Exibição da loja | Identifica o [!DNL Google Tag Manager] propriedade associada ao bloco de venda cruzada. Valor padrão: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Exibição da loja | Identifica o [!DNL Google Tag Manager] propriedade associada ao bloco de venda adicional. Valor padrão: `Up-sell` |
| [!UICONTROL List property for the related products block] | Exibição da loja | Identifica o [!DNL Google Tag Manager] propriedade associada ao bloco produtos relacionados. Valor padrão: `Related Products` |
| [!UICONTROL List property for the search results page] | Exibição da loja | Identifica o [!DNL Google Tag Manager] propriedade associada à página de resultados da pesquisa. Valor padrão: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Exibição da loja | Identifica o [!DNL Google Tag Manager] propriedade associada aos rótulos para promoções internas. Valor padrão: `Label` |

{style="table-layout:auto"}

## [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Exibição da loja | Ativa o Google AdWords na loja. Opções: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Exibição da loja | A ID da sua conta do Google AdWords. |
| [!UICONTROL Conversion Language] | Exibição da loja | O idioma usado para conversões do AdWords. Opções: `All available languages` |
| [!UICONTROL Conversion Format] | Exibição da loja | Determina o formato do [!DNL Google Site Stats] que aparece na página de conversão. A notificação está vinculada a uma página que informa os visitantes sobre os cookies usados para rastrear suas visitas. Esse valor numérico é atribuído à variável `google_conversion_format` no seu script do AdWords. Para saber mais, consulte [Sobre o rastreamento de conversão](https://support.google.com/google-ads/answer/1722022?hl=en) no site da Google. Opções: <br/>**`1`**- Exibe uma notificação em uma linha.<br/>**`2`** - (Padrão) Exibe uma notificação em duas linhas. <br/>**`3`**- Não exibe nenhuma notificação ao cliente. |
| [!UICONTROL Conversion Color] | Exibição da loja | Determina a cor do rótulo de conversão. Use um [seletor de cores](https://www.w3schools.com/colors/colors_picker.asp) para escolher o valor hexadecimal. Esse valor hexadecimal é atribuído à variável `google_conversion_color` no seu script do AdWords. Por exemplo: ffffff  `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Exibição da loja | Um rótulo de texto que aparece com a variável [!DNL Google Site Stats] notificação. Essa cadeia de texto é atribuída à variável `~` no seu script do AdWords. Por exemplo: &quot;Obrigado por comprar!&quot; |
| [!UICONTROL Conversion Value Type] | Exibição da loja | Especifica o tipo de valor usado para determinar quando uma conversão ocorre. Opções: <br/>**`Dynamic`**- Determina que ocorreu uma conversão com base no valor dinâmico do pedido.<br/>**`Constant`** - Determina se uma conversão ocorreu com base no valor inserido. |
| [!UICONTROL Conversion Value] | Exibição da loja | Especifica o valor usado para um _[!UICONTROL Constant]_tipo de valor de conversão. |
| [!UICONTROL Send Order Currency] | Exibição da loja | Ativa os valores de conversão de moeda específicos da transação no AdWords (para sites com moedas base diferentes). |

{style="table-layout:auto"}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![GOOGLE ANALYTICS4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Exibição da loja | Habilita Google Analytics 4 para sua loja. Opções: `Yes` / `No` |
| [!UICONTROL Account Type] | Exibição da loja | ![Adobe Commerce](../../assets/adobe-logo.svg) (Somente no Adobe Commerce) Determina as opções de configuração de acordo com o tipo de conta do Google Analytics. Opções: `Google Analytics4` (padrão) / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | Exibição da loja | O número da conta, ou código de rastreamento, que foi atribuído quando você criou sua conta do Google Analytics. |
| [!UICONTROL Anonymize IP] | Exibição da loja | Determina se as informações de identificação são removidas dos endereços IP exibidos nos resultados de Google Analytics. |
| [!UICONTROL Enable Content Experiments] | Exibição da loja | Ativa [Experimentos de conteúdo do Google](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207), que pode ser usada para testar até dez versões diferentes da mesma página. Opções: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics4 - Tipo de conta do Google Tag Manager](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

Quando **[!UICONTROL Account Type]** está definida como `Google Tag Manager`, há campos adicionais exibidos.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | Exibição da loja | O identificador exclusivo do [!DNL Google Tag Manager] recipiente. Normalmente, esse valor começa com `GTM-`. Essa ID está na sua conta do Google Tab Manager. Se [!DNL Google Tag Manager] já estiver instalado e configurado para a loja, a ID do contêiner aparecerá automaticamente neste campo. |
| [!UICONTROL List property for the catalog page] | Exibição da loja | Identifica o [!DNL Google Tag Manager] propriedade associada à página do catálogo. Valor padrão: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Exibição da loja | Identifica o [!DNL Google Tag Manager] propriedade associada ao bloco de venda cruzada. Valor padrão: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Exibição da loja | Identifica o [!DNL Google Tag Manager] propriedade associada ao bloco de venda adicional. Valor padrão: `Up-sell` |
| [!UICONTROL List property for the related products block] | Exibição da loja | Identifica o [!DNL Google Tag Manager] propriedade associada ao bloco produtos relacionados. Valor padrão: `Related Products` |
| [!UICONTROL List property for the search results page] | Exibição da loja | Identifica o [!DNL Google Tag Manager] propriedade associada à página de resultados da pesquisa. Valor padrão: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Exibição da loja | Identifica o [!DNL Google Tag Manager] propriedade associada aos rótulos para promoções internas. Valor padrão: `Label` |

{style="table-layout:auto"}

### [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Exibição da loja | Ativa o Google AdWords na loja. Opções: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Exibição da loja | A ID da sua conta do Google AdWords. |
| [!UICONTROL Conversion Language] | Exibição da loja | O idioma usado para conversões do AdWords. Opções: todos os idiomas disponíveis |
| [!UICONTROL Conversion Format] | Exibição da loja | Determina o formato da notificação de Estatísticas do site do Google que aparece na página de conversão. A notificação está vinculada a uma página que informa os visitantes sobre os cookies usados para rastrear suas visitas. Esse valor numérico é atribuído à variável `google_conversion_format` no seu script do AdWords. Para saber mais, consulte [Sobre o rastreamento de conversão](https://support.google.com/google-ads/answer/1722022?hl=en) no site da Google. Opções: <br/>**`1`**- Exibe uma notificação em uma linha.<br/>**`2`** - (Padrão) Exibe uma notificação em duas linhas. <br/>**`3`**- Não exibe nenhuma notificação ao cliente. |
| [!UICONTROL Conversion Color] | Exibição da loja | Determina a cor do rótulo de conversão. Use um [seletor de cores](https://www.w3schools.com/colors/colors_picker.asp) para escolher o valor hexadecimal. Esse valor hexadecimal é atribuído à variável `google_conversion_color` no seu script do AdWords. Por exemplo: ffffff  `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Exibição da loja | Um rótulo de texto que aparece com a notificação de Estatísticas de site do Google. Essa cadeia de texto é atribuída à variável `~` no seu script do AdWords. Por exemplo: &quot;Obrigado por comprar!&quot; |
| [!UICONTROL Conversion Value Type] | Exibição da loja | Especifica o tipo de valor usado para determinar quando uma conversão ocorre. Opções: <br/>**`Dynamic`**- Determina que ocorreu uma conversão com base no valor dinâmico do pedido.<br/>**`Constant`** - Determina se uma conversão ocorreu com base no valor inserido. |
| [!UICONTROL Conversion Value] | Exibição da loja | Especifica o valor usado para um _[!UICONTROL Constant]_tipo de valor de conversão. |
| [!UICONTROL Send Order Currency] | Exibição da loja | Ativa os valores de conversão de moeda específicos da transação no AdWords (para sites com moedas base diferentes). |

{style="table-layout:auto"}
