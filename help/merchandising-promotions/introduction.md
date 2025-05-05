---
title: Introdução a merchandising e promoções do Commerce
description: Conheça as ferramentas do Commerce para criar promoções e oportunidades direcionadas ao engajamento de clientes.
exl-id: 8e55ac42-aeef-4f97-b1e8-9b2db354e5e6
source-git-commit: 7774aa82149faff55591303c7ff2fe2c84797a4a
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 1%

---

# Introdução a merchandising e promoções do Commerce

Direcione promoções e crie oportunidades para o envolvimento do cliente e transforme os compradores em compradores. Gerencie o relacionamento com o cliente apoiando atividades pós-compra e oferecendo descontos especiais aos clientes recorrentes. Conheça as práticas recomendadas e técnicas para apoiar suas iniciativas de SEO.

## Merchandising

_Merchandising_ é um termo usado no varejo para descrever a arte e a ciência do desenvolvimento de plantas baixas e a apresentação de produtos. Você pode pensar na [navegação baseada em categoria](../catalog/navigation-top.md) como a planta baixa da loja, e na apresentação dinâmica de produtos como as condições que você pode aplicar à listagem de produtos na loja. Além disso, você pode implementar programas que impulsionam mais vendas de produtos:

- [!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} [Visual Merchandiser](visual-merchandiser.md) - Um conjunto de ferramentas avançadas que permite posicionar produtos e aplicar condições que determinam quais produtos aparecem na lista de categorias.

- [Registros de presentes](gift-registries.md) - Dê aos seus clientes a capacidade de criar registros de presentes para ocasiões especiais e de convidar seus amigos e familiares para comprar seus presentes no registro de presentes.

- [Recompensas e fidelidade](rewards-loyalty.md) - Use um sistema de pontos para implementar programas exclusivos que impulsionem o engajamento do cliente e promovam a fidelidade do cliente. Você pode atribuir pontos por uma grande variedade de atividades de transações e clientes e controlar a alocação, o saldo e a expiração dos pontos.

- [Vendas e eventos privados](events-private-sales.md) - Use sua base de clientes existente para gerar burburinho e novos clientes potenciais ou para descarregar o estoque excedente por meio de vendas privadas e outros eventos de catálogo.

>[!TIP]
>
>Para saber mais sobre as Recomendações de Produtos e como elas podem fornecer a você o controle e a insight necessários para criar a melhor experiência para seus compradores, consulte o [Guia do Usuário das Recomendações de Produtos](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html?lang=pt-BR).

## Promoções

No Adobe Commerce, use os recursos de promoções para configurar relacionamentos de produtos e usar regras de preço para acionar descontos com base em várias condições. Você pode usar regras de preço para oferecer incentivos ao cliente, como:

- Envie aos melhores clientes um cupom para um desconto em um produto específico
- Oferecer frete grátis para compras acima de um determinado valor
- Programar uma promoção para um período específico

Uma regra é um conjunto de condições (uma ou mais) que aplicam alterações nos preços dos produtos quando um ou todos são atendidos. Cada regra pode ter várias condições, que se aplicam quando todas ou qualquer declaração (uma ou mais, mas não todas) é verdadeira ou falsa.

### Condições

As condições são declarações que refinam a lista de produtos e situações para aplicar a regra. Os atributos e as opções das condições diferem entre os tipos de regras disponíveis. Quando atendida, a ação é concluída, como descontos, buy-one-get-one (BOGO) e outras opções. As regras podem ser tão simples ou complicadas quanto necessário para atender às suas necessidades comerciais, descontos e promoções sazonais e oportunidades de um ano. Por exemplo, talvez você queira adicionar mais algumas opções de feriados e, ao mesmo tempo, fornecer frete gratuito o ano todo quando os carrinhos tiverem um subtotal alto.

>[!NOTE]
>
>Se você deseja definir uma condição baseada em um atributo de produto específico, **[!UICONTROL Use for Promo Rule Conditions]** deve ser definido como `Yes` para o atributo em suas [Propriedades da vitrine](../catalog/attribute-product-create.md).


### Regras de preço

Para [regras de preço de catálogo](price-rules-catalog.md), você cria condições com base em [conjuntos de atributos](../catalog/attribute-sets.md) no catálogo, funções de comparação e atributos selecionados. Você cria as condições como frases selecionando algumas instruções. Por exemplo, você pode criar duas regras de preço para aplicar descontos para roupas infantis e roupas masculinas/femininas com base na categoria.

