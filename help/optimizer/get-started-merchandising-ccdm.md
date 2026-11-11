---
title: Tarefas de merchandising do catálogo por função
description: Encontre orientações de tarefas para administradores, desenvolvedores e merchandisers que trabalham com instâncias do Adobe Commerce as a Cloud Service provisionadas com o CCDM.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="Somente SaaS" type="Positive" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplicável a instâncias do Adobe Commerce as a Cloud Service provisionadas apenas com CCDM (infraestrutura SaaS gerenciada pela Adobe)."
TQID: 'https://experienceleague.adobe.com/0PmobUkdEWspxuRSaIPL8vS1ojDDZ3gw-L-3SfPmJAg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: cc04bd17-78d5-5120-8c3d-1b8a57e49280
    internal-label: Integration
  - id: dec06508-d41f-555a-87e8-29e8bcdfa95a
    internal-label: Recommendations
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
  - id: f37757d8-3174-5335-b977-1161792f965d
    internal-label: Personalization
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: dba482e5-29a8-4127-afa2-c4b913512ef8
    internal-label: Data and analytics
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 742236e7fdb26c56a80f66a44b0a4960210f4dac
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%
---

# Tarefas de merchandising do catálogo por função

Use esta referência de tarefa para encontrar orientação para configurar dados de catálogo, integrar a loja, gerenciar merchandising e revisar o desempenho nas instâncias do Adobe Commerce as a Cloud Service provisionadas com o Composable Catalog Data Model (CCDM).

As responsabilidades variam de acordo com a implementação. As seções a seguir agrupam tarefas pelas funções que normalmente as executam.

- Os administradores gerenciam produtos, preços e configuração B2B no Commerce Foundation.
- Os desenvolvedores configuram a integração da loja e verificam as solicitações de catálogo e a coleta de dados comportamentais.
- Os merchandisers configuram a descoberta e as recomendações de produtos e usam relatórios para informar as decisões de merchandising.

Os dados de produtos e preços são sincronizados ao CCDM por meio da integração nativa do Adobe Commerce as a Cloud Service. Não é necessária nenhuma instalação de conector separado ou aplicativo App Builder.

## Preparar o catálogo e a loja

Conclua as tarefas que se aplicam à sua implementação. As exibições de catálogo B2C podem ser criadas manualmente. As exibições, as políticas e os catálogos de preços B2B são gerados a partir da configuração B2B no Commerce Foundation.

| Tarefa | Descrição | Recursos |
| --- | --- | --- |
| **Configurar produtos e preços** | Gerenciar produtos e preços no Commerce Foundation. Os dados de precificação são sincronizados com o CCDM como catálogos de preços; não crie preços de forma independente no CCDM. | [Lista de produtos](../catalog/products-list.md), [Criar um produto](../catalog/product-create.md), [Escopo de preço](../catalog/catalog-price-scope.md) e [Preços avançados](../catalog/pricing-advanced.md) |
| **Configurar exibições de repositório** | Configure as visualizações da loja e os dados localizados do produto necessários para sua loja no Commerce Foundation. | [Exibições de armazenamento](../stores-purchase/store-views.md) |
| **Configurar catálogos e empresas compartilhadas B2B** | Para implementações B2B, configure catálogos compartilhados e relacionamentos de empresa no Commerce Foundation antes de revisar a configuração de catálogo gerada. | [Catálogos compartilhados](../b2b/catalog-shared.md) e [Empresas](../b2b/account-companies.md) |
| **Configurar políticas e exibições do catálogo B2C** | Crie exibições de catálogo e selecione as políticas que definem a variedade de produtos disponíveis. Associe os catálogos de preços sincronizados aplicáveis a cada exibição. | [Exibições de catálogo](./setup/catalog-view.md) |
| **Revisar exibições do catálogo B2B** | Confirme se a sincronização nativa gerou as exibições de catálogo, as políticas e os catálogos de preços esperados. Gerencie a configuração B2B subjacente no Commerce Foundation em vez de criar estruturas duplicadas manualmente. | [Exibições de catálogo B2B](./setup/catalog-view.md#b2b-catalog-views) |
| **Configurar a vitrine eletrônica** | Configure a loja para solicitar o contexto do catálogo desejado. Para integrações personalizadas ou de outras lojas, analise os cabeçalhos de solicitação de catálogo aplicáveis. | [Configuração de vitrine](https://experienceleague.adobe.com/en/tools/commerce-storefront/setup/configuration/commerce-configuration/) |

Antes de configurar o merchandising, confirme se a loja retorna os produtos e preços esperados. Teste complementos ao carrinho, carrinho e check-out para verificar se os preços da transação correspondem à configuração pretendida do Commerce Foundation.

## Configurar merchandising e revisar o desempenho

| Tarefa | Descrição | Recursos |
| --- | --- | --- |
| **Configurar descoberta de produto** | Configurar regras de merchandising, aspectos e sinônimos. As regras podem se aplicar a todas as exibições de catálogo ou ser personalizadas para uma exibição específica. | [Visão geral do merchandising](./merchandising/overview.md) |
| **Revisar configurações de pesquisa** | Revise a configuração de pesquisa e as opções de pesquisa semântica disponíveis para sua implementação. | [Configurações de merchandising](./settings.md) e [Pesquisa semântica](./setup/semantic-search.md) |
| **Configurar recomendações** | Crie unidades de recomendação e verifique se a loja coleta os dados comportamentais necessários para a implementação. | [Visão geral das recomendações](./merchandising/recommendations/overview.md) |
| **Revisar desempenho** | Use as Métricas de sucesso e os relatórios de desempenho de pesquisa para avaliar a atividade da loja e informar as decisões de merchandising. | [Métricas de sucesso](./manage-results/success-metrics.md) e [Desempenho de pesquisa](./manage-results/search-performance.md) |

## Próximas etapas

Depois de configurar o merchandising e revisar o desempenho, continue monitorando e ajustando suas regras, aspectos e recomendações, conforme necessário, para otimizar a experiência da loja.
