---
title: Exibições do catálogo
description: Saiba o que são exibições de catálogo e como criá-las para organizar o catálogo de produtos por estrutura de negócios, políticas e preços.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="Somente SaaS" type="Positive" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplicável a instâncias do Adobe Commerce as a Cloud Service provisionadas apenas com CCDM (infraestrutura SaaS gerenciada pela Adobe)."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 8fbcfcdeb13c452a45e872d939e129703ac5abab
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%
---

# Exibições de catálogo

Uma exibição de catálogo define os produtos e os preços que uma vitrine eletrônica pode recuperar. Nas instâncias do Adobe Commerce as a Cloud Service provisionadas com o Modelo de dados de catálogo combinável (CCDM), as exibições de catálogo usam a mesma base de catálogo que capacita o Adobe Commerce Optimizer.

As visualizações de catálogo combinam origens de catálogo, políticas e catálogos de preços para definir o contexto de catálogo de uma loja. As políticas determinam a variedade de produtos disponíveis. As regras de merchandising controlam como os produtos dentro desse sortimento são promovidos e classificados, e podem ser aplicadas em todas as exibições de catálogo ou personalizadas para uma exibição específica. Consulte [Criar uma regra de comercialização](../merchandising/rules/add.md).

A Commerce Foundation continua sendo a fonte da verdade para os produtos e preços. Os dados de produto e preço sincronizam de uma maneira para o CCDM por meio da integração nativa do Adobe Commerce as a Cloud Service, sem instalação de conector separado ou aplicativo do App Builder. A configuração do site, da loja e da visualização da loja permanece no Commerce Foundation, que também gerencia carrinho, check-out, promoções, clientes, pedidos e pagamentos.

>[!NOTE]
>
>Para instâncias provisionadas com o CCDM, use o [Commerce Admin na Experiência unificada do Adobe](../../getting-started/admin-unified-experience.md) para configurar políticas e exibições de catálogo e associar catálogos de preços sincronizados a exibições de catálogo. As instâncias que usam o Serviço de Catálogo com o Live Search e as Recomendações de Produto não têm acesso a essas telas de gerenciamento de catálogo.

## Como as exibições de catálogo funcionam

Uma exibição de catálogo reúne dados de catálogo e configuração para um contexto de loja. Ele pode ser usado para representar uma unidade de negócios, marca, região ou outra experiência de loja.

- **[Fontes de catálogo](catalog-sources.md)** fornecem dados de produto para experiências de catálogo.
- **[Políticas](policies.md)** filtre dados de produto para uma exibição de catálogo.
- **[Os catálogos de preços](pricebooks.md)** fornecem dados de preços associados a uma exibição de catálogo.

As exibições de catálogo não substituem a estrutura de site, loja e visualização de loja no Adobe Commerce as a Cloud Service. O Commerce Foundation continua a gerenciar essa estrutura e operações transacionais.

Os dados do catálogo sincronizam unidirecionalmente do Commerce Foundation para o CCDM. O CCDM oferece suporte a experiências de catálogo da loja e à descoberta de produtos. O Commerce Foundation continua a lidar com carrinhos, check-out, promoções, clientes e pedidos.

## Antes de começar

Antes de configurar uma visualização de catálogo:

- [Confirme se a instância do Adobe Commerce as a Cloud Service usa o CCDM](../overview.md).
- Confirme se os dados de catálogo necessários para a loja foram preenchidos e [sincronizados](data-sync.md).
- Identifique a [origem do catálogo](catalog-sources.md), [políticas](policies.md) e [catálogos de preços](pricebooks.md) necessários para o contexto da loja.
- Determine se você precisa criar exibições de catálogo B2C manualmente ou revisar exibições de catálogo B2B geradas pela sincronização nativa.

>[!NOTE]
>
>Para implementações B2B, a sincronização nativa gera exibições de catálogo, políticas e catálogos de preços da configuração B2B no Commerce Foundation. Não crie manualmente duplicatas dessas estruturas geradas automaticamente.

## Criar uma visualização de catálogo para uma implementação B2C

Use esse workflow quando a implementação B2C exigir que as exibições de catálogo sejam configuradas manualmente.