![Diagrama - exemplo de regras de preço de catálogo](./assets/diagram-catalog-price-rules.png){width="500"}

As condições da [Regra de preço do carrinho](price-rules-cart.md) podem ser baseadas em qualquer categoria que seja filha do armazenamento [raiz](../catalog/category-root.md). As regras de preços são estabelecidas com antecedência e entram em ação sempre que as condições exigidas são cumpridas. Essas regras usam atributos, incluindo combinações de atributos de produto, como a correspondência de um SKU no carrinho usando atributos de produto. Essas regras também podem usar condições de quantidade para a seleção de produtos, combinações de condições para regras complicadas e atributos do carrinho, como subtotal.

![Diagrama - exemplo de regras de preço do carrinho](./assets/diagram-cart-price-rules.png){width="500"}

## Comunicações e SEO

Dominar a [Otimização do mecanismo de pesquisa (SEO)](seo-overview.md) é fundamental para atrair possíveis compradores. Saiba mais sobre a otimização de mecanismos de pesquisa e o ajuste do conteúdo e da apresentação do site para melhorar a forma como as páginas são indexadas por mecanismos de pesquisa.

Uma das tarefas a serem concluídas antes de iniciar sua loja é revisar os modelos de email usados para todas as comunicações enviadas pela loja para garantir que eles reflitam a sua marca. Mas você deve dar um passo além, desenvolvendo outras comunicações que promovam sua marca e produtos para os clientes existentes. É possível personalizar o conteúdo com variáveis e tags de marcação.

>[!NOTE]
>
>As versões 2.4.0 a 2.4.3 do Adobe Commerce e do Magento Open Source incluíam a extensão desenvolvida pelo fornecedor dotdigital usada para integrar com a nuvem do Engajamento dotdigital. A partir da versão 2.4.4, essa extensão não é mais fornecida com a versão principal e deve ser instalada e atualizada do Commerce Marketplace. O Marketplace também fornece acesso à documentação atual fornecida pelo desenvolvedor da extensão.
><br><br>
>Se você tiver a extensão agrupada ativada e configurada, deverá atualizar o arquivo composer.json como parte do processo de atualização 2.4.4 e gerenciar as atualizações de extensão a partir de agora. Consulte [Atualizar módulos](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=pt-BR) no _Guia de Atualização_ para obter mais informações.

- [Boletins informativos](newsletters.md) - Produza boletins informativos, gerencie sua lista de assinantes, desenvolva conteúdo e direcione o tráfego para sua loja.

- [RSS Feeds](social-rss.md#rss-feeds) - Use RSS feeds para publicar informações de seu produto em sites de agregação de compras e até mesmo incluí-los em seus informativos. Os clientes podem assinar seus RSS feeds para saber mais sobre novos produtos e promoções.

- [Redes sociais](social-rss.md#social-networks) - Integre seu armazenamento às suas redes sociais instalando uma extensão do Marketplace ou adicionando um plug-in às suas páginas de conteúdo.

## Ferramentas de marketing do Google

A configuração da sua loja está integrada às seguintes ferramentas do Google para ajudar a otimizar o seu conteúdo, analisar o seu tráfego e conectar o seu catálogo a agregadores de compras e marketplaces.

>[!NOTE]
>
>A partir da versão 2.4.5, a integração de serviços da Google é atualizada para oferecer suporte ao uso das APIs GTag. O GTag é um mecanismo unificado para integração com a funcionalidade do Google para páginas da Web e oferece suporte aos mais novos recursos e oportunidades para rastreamento e gerenciamento de conteúdo por meio dos Serviços da Google. Para obter mais informações, consulte a [documentação para desenvolvedores do Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

- [Google Analytics](google-analytics.md) - Use o Google Universal Analytics para definir dimensões e métricas personalizadas adicionais para rastreamento, com suporte para interações offline e de aplicativos móveis e acesso a atualizações contínuas.

- [Experimentos de conteúdo do Google](google-content-experiments.md) - Configure um teste A/B de produtos, categorias ou páginas de conteúdo usando o Conteúdo do Google Analytics

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Use o Google Tag Manager para gerenciar as várias tags relacionadas aos eventos de campanha de marketing.

- [Google AdWords](google-adwords.md) - Crie uma campanha do Google AdWords e rastreie as conversões da sua loja.
