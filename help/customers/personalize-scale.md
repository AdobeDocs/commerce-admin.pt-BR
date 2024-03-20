---
title: Personalização em escala
description: Saiba quais recursos do Adobe Commerce permitem criar uma experiência personalizada para seus compradores.
feature: Customers, Storefront, Personalization
source-git-commit: a4eeda918adcb74ad5e7008b80eff703fa15e878
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---

# Personalização em escala

&#x200B;A personalização em escala permite que as empresas personalizem a experiência de compra para cada ponto de contato do cliente com base no contexto imediato e no comportamento observado anteriormente. O objetivo é apresentar sempre a experiência mais relevante e personalizada possível.

Para entender os benefícios de oferecer uma experiência de compra personalizada, baixe o [_Introdução à personalização em escala_](https://business.adobe.com/resources/reports/getting-started-with-personalization-at-scale.html) relatório.

Criar uma experiência de compra personalizada requer que você saiba mais sobre o tipo de dados necessários para entender o contexto do cliente. A partir daí, você aprenderá sobre os recursos do Adobe Commerce que usam esses dados para desbloquear os insights do cliente necessários para criar a experiência de compras personalizada.

A imagem a seguir ilustra os conceitos envolvidos na personalização da experiência de compra:

![Criação de um pipeline de personalização](assets/personalization-journey.png){width="700" zoomable="yes"}

Este artigo discute cada um dos conceitos acima com mais detalhes.

## Como personalizar a experiência de compras

A personalização bem-sucedida começa com o contexto do cliente. Nesta seção, você aprenderá sobre os tipos de dados disponíveis para ajudar a criar o contexto do cliente.

### Dados da vitrine

Os dados da loja, também chamados de dados comportamentais ou do navegador, podem revelar insights sobre como os compradores interagem com o site. Por exemplo:

- Em quais produtos e categorias meus compradores estão mais interessados?
- Em que tipo de consultantes de pesquisa meus compradores estão mais envolvidos?
- Meus compradores estão adicionando produtos ao carrinho e depois abandonando-os?
- Meus compradores estão usando um navegador móvel ou desktop?

Os eventos da loja a seguir capturam dados que podem ajudar você a responder a essas perguntas:

- [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)

### Dados do back office

Os dados de back office, também chamados de dados do lado do servidor, podem revelar insights sobre o ciclo de vida do pedido. Por exemplo:

- Existem produtos comprados com mais frequência com base na estação do ano?
- Meus compradores estão devolvendo produtos?
- Como posso calcular o valor vitalício do cliente?

Os seguintes eventos de back office capturam dados que podem ajudá-lo a responder a essas perguntas:

- [orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderCanceled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

### Dados de perfil e segmento do cliente

Os dados de perfil do cliente podem revelar insights sobre quem são seus compradores e quais segmentos eles se qualificam. Por exemplo:

- Nome
- Sexo
- Endereço
- Status de fidelidade
- Número de telefone
- Endereço de email
- Status de fidelidade
- Número de telefone
- Endereço de email
- Qualificação para atualizações
- Compradores em vários canais
- Perspectivas de novos produtos
- Membros de fidelidade Ouro, prata ou bronze

Os eventos de perfil a seguir capturam dados que podem ajudar você a responder a essas perguntas:

- [Registro de perfil](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord)
- [accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

Os dados de vitrine, back office e perfil formam a base do cliente do Commerce e do contexto do pedido, o que ajuda você a saber quais produtos seus clientes estão visualizando e comprando. Você pode então direcionar os interesses deles e personalizar a experiência deles. Na próxima seção, você aprenderá quais tipos de experiências personalizadas você pode participar com seus compradores.

## Tipos de experiências personalizadas

Os dados de contexto do cliente e do pedido no Commerce alimentam os seguintes tipos de experiências personalizadas:

| Experiência | Descrição |
|---|---|
| **Descoberta de produto** | Contém serviços de comercialização que são [implantado como SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas). Esses são recursos que permitem usar dados comportamentais, atributos de produto e níveis de inventário para personalizar automaticamente a descoberta de produtos em resultados de pesquisa, recomendações de produtos e páginas de navegação. Todos esses recursos usam [ADOBE SENSEI AI](https://business.adobe.com/products/sensei/adobe-sensei.html). |
| **Conteúdo do site** | Refere-se à capacidade de implantar blocos de conteúdo dinâmico personalizados com base na navegação do cliente atual em seu site. |
| **Ofertas e campanhas** | Permite implantar conteúdo promocional personalizado com base nos dados do segmento. |
| **Medição** | Usa a inteligência de dados para entender melhor sua empresa, incluindo receita, desempenho de canal e mercadoria, promoções e assim por diante. |

Nas próximas duas seções, você aprenderá como usar esses dados para criar experiências personalizadas em [Adobe Experience Platform](#using-commerce-data-in-adobe-experience-platform) e no [recursos nativos do Commerce](#using-commerce-data-in-native-commerce-features).

## Uso de dados do Commerce no Adobe Experience Platform

Para criar uma experiência personalizada para seus compradores em todos os canais, envie os dados do Commerce para a Rede de borda do Experience Platform usando o [[!DNL Data Connection]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) extensão.

![Como os dados fluem para a borda do Experience Platform](assets/commerce-edge.png){width="700" zoomable="yes"}

Na imagem acima, os dados da loja, do back office e do perfil do cliente são enviados para a borda do Experience Platform usando um SDK, uma API e um conector de origem. Não é necessário entender totalmente como essas partes funcionam, pois a extensão lida com a complexidade do compartilhamento de dados para você. Quando os dados do evento estiverem na borda, você poderá puxá-los para outros aplicativos Experience Platform.

A tabela a seguir destaca alguns dos aplicativos Experience Platform disponíveis e como esses aplicativos usam seus dados do Commerce.

| Experiência | Aplicativo | Como os dados do Commerce são usados |
|---|---|---|
| **Conteúdo do site** | [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview) | Os dados do Adobe Commerce alimentam perfis unificados do cliente, com a Real-Time CDP unindo dados de várias fontes (ERP, CRM, CMS, POS) em perfis únicos. O Real-Time CDP também pode criar segmentos baseados em regras e AI para usar em seu conjunto de soluções de marketing. Você também pode usar os públicos do Real-Time CDP para personalizar blocos de conteúdo, promoções e regras de produtos relacionados. Consulte [[!DNL Audience Activation]](../customers/audience-activation.md) para saber mais.&#x200B; |
|  | [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro) | Os dados do Adobe Commerce podem ser ativados no Adobe [!DNL Target] para testar, otimizar e criar páginas de aterrissagem dinâmicas. Você pode personalizar a ordem em que o conteúdo é exibido em uma página, como descrições, especificações, revisões e produtos recomendados com base nos dados do Commerce enviados. |
| **Ofertas e campanhas** | [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) | Os dados comportamentais e de back office do Adobe Commerce podem servir como um acionador de jornadas personalizadas omnicanais, incluindo campanhas de email, SMS, notificações por push e muito mais.&#x200B; |
| **Medição** | [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview) e [Cliente [!DNL Journey Analytics]](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) | O Commerce envia os dados da loja e do back-office para o Cliente [!DNL Journey Analytics] (e somente dados da loja para o Adobe [!DNL Analytics]) para permitir uma análise mais avançada além das métricas básicas no Adobe Commerce Intelligence, como receita, mercadoria e promoções.&#x200B; |

Para saber mais sobre como enviar seus dados do Commerce para o Experience Platform, consulte [Conexão de dados](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview).

## Uso de dados do Commerce em recursos nativos do Commerce

Na seção a seguir, saiba como usar recursos nativos do Commerce, como o Product Recommendations e o Live Search, para criar uma experiência personalizada de compras. Você também aprenderá sobre um recurso chamado [!DNL Audience Activation], que usa dados de um produto disponível no Experience Platform chamado Real-Time CDP, conforme mencionado [anteriormente](#using-commerce-data-in-adobe-experience-platform). Embora o Real-Time CDP não seja nativo do Commerce, suas informações podem ser assimiladas no Commerce por meio do [[!DNL Audience Activation]](../customers/audience-activation.md) extensão.

A tabela a seguir destaca os recursos do Commerce disponíveis para transformar os dados de contexto de cliente e pedido do Commerce em insights acionáveis.

| Experiência | Recurso | Descrição |
|---|---|---|
| **Descoberta de produto** | [Live Search](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview) | Usa algoritmos de classificação de IA para personalizar e otimizar os resultados da pesquisa com base nas ações comportamentais no site de um comprador, aumentando a relevância e a conversão da pesquisa. |
|  | [Recommendations do produto](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) | Exibe recomendações de produtos alimentados por IA com base no comportamento do comprador, tendências, similaridade de produtos e muito mais. Quando combinadas com seu catálogo do Adobe Commerce, as recomendações de produto fornecem uma experiência altamente envolvente, relevante e personalizada. |
|  | [Merchandising de categoria](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch) | Acessado pelo Administrador do Live Search, o merchandising de categoria usa a IA para reclassificar automaticamente a sequência de produtos em cada página de categoria, a fim de aumentar a relevância e a conversão para cada comprador. Você pode criar e gerenciar regras alimentadas por IA para reclassificar automaticamente o sequenciamento de produtos em páginas de categoria de acordo com as ações e afinidades do comprador. |
| **Conteúdo do site** | [Blocos dinâmicos informados por recursos nativos do Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Permite fornecer conteúdo personalizado do site com base na lógica configurada nas regras de preço e nos segmentos do cliente. |
|  | [Blocos dinâmicos informados por públicos da Real-Time CDP](../customers/audience-activation.md) | Permite que os comerciantes forneçam conteúdo personalizado do site com base em públicos configurados no Real-Time CDP. |
| **Ofertas e campanhas** | [Regras de preço do carrinho](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) | Permite aplicar descontos a itens no carrinho de compras com base em um conjunto de condições. |
|  | [Blocos dinâmicos informados por recursos nativos do Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Permite exibir promoções de banner personalizadas com base em segmentos de clientes configurados nativamente no Commerce. |
|  | [Blocos dinâmicos informados por públicos da Real-Time CDP](../customers/audience-activation.md) | Permite exibir promoções personalizadas com base em públicos configurados no Real-Time CDP. |
| **Medição** | [Adobe Commerce Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) | (Anteriormente conhecido como Magento Business Intelligence) é uma plataforma de nuvem que fornece insights de práticas recomendadas para ajudar você a tomar decisões orientadas por dados e tomar ações claras e informadas. O Adobe Commerce Intelligence pode analisar seus dados para ajudá-lo a responder perguntas sobre o crescimento de pedidos, o comportamento do cliente e a eficácia das estratégias promocionais. |