1. Faça logon no [Administrador do Commerce na Experiência unificada](../../getting-started/admin-unified-experience.md) e selecione a instância do Adobe Commerce as a Cloud Service provisionada com o CCDM.
1. Na navegação à esquerda, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Views]**.
1. Selecione **[!UICONTROL Create catalog view]**.
1. Insira um nome para a exibição do catálogo.
1. Selecione a [origem ou origens do catálogo](catalog-sources.md) para o contexto da loja.
1. Associe as [políticas](policies.md) relevantes à exibição do catálogo.
1. Associe os catálogos de preços relevantes à exibição de catálogo [configurando a disponibilidade do catálogo de preços](pricebooks.md).
1. Crie a exibição do catálogo.

## Visualizações de catálogo B2B

Para implementações B2B, a sincronização nativa gera exibições de catálogo, políticas e catálogos de preços da configuração B2B no Commerce Foundation. Gerencie o catálogo B2B subjacente e os relacionamentos da empresa no Commerce Foundation em vez de criar manualmente estruturas duplicadas no CCDM.

Para obter instruções de configuração, consulte [Criar um catálogo compartilhado](../../b2b/catalog-shared-create.md) e [Atribuir empresas a um catálogo compartilhado](../../b2b/catalog-shared-assign-companies.md).

Após configurar as relações B2B:

1. Confirme se a [sincronização](data-sync.md) foi concluída.
2. Revise as exibições de catálogo geradas, [políticas](policies.md) e [catálogos de preços](pricebooks.md) em [Administrador do Commerce na Experiência Unificada](../../getting-started/admin-unified-experience.md).
3. Verifique se a loja exibe a variedade e os preços esperados do produto para a empresa.
4. Teste complementos ao carrinho, carrinho e check-out para confirmar se a disponibilidade do produto e os preços da transação correspondem à configuração B2B desejada.

## Catálogos de preços e check-out

Os catálogos de preços fornecem os dados de preço disponíveis por meio de uma exibição de catálogo. No Adobe Commerce as a Cloud Service, a Commerce Foundation continua sendo a fonte da verdade de preços, e os dados de preços são sincronizados com o CCDM por meio da integração nativa. Ao configurar uma visualização de catálogo, use os catálogos de preços sincronizados aplicáveis em vez de criar preços independentemente no CCDM.

O carrinho e o checkout usam os preços do Commerce Foundation. Verifique se os preços da loja exibidos correspondem aos preços aplicáveis do carrinho e do checkout.

## Revisar e validar uma exibição de catálogo

Depois de configurar uma visualização de catálogo, verifique a experiência completa da loja:

- Confirme se os dados de catálogo pretendidos estão [sincronizados](data-sync.md).
- Confirme se a exibição do catálogo está associada às [políticas](policies.md) e [catálogos de preços](pricebooks.md) pretendidos.
- Verifique se a loja retorna a variedade de produtos esperada.
- Verifique a precificação exibida em relação à precificação do Commerce Foundation correspondente.
- Teste complementos ao carrinho, carrinho e check-out.

Para implementações B2B, confirme também se as estruturas de catálogo geradas pela sincronização correspondem à configuração pretendida da empresa e do catálogo.

## Solução de problemas

### Faltam produtos na loja

- [Confirme se a instância usa CCDM](../overview.md).
- Confirme se os dados do catálogo estão [sincronizados](data-sync.md).
- Verifique se a loja está usando o contexto de catálogo desejado.
- Revise as [políticas](policies.md) associadas à exibição do catálogo.

### O preço exibido é inesperado

- Confirme se o [catálogo de preços](pricebooks.md) pretendido está associado à exibição do catálogo.
- Verifique se os dados de preço estão [sincronizados](data-sync.md) e consistentes com o Commerce Foundation.

  Consulte [Catálogos de preços](pricebooks.md) para obter os mapeamentos de preços de site e grupo de clientes.

- Valide o preço novamente no carrinho e na finalização da compra.

### As telas do catálogo do CCDM não estão visíveis no Administrador do Commerce

[Confirme se a instância selecionada usa o CCDM](../overview.md) e se você está acessando o [Administrador do Commerce na Experiência Unificada](../../getting-started/admin-unified-experience.md). Uma instância que executa serviços de catálogo v1 não tem as telas de administração do CCDM.

## Conteúdo relacionado

- [Introdução ao Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/pt-br/docs/commerce/cloud-service/getting-started)
- [Visão geral do catálogo compartilhado B2B do Adobe Commerce](../../b2b/catalog-shared.md)
- [Notas de versão do Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/pt-br/docs/commerce/cloud-service/release-notes)
- [Sincronização do catálogo](data-sync.md)
