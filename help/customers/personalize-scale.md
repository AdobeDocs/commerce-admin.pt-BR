---
title: Crie experiências atraentes e personalizadas em escala
description: Saiba quais recursos estão disponíveis no Adobe [!DNL Commerce] O permite criar uma experiência personalizada para seus compradores.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 1a63af10d76cb9d17a992e8822e99d50bcdfa84e
workflow-type: tm+mt
source-wordcount: '1630'
ht-degree: 0%

---

# Crie experiências atraentes e personalizadas em escala

Adobe [!DNL Commerce] O oferece um kit de ferramentas avançado para personalizar cada ponto de contato do cliente, aumentando o envolvimento, a conversão e a receita do comprador.

Neste artigo, você aprenderá:

- O que é personalização?
- Quais dados são necessários para realizar a personalização?
- Como o Adobe [!DNL Commerce] desbloquear personalização?
- Casos de uso de personalização disponíveis

## O que é personalização?

Personalização significa adaptar os aspectos da experiência de compra de cada cliente para atender às suas necessidades, contexto e preferências exclusivas. A personalização não está limitada ao conteúdo no site ou à recomendação de produtos de melhor ajuste, mas abrange todos os pontos de contato na jornada do cliente, incluindo:

- **Campanhas e comunicações** - Fornecer mensagens relevantes e consistentes por meio de campanhas e comunicações
- **Descoberta de produto** - Mostrando os produtos certos aos clientes certos nos momentos certos
- **Promoções e ofertas** - Direcionar promoções e ofertas para impulsionar cada cliente a converter
- **Experiências de conteúdo** - Personalização do conteúdo do site para que ele se sinta hiper-relevante para cada cliente e sua jornada

![Tipos de personalização](assets/types-personalization.png){width="700" zoomable="yes"}

Embora esses tipos de experiências personalizadas possam parecer viáveis para um pequeno subconjunto de clientes, personalizar em escala para milhares ou milhões de clientes em cada ponto de contato e canal, tudo em tempo real pode parecer impossível. Nas seções a seguir, você aprenderá como o Adobe [!DNL Commerce] e o Adobe Experience Cloud podem ajudar.

## Quais dados são necessários para realizar a personalização?

Uma personalização eficiente requer contexto ou sinais que fornecem informações sobre os clientes que podem ser usadas para modificar sua experiência. A tabela a seguir fornece os vários tipos de dados e a função que o Adobe [!DNL Commerce] ações de apoio à recolha e ativação desses dados.

| Tipos de dados | Dados da vitrine (Eventos comportamentais) | Dados de back office (eventos do lado do servidor) | Perfil do cliente e dados do segmento |
|---|---|---|---|
| **Definição** | Cliques ou ações que os clientes realizam no site. | Informações sobre o ciclo de vida e detalhes de cada pedido (passado e atual). | Quem são seus compradores e para quais segmentos eles se qualificam. |
| **Eventos capturados pelo Adobe Commerce** | [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signin)<br>[signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#removefromrequisitionlist) | **Status do pedido**:<br>[orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCanceled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**Histórico de pedidos**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/connect-data#send-historical-order-data):<br>- SKU, Nome, Quantidade de Preço, Desconto<br>- Categoria do produto<br>- Valor do Pagamento, Tipo, Moeda<br>- Método de envio e valor<br>- ID do reembolso, valor, moeda<br>- Motivo da devolução, Condição, Resolução<br>- Endereço<br>- Email | [**Registro de perfil**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord): (Nome, Gênero, Endereço, Status De Fidelidade, Número De Telefone, Endereço De Email)<br>**Status da conta**:<br>[accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountdeleted) |

Com todos esses ricos, originais [!DNL Commerce] dados, você estará pronto para direcionar e personalizar a experiência de cada comprador. Na próxima seção, você aprenderá como [!DNL Commerce] O e o Adobe Experience Cloud ajudam a criar experiências personalizadas e os casos de uso que você pode ativar.

## Como o Adobe [!DNL Commerce] capacitar a personalização?

Adobe [!DNL Commerce] O compartilhamento de dados permite coletar e compartilhar os tipos de dados na tabela anterior com outros produtos da Adobe Experience Cloud para potencializar perfis e públicos-alvo de clientes unificados, campanhas personalizadas e análises e insights avançados.

![Como os dados fluem para a borda do Experience Platform](assets/commerce-edge.png){width="700" zoomable="yes"}

Adobe [!DNL Commerce] O Compartilhamento de dados inclui dois componentes principais:

1. [Conexão de dados](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview): compartilhe dados de vitrine, back office e perfil do cliente do Adobe [!DNL Commerce] à rede de borda Adobe Experience Platform para uso em aplicativos Adobe Experience Cloud, incluindo:

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview): junte os dados do cliente de várias fontes (ERP, CRM, POS) em perfis unificados e crie segmentos baseados em regras ou AI.
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started): inicie jornadas personalizadas omnicanal, incluindo campanhas de email, SMS, notificações por push e muito mais.
   - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) e [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview): obtenha insights do cliente e da empresa.
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro): teste e otimize o conteúdo, produtos recomendados, ofertas, navegação e muito mais.

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation): Uso [!DNL Real-Time CDP] públicos-alvo para personalizar blocos de conteúdo dinâmico, promoções e regras de produto relacionadas no seu Adobe [!DNL Commerce] local.

