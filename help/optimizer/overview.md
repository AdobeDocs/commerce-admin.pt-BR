---
title: Visão geral dos serviços de merchandising
description: Saiba mais sobre a configuração de catálogos, merchandising, relatórios e ferramentas de monitoramento para instâncias do Adobe Commerce as a Cloud Service provisionadas com o CCDM.
recommendations: noCatalog
badgeSaas: label="Somente SaaS" type="Positive" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplicável a instâncias do Adobe Commerce as a Cloud Service provisionadas apenas com CCDM (infraestrutura SaaS gerenciada pela Adobe)."
exl-id: f9516d4c-fbae-4db2-a1a9-cda3684a8122
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: a6a5a899ba60097bd6baf2a5de14063a0af2f313
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%
---
# Visão geral dos serviços de merchandising com o CCDM

As instâncias do Adobe Commerce as a Cloud Service provisionadas com o Modelo de Dados de Catálogo de Composição (CCDM) fornecem ferramentas de configuração de catálogo, merchandising, relatórios e monitoramento no [Administrador do Commerce na Experiência Unificada da Adobe](../getting-started/admin-unified-experience.md). O CCDM é a mesma base de catálogo que habilita o Adobe Commerce Optimizer.

Com os serviços de merchandising, você pode:

- Use dados de catálogo da sua instância do Adobe Commerce as a Cloud Service para oferecer suporte às experiências da loja.
- Configure visualizações e políticas de catálogo para definir sortimentos de produtos da loja.
- Aplique regras de merchandising em todas as exibições de catálogo ou adapte-as a uma exibição específica.
- Configurar recomendações de produto, aspectos de pesquisa e sinônimos.
- Revise o desempenho da loja por meio das Métricas de sucesso e dos relatórios de desempenho de pesquisa.
- Monitore a sincronização do catálogo e os eventos da loja capturados.

O Commerce Foundation continua a ser a fonte da verdade para produtos e preços e gerencia carrinhos, check-out e outras operações transacionais.

## Tour rápido

>[!BEGINTABS]

>[!TAB Configuração do catálogo]

Configure o contexto do catálogo disponível para uma vitrine.

- **Exibições de catálogo** — Combine origens de catálogo, políticas e catálogos de preços para definir os produtos e os preços que uma vitrine pode recuperar. Consulte [Exibições de catálogo](./setup/catalog-view.md).
- **Camadas do catálogo** — Substitua os atributos de produto selecionados sem alterar os dados de origem. Ao usar o AEM Assets para imagens de produtos, a camada AEM-Assets é aplicada por meio das Visualizações de produto. Consulte [Camadas do catálogo](./setup/catalog-layer.md).
- **Exibições de catálogo privado** — Habilite a Proteção de Catálogo para exigir um token assinado válido ao recuperar os dados de uma exibição de catálogo. Consulte [Exibições de catálogo privado](./setup/private-catalog-view.md).

>[!TAB Políticas]

As políticas filtram os produtos disponíveis por meio de uma visualização de catálogo com base nos atributos do produto. Por exemplo, uma política pode limitar um sortimento a uma marca ou categoria de produto específica.

As políticas determinam a variedade de produtos disponíveis. Eles não substituem a Proteção de catálogo, que controla o acesso a uma visualização de catálogo privado.

>[!TAB Merchandising]

Configure como os compradores descobrem produtos e como os produtos são promovidos dentro do sortimento disponível.

- **Oportunidades**—Revise o desempenho do produto, o comportamento do comprador e as tendências de pesquisa para identificar áreas para melhorias de merchandising.
- **Recommendations**—Crie e gerencie unidades de recomendação no Administrador do Commerce. As recomendações usam dados de catálogo e comportamento de comprador agregado para sugerir produtos relevantes, como &quot;Clientes que visualizaram este produto também visualizaram&quot;.
- **Regras de merchandising** — Controle como os produtos são promovidos e classificados. As regras podem se aplicar a todas as exibições de catálogo ou ser personalizadas para uma exibição específica. Consulte [Criar uma regra de comercialização](https://experienceleague.adobe.com/pt-br/docs/commerce/optimizer/merchandising/rules/add#create-a-rule).
- **Facetas**—Configure os filtros que os compradores usam para restringir os resultados do produto por atributos como marca, tamanho ou preço.
- **Sinônimos**—Associe termos de pesquisa equivalentes para ajudar os compradores a encontrar produtos usando palavras diferentes para o mesmo conceito.
- **Configurações**—Configure as opções de pesquisa e merchandising, incluindo aspectos de preço, idioma e pesquisa avançada.

As políticas determinam quais produtos estão disponíveis por meio de uma exibição de catálogo. As regras de merchandising controlam como os produtos dentro desse sortimento são promovidos e classificados.

Para obter detalhes sobre como os resultados da pesquisa são correspondidos e classificados, consulte [Correspondência e classificação de pesquisa](./manage-results/search-relevance-matching.md).

>[!TAB Relatórios]

Use relatórios para analisar a atividade da loja e informar as decisões de merchandising.

- **Métricas de sucesso** — examine a receita, a conversão, o envolvimento, a aquisição e a taxa de rejeição com base na atividade da loja.
- **Desempenho da pesquisa**—Revise os termos de pesquisa que os compradores usam e seu desempenho para identificar áreas para refinar a descoberta de produtos.

Os relatórios dependem dos dados de atividade da loja coletados pela implementação.

>[!TAB Configuração do sistema]

Monitore a sincronização do catálogo e a coleção de eventos da loja para investigar problemas de disponibilidade e implementação de dados.

- **Sincronização de catálogo** — Revise o status de sincronização para dados de catálogo transferidos do Commerce Foundation.
- **Eventos**—Revise os eventos capturados da loja usados pela descoberta de produtos, recomendações e relatórios. Use a página Eventos para ajudar a verificar a coleta de dados comportamentais e investigar eventos ausentes ou inesperados.

>[!ENDTABS]
<!--
Watch the following video for a high-level overview of [!DNL Adobe Commerce Optimizer]:

>[!VIDEO](https://video.tv.adobe.com/v/3450226)
-->

## Confirmar se uma instância usa o CCDM

1. Faça logon no Commerce Admin por meio do Unified Shell e selecione a instância desejada do Adobe Commerce as a Cloud Service.
1. Confirme se as páginas de merchandising do CCDM, como Exibições e políticas do catálogo, estão disponíveis na navegação da instância.
1. Se essas páginas não estiverem disponíveis, confirme se você selecionou a instância correta e se está usando o Unified Shell.

   Entre em contato com o Suporte da Adobe ou com a equipe de provisionamento da Commerce para verificar o status de provisionamento do CCDM da instância.

O status Pronto da instância confirma que está provisionada, mas não confirma por si só que usa o CCDM.

