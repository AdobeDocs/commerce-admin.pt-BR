---
title: Configurar pesquisa no catálogo
description: Saiba como configurar a pesquisa no catálogo para sua loja.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Configurar pesquisa no catálogo

Há duas variações da configuração da Pesquisa no catálogo. O primeiro método descreve as configurações disponíveis quando [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) O está instalado. O segundo método descreve as definições de configuração do Adobe Commerce nativo com [Elasticsearch][1]{:target=&quot;_blank&quot;}.

## Método 1: Adobe Commerce com [!DNL Live Search]

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** por baixo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Catalog Search]** seção.

   ![Pesquisa no catálogo do Live Search](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada dessas opções, consulte [Adobe Commerce com Live Search](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) no _Referência de configuração_.

1. Para limitar o comprimento e a contagem de palavras do texto de consulta de pesquisa, defina um valor para **[!UICONTROL Minimal Query Length]** e **[!UICONTROL Maximum Query Length]**.

1. Para limitar a quantidade de resultados de pesquisa populares a serem armazenados em cache para respostas mais rápidas, defina uma quantidade para **[!UICONTROL Number of top search results to cache]**.

   O valor padrão é `100`. Inserir um valor de `0` armazena em cache todos os termos e resultados da pesquisa quando inseridos uma segunda vez.

1. Para alterar o número máximo de linhas disponíveis para resultados retornados na variável [pop-over da loja](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html), insira um diferente **[!UICONTROL Autocomplete Limit]** valor.

   A restrição do número de linhas melhora o desempenho das pesquisas e reduz o tamanho da lista retornada. O valor padrão é `8` linhas.

## Método 2: comércio com o Elasticsearch

>[!IMPORTANT]
>
>Devido à [!DNL Elasticsearch 7] Anúncio do fim do suporte em agosto de 2023, recomenda-se que todos os clientes do Adobe Commerce migrem para o mecanismo de pesquisa OpenSearch 2.x. Para obter informações sobre como migrar o mecanismo de pesquisa durante a atualização do produto, consulte [Migração para o OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) no _Guia de atualização_.

### Etapa 1: configurar opções gerais de pesquisa

>[!NOTE]
>
>Com o Elasticsearch, não há suporte pronto para uso para pesquisa pelo sufixo. Por exemplo, a pesquisa por SKU pode não retornar o resultado esperado se a palavra-chave contiver somente a parte final do SKU.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** por baixo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Catalog Search]** seção.

   ![Configurações do Elasticsearch](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   Para obter mais informações sobre essas opções, consulte [Adobe Commerce com Elasticsearch](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) no _Referência de configuração_.

1. Para limitar o comprimento e a contagem de palavras do texto de consulta de pesquisa, defina um valor para **[!UICONTROL Minimal Query Length]** e **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >O valor definido para esse intervalo mínimo e máximo deve ser compatível com o intervalo correspondente definido na configuração do mecanismo de pesquisa Elasticsearch. Por exemplo, se você definir esses valores como `2` e `300` no Commerce, atualize os valores correspondentes no mecanismo de pesquisa.

1. Para limitar a quantidade de resultados de pesquisa populares a serem armazenados em cache para respostas mais rápidas, defina uma quantidade para **[!UICONTROL Number of top search results to cache]**.

   O valor padrão é `100`. Inserir um valor de `0` armazena em cache todos os termos e resultados da pesquisa quando inseridos uma segunda vez.

1. Se quiser ativar ou desativar o indexador de VEA do produto, defina o **[!UICONTROL Enable EAV Indexer]**.

   Esse recurso melhora a velocidade de indexação e restringe o uso do indexador por extensões de terceiros.

1. Para limitar o número máximo de resultados de pesquisa a serem exibidos para preenchimento automático de pesquisa, defina uma quantia para **[!UICONTROL Autocomplete Limit]**.

   A restrição dessa quantidade aumenta o desempenho das pesquisas e reduz o tamanho da lista exibida. O valor padrão é `8`.

### Etapa 2: configurar a conexão Elasticsearch

>[!IMPORTANT]
>
>A variável **[!UICONTROL Search Engine]**, **[!UICONTROL Elasticsearch Server Hostname]**, **[!UICONTROL Elasticsearch Server Port]**, **[!UICONTROL Elasticsearch Index Prefix]**, **[!UICONTROL Enable Elasticsearch HTTP Auth]**, e **[!UICONTROL Elasticsearch Server Timeout]** Os campos foram configurados quando o Commerce foi instalado ou atualizado. Esses valores devem ser alterados somente ao atualizar ou modificar o Elasticsearch.

1. Para **[!UICONTROL Search Engine]**, aceite o valor padrão `Elasticsearch 7`.

   O Elasticsearch 7.6.x é necessário para todas as instalações do Commerce.

1. Para **[!UICONTROL Elasticsearch Server Hostname]**, aceite o valor padrão que foi configurado quando o Commerce foi instalado.

   Neste exemplo, o valor padrão é `elasticsearch.internal`.

1. Para **[!UICONTROL Elasticsearch Server Port]**, aceite o valor padrão que foi configurado quando o Commerce foi instalado.

   Neste exemplo, o valor padrão é `9200`.

1. Para **[!UICONTROL Elasticsearch Index Prefix]**, insira um prefixo para identificar o índice de Elasticsearch.

   O valor padrão é `magento2`.

1. Para usar a autenticação HTTP para solicitar um nome de usuário e senha para acessar o Elasticsearch Server, defina **[!UICONTROL Enable Elasticsearch HTTP Auth]** para `Yes`.

1. Para **[!UICONTROL Elasticsearch Server Timeout]**, digite o número de segundos antes de o sistema atingir o tempo limite.

   O valor padrão é `15`.

1. Para verificar a configuração, clique em **[!UICONTROL Test Connection]**.

### Etapa 3: configurar sugestões e recomendações

>[!NOTE]
>
>As sugestões e recomendações de pesquisa podem afetar o desempenho do servidor.

1. Para oferecer recomendações, defina **[!UICONTROL Enable Search Recommendations]** para `Yes` e faça o seguinte:

   - Para **[!UICONTROL Search Recommendation Count]**, insira o número de recomendações a serem oferecidas.

   - Para mostrar o número de resultados encontrados para cada recomendação, defina **[!UICONTROL Show Results Count for Each Recommendation]** para `Yes`.

1. Definir **[!UICONTROL Enable Search Suggestions]** para `Yes` e faça o seguinte:

   - Para **[!UICONTROL Search Suggestions Count]**, digite o número de sugestões de pesquisa a serem oferecidas.

   - Para mostrar o número de resultados encontrados para cada sugestão, defina **[!UICONTROL Show Results for Each Suggestion]** para `Yes`.

### Etapa 4: configurar termos mínimos para corresponder a

Para controlar o número mínimo de termos da sua consulta que os resultados da pesquisa devem corresponder para o retorno, especifique um valor para **[!UICONTROL Minimum Terms to Match]**. Especificar esse valor garante a relevância ideal dos resultados para os compradores. Para obter uma lista de valores aceitos, consulte [parâmetro minimum_should_match](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) na documentação do Elasticsearch.

Quando terminar, clique em **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