### Personalização pronta para uso: introdução ao Adobe nativo [!DNL Commerce] recursos

Adobe [!DNL Commerce] O oferece personalização eficiente com seus recursos nativos e prontos para uso. A tabela a seguir descreve [!DNL Commerce] recursos que você pode ativar imediatamente para começar a personalizar a jornada.

| Categoria | Recursos |
|---|---|
| Descoberta personalizada de produtos | [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview): personalize e otimize os resultados da pesquisa com base nas ações comportamentais e afinidades de um comprador no site com a pesquisa habilitada por IA.<br>[Merchandising inteligente de categorias](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch): classificação de produtos orientada por IA em páginas de categoria com base nas ações comportamentais e afinidades de um comprador no site.<br>[Recommendations do produto](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview): recomendações de produtos alimentados por IA com base no comportamento, nas tendências e nas afinidades do comprador.<br>[Regras de produto relacionadas](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules): defina regras personalizadas para exibir produtos do seu catálogo para gerar vendas cruzadas e suplementares. |
| Conteúdo personalizado do site | [Blocos de conteúdo dinâmico](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks): exiba blocos de conteúdo personalizados, por exemplo, banners, com base nos segmentos de clientes no Adobe Commerce. |
| Ofertas e promoções personalizadas | [Regras de preço do carrinho](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart): aplique descontos a itens no carrinho de compras com base em um conjunto de condições, incluindo segmentos de clientes no Adobe [!DNL Commerce]. |
| Insights e medição | [Adobe [!DNL Commerce] Inteligência](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started): entenda como suas estratégias de personalização estão funcionando e melhoram com o tempo. |

## Principais casos de uso de personalização

Adobe [!DNL Commerce] Os clientes do estão usando recursos prontos para uso e compartilhando dados com a Adobe Experience Cloud para vários casos de uso. As seções a seguir destacam os principais casos de uso e descrevem como eles são implementados usando o Adobe [!DNL Commerce] Somente ou [!DNL Commerce] mais aplicativos Experience Cloud.

### Campanhas e comunicações personalizadas

