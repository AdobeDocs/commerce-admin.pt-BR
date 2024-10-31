---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Google API]'
description: Revise as configurações na página [!UICONTROL Sales] &gt; [!UICONTROL Google API] do Administrador do Commerce.
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-analytics) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Exibição da loja | Habilita [!DNL Google Analytics] para o seu armazenamento. Opções: `Yes` / `No` |
| [!UICONTROL Account Type] | Exibição da loja | ![Adobe Commerce](../../assets/adobe-logo.svg) (somente Adobe Commerce) Determina as opções de configuração de acordo com o tipo de conta Google Analytics. Opções: Universal Analytics (padrão) / Google Tag Manager |
| [!UICONTROL Account Number] | Exibição da loja | O número da conta, ou código de rastreamento, que foi atribuído quando você criou sua conta do [!DNL Google Analytics]. |
| [!UICONTROL Anonymize IP] | Exibição da loja | Determina se as informações de identificação são removidas dos endereços IP que aparecem nos resultados de [!DNL Google Analytics]. |
| [!UICONTROL Enable Content Experiments] | Exibição da loja | Ativa os [Experimentos de Conteúdo do Google](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207), que podem ser usados para testar até dez versões diferentes da mesma página. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics - Tipo de conta do Google Tag Manager](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

Quando **[!UICONTROL Account Type]** está definido como `Google Tag Manager`, campos adicionais são exibidos.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | Exibição da loja | O identificador exclusivo do contêiner [!DNL Google Tag Manager]. Normalmente, este valor começa com `GTM-`. Esta ID está na sua conta do [!DNL Google Tag Manager]. Se [!DNL Google Tag Manager] já estiver instalado e configurado para o armazenamento, a ID do Contêiner aparecerá automaticamente neste campo. |
| [!UICONTROL List property for the catalog page] | Exibição da loja | Identifica a propriedade [!DNL Google Tag Manager] associada à página de catálogo. Valor padrão: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Exibição da loja | Identifica a propriedade [!DNL Google Tag Manager] associada ao bloco de venda cruzada. Valor padrão: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Exibição da loja | Identifica a propriedade [!DNL Google Tag Manager] associada ao bloco de venda adicional. Valor padrão: `Up-sell` |
| [!UICONTROL List property for the related products block] | Exibição da loja | Identifica a propriedade [!DNL Google Tag Manager] associada ao bloco de produtos relacionado. Valor padrão: `Related Products` |
| [!UICONTROL List property for the search results page] | Exibição da loja | Identifica a propriedade [!DNL Google Tag Manager] associada à página de resultados da pesquisa. Valor padrão: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Exibição da loja | Identifica a propriedade [!DNL Google Tag Manager] associada aos rótulos para promoções internas. Valor padrão: `Label` |

{style="table-layout:auto"}

## [!UICONTROL Google AdWords]

![AdWords do Google](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-adwords) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Exibição da loja | Ativa o Google AdWords na loja. Opções: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Exibição da loja | A ID da sua conta do Google AdWords. |
| [!UICONTROL Conversion Language] | Exibição da loja | O idioma usado para conversões do AdWords. Opções: `All available languages` |
| [!UICONTROL Conversion Format] | Exibição da loja | Determina o formato da notificação [!DNL Google Site Stats] que aparece na página de conversão. A notificação está vinculada a uma página que informa os visitantes sobre os cookies usados para rastrear suas visitas. Este valor numérico é atribuído à variável `google_conversion_format` no script do AdWords. Para saber mais, consulte [Sobre o rastreamento de conversão](https://support.google.com/google-ads/answer/1722022?hl=en) no site do Google. Opções: <br/>**`1`**- Exibe uma notificação de uma linha.<br/>**`2`** - (Padrão) Exibe uma notificação de duas linhas. <br/>**`3`**- Não exibe notificações de clientes. |
| [!UICONTROL Conversion Color] | Exibição da loja | Determina a cor do rótulo de conversão. Use um [seletor de cores](https://www.w3schools.com/colors/colors_picker.asp) para escolher o valor hexadecimal. Esse valor hexadecimal é atribuído à variável `google_conversion_color` no script do AdWords. Por exemplo: ffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Exibição da loja | Um rótulo de texto que aparece com a notificação [!DNL Google Site Stats]. Esta cadeia de texto é atribuída à variável `~` no script do AdWords. Por exemplo: &quot;Obrigado por comprar!&quot; |
| [!UICONTROL Conversion Value Type] | Exibição da loja | Especifica o tipo de valor usado para determinar quando uma conversão ocorre. Opções: <br/>**`Dynamic`**- Determina que ocorreu uma conversão com base no Valor dinâmico do Pedido.<br/>**`Constant`** - Determina que ocorreu uma conversão com base no valor inserido. |
| [!UICONTROL Conversion Value] | Exibição da loja | Especifica o valor usado para um tipo de valor de conversão _[!UICONTROL Constant]_. |
| [!UICONTROL Send Order Currency] | Exibição da loja | Ativa os valores de conversão de moeda específicos da transação no AdWords (para sites com moedas base diferentes). |

{style="table-layout:auto"}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![Google Analytics4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-analytics) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Exibição da loja | Habilita Google Analytics 4 para sua loja. Opções: `Yes` / `No` |
| [!UICONTROL Account Type] | Exibição da loja | ![Adobe Commerce](../../assets/adobe-logo.svg) (somente Adobe Commerce) Determina as opções de configuração de acordo com o tipo de conta Google Analytics. Opções: `Google Analytics4` (padrão) / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | Exibição da loja | O número da conta, ou código de rastreamento, que foi atribuído quando você criou sua conta do Google Analytics. |
| [!UICONTROL Anonymize IP] | Exibição da loja | Determina se as informações de identificação são removidas dos endereços IP exibidos nos resultados de Google Analytics. |
| [!UICONTROL Enable Content Experiments] | Exibição da loja | Ativa os [Experimentos de Conteúdo do Google](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207), que podem ser usados para testar até dez versões diferentes da mesma página. Opções: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics4 - Tipo de conta do Google Tag Manager](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

Quando **[!UICONTROL Account Type]** está definido como `Google Tag Manager`, campos adicionais são exibidos.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | Exibição da loja | O identificador exclusivo do contêiner [!DNL Google Tag Manager]. Normalmente, este valor começa com `GTM-`. Essa ID está na sua conta do Google Tab Manager. Se [!DNL Google Tag Manager] já estiver instalado e configurado para o armazenamento, a ID do Contêiner aparecerá automaticamente neste campo. |
| [!UICONTROL List property for the catalog page] | Exibição da loja | Identifica a propriedade [!DNL Google Tag Manager] associada à página de catálogo. Valor padrão: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Exibição da loja | Identifica a propriedade [!DNL Google Tag Manager] associada ao bloco de venda cruzada. Valor padrão: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Exibição da loja | Identifica a propriedade [!DNL Google Tag Manager] associada ao bloco de venda adicional. Valor padrão: `Up-sell` |
| [!UICONTROL List property for the related products block] | Exibição da loja | Identifica a propriedade [!DNL Google Tag Manager] associada ao bloco de produtos relacionado. Valor padrão: `Related Products` |
| [!UICONTROL List property for the search results page] | Exibição da loja | Identifica a propriedade [!DNL Google Tag Manager] associada à página de resultados da pesquisa. Valor padrão: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Exibição da loja | Identifica a propriedade [!DNL Google Tag Manager] associada aos rótulos para promoções internas. Valor padrão: `Label` |

{style="table-layout:auto"}

### [!UICONTROL Google AdWords]

![AdWords do Google](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-adwords) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Exibição da loja | Ativa o Google AdWords na loja. Opções: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Exibição da loja | A ID da sua conta do Google AdWords. |
| [!UICONTROL Conversion Language] | Exibição da loja | O idioma usado para conversões do AdWords. Opções: todos os idiomas disponíveis |
| [!UICONTROL Conversion Format] | Exibição da loja | Determina o formato da notificação de Estatísticas do site do Google que aparece na página de conversão. A notificação está vinculada a uma página que informa os visitantes sobre os cookies usados para rastrear suas visitas. Este valor numérico é atribuído à variável `google_conversion_format` no script do AdWords. Para saber mais, consulte [Sobre o rastreamento de conversão](https://support.google.com/google-ads/answer/1722022?hl=en) no site do Google. Opções: <br/>**`1`**- Exibe uma notificação de uma linha.<br/>**`2`** - (Padrão) Exibe uma notificação de duas linhas. <br/>**`3`**- Não exibe notificações de clientes. |
| [!UICONTROL Conversion Color] | Exibição da loja | Determina a cor do rótulo de conversão. Use um [seletor de cores](https://www.w3schools.com/colors/colors_picker.asp) para escolher o valor hexadecimal. Esse valor hexadecimal é atribuído à variável `google_conversion_color` no script do AdWords. Por exemplo: ffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Exibição da loja | Um rótulo de texto que aparece com a notificação de Estatísticas de site do Google. Esta cadeia de texto é atribuída à variável `~` no script do AdWords. Por exemplo: &quot;Obrigado por comprar!&quot; |
| [!UICONTROL Conversion Value Type] | Exibição da loja | Especifica o tipo de valor usado para determinar quando uma conversão ocorre. Opções: <br/>**`Dynamic`**- Determina que ocorreu uma conversão com base no Valor dinâmico do Pedido.<br/>**`Constant`** - Determina que ocorreu uma conversão com base no valor inserido. |
| [!UICONTROL Conversion Value] | Exibição da loja | Especifica o valor usado para um tipo de valor de conversão _[!UICONTROL Constant]_. |
| [!UICONTROL Send Order Currency] | Exibição da loja | Ativa os valores de conversão de moeda específicos da transação no AdWords (para sites com moedas base diferentes). |

{style="table-layout:auto"}