| Caso de uso | Solução |
|---|---|
| **Carrinho e navegação abandonados** - Enviar um email personalizado de reengajamento ou uma notificação quando um cliente abandonar o carrinho ou a sessão de navegação após demonstrar alto engajamento | **Adobe [!DNL Commerce] Somente**:<br>[Lembretes de email](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe [!DNL Commerce] com o Adobe Journey Optimizer**:<br>[!DNL Commerce] os dados do servem como acionador para uma jornada de abandono omnicanal. Personalize essa jornada com base nos atributos do cliente, no que ele abandonou, em outros comportamentos de compra e em compras anteriores.<br>Commerce com Adobe Journey Optimizer e Real-Time CDP: adapte campanhas de abandono com base em perfis unificados do cliente e públicos gerenciados centralmente, por exemplo, criando um público com alta taxa de abandono. |
| **Criação de público-alvo centralizada** : crie públicos-alvo com base em regras ou alimentados por IA com base no comportamento no site, compras anteriores, atributos de perfil, afinidades de categoria, status de fidelidade, valor do cliente e muito mais | **Adobe [!DNL Commerce] Somente**:<br>Coletar informações de perfil do cliente quando [!DNL Commerce] os clientes criam contas. Criar baseado em regras [segmentos de clientes](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) e grupos de clientes para personalizar conteúdo e promoções.<br>**Adobe [!DNL Commerce] com o Adobe Real-Time CDP**:<br> [Perfis unificados](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) de várias fontes de dados e canais; públicos-alvo baseados em regras ou alimentados por IA. |
| **Oferta de email/SMS personalizada com base no comportamento do comprador** - Envie ofertas personalizadas aos clientes por email direcionado com base em compras anteriores e no comportamento do comprador, por exemplo, envie ofertas de produtos ou categorias que os clientes visualizaram ou com os quais participaram. | **Adobe [!DNL Commerce] Somente**:<br>Exportar dados para uso com soluções de automação de marketing.<br>**Adobe [!DNL Commerce] com Adobe Journey Optimizer e Real-Time CDP**:<br>[!DNL Commerce] Os dados do servem como acionador para ofertas de email ou SMS e fornecem sinais (comportamentos do comprador) para personalizar com base no. O Real-Time CDP não é necessário, mas geralmente essas ofertas e campanhas são criadas em torno de públicos-alvo, que seriam criados e gerenciados no Real-Time CDP. |
| **Produtos/Marcas compatíveis com várias ou outras vendas** - Se um cliente comprar um produto ou marca compatível ou indicar alta afinidade com outro produto ou marca, envie uma campanha (email/SMS) para impulsionar a conversão de venda cruzada. | **Adobe [!DNL Commerce] Somente**:<br>Usar Adobe [!DNL Commerce] [Recommendations do produto](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) para recomendar produtos específicos no site. Também é possível usar [Regras de produto relacionadas](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) para sugerir outros produtos.<br>**[!DNL Commerce] com [!DNL Target]**:<br>Adobe [!DNL Target] O também tem um mecanismo de recomendação de produto integrado com recursos avançados, como afinidade de categorias. Isso pode ser usado para venda cruzada ou adicional.<br>**[!DNL Commerce] com o Adobe Journey Optimizer**:<br>Uso [!DNL Target] ou [!DNL Commerce] para determinar os produtos a serem recomendados e, em seguida, entregues por meio do Adobe Journey Optimizer. |

### Experiências personalizadas do site

| Caso de uso | Solução |
|---|---|
| **Conteúdo personalizado do site** - Personalize banners de sites e outros conteúdos de página com base nas ações do comprador, como navegação de produtos e afinidades de categorias. Implante conteúdo de melhor ajuste com base nos resultados de testes A/B ou metas comerciais. | **Adobe [!DNL Commerce] Somente**:<br>Implantar específico de segmento [blocos de conteúdo dinâmico](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks).<br>**[!DNL Commerce] com o Real-Time CDP **:<br>Uso [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) para implantar blocos de conteúdo dinâmico específicos do público-alvo que respondam a ações em tempo real e dados unificados do perfil do cliente, enquanto gerenciam centralmente perfis e públicos-alvo no Real-Time CDP.<br>**[!DNL Commerce] com[!DNL Target]**:<br>Personalize cada parte da experiência do site, incluindo conteúdo, itens de navegação, layouts completos de página e muito mais, usando o Adobe [!DNL Commerce] dados no Adobe [!DNL Target]. Teste A/B do conteúdo, selecione e implante automaticamente o conteúdo vencedor para cada cliente.<br>**[!DNL Commerce] com o AEM Assets **:<br>Armazene todo o seu conteúdo no Adobe Experience Manager Assets. Acesse nativamente esse conteúdo no Adobe Commerce. Use a GenAI para criar variações de conteúdo para personalizar para segmentos ou públicos diferentes. |
| **Oferta personalizada no site com base no comportamento** - Personalize promoções com base em ações do comprador, como navegação de produtos e afinidades de categorias. Implante a próxima melhor oferta com base nos resultados de testes A/B ou metas de negócios. | **Adobe [!DNL Commerce] Somente**:<br>Implantar catálogo específico de segmento e [regras de preço do carrinho](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart).<br>**Adobe [!DNL Commerce] com o Real-Time CDP**:<br>Uso [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) para implantar ofertas específicas de público-alvo, enquanto gerencia centralmente perfis/públicos-alvo no Real-Time CDP.<br>**Commerce com[!DNL Target]**: use o offer decisioning para determinar qual oferta implantar, teste A/B ou defina metas de negócios para orientar as ofertas implantadas no Adobe Commerce. |

### Analytics e Insights

| Caso de uso | Solução |
|---|---|
| **Comportamento do cliente por canal** - Entenda as nuances de como os clientes se envolvem em cada canal (Web, presencial, de aplicativo ou outro) para afetar as estratégias de marketing de cada canal; entenda o funil do comprador e as fraquezas na experiência do cliente. | **Adobe [!DNL Commerce] Somente**:<br>[Adobe [!DNL Commerce] Inteligência](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) O fornece análises avançadas no ambiente digital [!DNL Commerce] canal, mas não entre canais ou partes mais amplas da jornada do cliente.<br>**Adobe [!DNL Commerce] com Customer Journey Analytics**:<br>[!DNL Commerce] feeds de dados painéis de dados para obter detalhes completos e avançados sobre todos os estágios da experiência do cliente (em vários canais). Entenda cada ponto de contato e o funil mais amplo para identificar pontos fracos na jornada do cliente em que os clientes podem cair. |
| **Tendências de compra** - Entenda os comportamentos de compra em um período específico (por exemplo, análise de cesta de compras, análise de produtos) para identificar tendências, sazonalidade e otimizar o marketing com base em padrões de compra históricos. | **Adobe [!DNL Commerce] Somente**:<br>[Adobe [!DNL Commerce] Inteligência](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) O fornece análises avançadas no ambiente digital [!DNL Commerce] canal, mas não entre canais ou partes mais amplas da jornada do cliente.<br>**Adobe [!DNL Commerce] com Customer Journey Analytics**:<br>[!DNL Commerce] feeds de dados painéis de dados para obter detalhes completos e avançados sobre todos os estágios da experiência do cliente (em vários canais). Entenda cada ponto de contato e o funil mais amplo para identificar pontos fracos na jornada do cliente em que os clientes podem cair. |

## Exemplo de caso de uso

Saiba como usar o Adobe Journey Optimizer para [enviar email de carrinho abandonado](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/using-ajo).
