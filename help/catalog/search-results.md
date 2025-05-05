---
title: Resultados da pesquisa
description: Saiba como configurar como seus produtos correspondem aos critérios de pesquisa inseridos na caixa Pesquisa rápida ou no formulário Pesquisa avançada.
exl-id: c721fb3b-ee31-4d2b-b4ea-9ae2c80aa800
feature: Catalog Management, Search
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# Resultados da pesquisa

>[!NOTE]
>
>Esta página descreve a funcionalidade de pesquisa padrão que pode ser diferente do [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html).

A lista _Resultados da Pesquisa_ inclui todos os produtos que correspondem aos critérios de pesquisa inseridos na caixa Pesquisa Rápida ou no formulário Pesquisa Avançada. Cada lista de produtos no catálogo tem essencialmente os mesmos controles. A única diferença é que um é o resultado de uma consulta de pesquisa, e a outra diferença é o resultado da [navegação](navigation.md).

Os resultados podem ser formatados como uma grade ou lista e classificados por uma seleção de atributos. Os controles de paginação serão exibidos se houver mais produtos do que cabem na página. Use esses controles para mover de uma página para a próxima. O número de registros por página é determinado pela configuração de front-end do catálogo. Para obter mais informações, consulte [Listagens de Produtos](navigation-product-listings.md).

Com **Elasticsearch**:

- Não há suporte pronto para uso para pesquisa pelo sufixo. Por exemplo, a pesquisa por SKU pode não retornar o resultado esperado se a palavra-chave contiver somente a parte final do SKU.
- Há suporte pronto para uso para pesquisa por prefixo (pesquisa parcial por palavra-chave) somente para atributos de produto `name` e `sku`. Todos os outros atributos de produto são pesquisados por toda a palavra-chave, com a correspondência exata.
- Os resultados da pesquisa de atributos de produto `name` e `sku` são baseados na relevância, não na correspondência exata. As correspondências mais relevantes, como um _Nome do Produto_ ou _SKU_ com correspondência exata, são listadas primeiro. Para procurar uma correspondência exata, o cliente pode usar aspas duplas na consulta de pesquisa. Por exemplo, uma consulta de pesquisa `WSH12-32-Red` pode retornar vários produtos, classificados por relevância. Mas uma consulta de pesquisa `"WSH12-32-Red"` retorna somente um produto com **_exatamente_** correspondidos `sku`.

![Pesquisar resultados com controles de paginação](./assets/storefront-search-results-shorts.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>Devido ao anúncio do fim do suporte do Elasticsearch 7 para agosto de 2023, é recomendável que todos os clientes do Adobe Commerce migrem para o mecanismo de pesquisa OpenSearch 2.x. Para obter informações sobre como migrar o mecanismo de pesquisa durante a atualização do produto, consulte [Migrando para o OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) no _Guia de Atualização_.

## Mapeamento de palavras-chave para estender os resultados da pesquisa

Essa técnica usa um atributo para criar uma associação baseada em palavras-chave entre dois produtos, de modo que uma pesquisa por um dos produtos retorne resultados para os dois. Você pode usar o mapeamento de palavra-chave para promover um produto nos resultados da pesquisa onde, de outra forma, ele não seria exibido.

![Resultados de pesquisa com mapeamento de palavra-chave](./assets/storefront-search-results-extended.png){width="700" zoomable="yes"}

O exemplo a seguir usa o mapeamento de palavra-chave com base no SKU. Quando um dos SKUs é inserido na caixa de pesquisa, ambos os produtos aparecem nos resultados. Os SKUs dos seguintes produtos configuráveis são mapeados, em vez dos SKUs de variações de produtos:

- Jaqueta corta-vento Montana (MJ03)
- Chaz Kangaroo Hoodie (MH01)

### Etapa 1: Criar um atributo

1. Na lista _[!UICONTROL Products]_, abra o `Montana Wind Jacket` (MJ03) no modo de edição.
1. No canto superior direito, clique em **[!UICONTROL Add Attribute]**.
1. Na página _Selecionar atributo_, clique em **[!UICONTROL Create New Attribute]**.
1. Complete as propriedades do atributo da seguinte maneira:

   **[!UICONTROL Attribute Properties]**

   - [!UICONTROL Attribute Label] - `Search Keywords`
   - [!UICONTROL Catalog Input Type for Store Owner] - `Text Field`

   **[!UICONTROL Advanced Attribute Properties]**

   - [!UICONTROL Add to Column Options] - `Yes` (padrão)
   - [!UICONTROL Use in Filter Options] - `Yes` (padrão)

   **[!UICONTROL Storefront Properties]**

   - [!UICONTROL Use in Search] - `Yes`
   - [!UICONTROL Visible on Catalog Pages in the Storefront] - `No`
   - [!UICONTROL Used in Product Listings] - `No`

1. Quando terminar, clique em **[!UICONTROL Save Attribute]**.

   O atributo é adicionado ao conjunto de atributos do produto.

### Etapa 2: Mapear o primeiro produto

1. Na página de configurações do produto, role para baixo e expanda a seção _[!UICONTROL Attributes]_.
1. No campo **[!UICONTROL Search Keywords]**, insira a SKU `MH01` que deve ser mapeada para este produto.

   Você pode inserir vários SKUs separados por um espaço no campo Pesquisar palavras-chave. Neste exemplo, apenas um é inserido.

   ![Seção de atributos com palavra-chave de pesquisa](./assets/search-keywords-attribute.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.
1. Vá para **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;e atualize o **[!UICONTROL Page Cache]**.

### Etapa 3: Mapear o segundo produto

1. Na lista _[!UICONTROL Products]_, abra o `Chaz Kangaroo Hoodie` (MH01) no modo de edição.
1. Role para baixo e expanda a seção **[!UICONTROL Attributes]**.
1. No campo **[!UICONTROL Search Keywords]**, insira o SKU do outro produto, `MJ03`.
1. Clique em **[!UICONTROL Save]**.
1. Vá para **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;e atualize o **[!UICONTROL Page Cache]**.

### Etapa 4: teste-o na loja

1. Vá para a loja e digite `MJ03` na caixa _Pesquisa rápida_.
1. Verifique se ambos os produtos são retornados na lista de resultados da pesquisa.

## Pesquisa ponderada

Os atributos de produto ativados para pesquisa no catálogo podem receber um peso para atribuir a eles um valor mais alto nos resultados da pesquisa. Os atributos com um peso maior são retornados antes dos atributos com um peso menor. Por exemplo, se houver dois atributos no sistema, _cor_ com um peso de pesquisa de 3 e _descrição_ com um peso de pesquisa de 1. Uma pesquisa pela palavra _vermelho_ retorna uma lista de produtos com um valor de atributo de cor de `red` na parte superior dos resultados da pesquisa e retorna produtos com descrições que contêm a palavra _vermelho_ na parte inferior dos resultados da pesquisa. Neste exemplo, o atributo `color` tem um peso definido maior que o atributo `description`.

>[!IMPORTANT]
>
>A classificação por relevância é afetada por **_vários_** critérios e relações entre eles **_ao mesmo tempo_**. [!UICONTROL Search Weight] é apenas um desses critérios. Isso significa que, às vezes, os atributos com menor peso de pesquisa ainda podem ter mais relevância do que os atributos com maior peso de pesquisa. Outros critérios podem incluir o número de correspondências em um determinado atributo, a posição do termo de pesquisa encontrado e a estrutura geral do texto antes e depois de um termo de pesquisa.

**_Para definir as propriedades de peso de pesquisa de um atributo:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Localize o atributo na lista e abra-o no modo de edição.

1. No painel esquerdo, escolha **[!UICONTROL Storefront Properties]** e faça o seguinte:

   - Para incluir o atributo em consultas de pesquisa, defina **[!UICONTROL Use in Search]** como `Yes`.

   - Para estabelecer o valor de pesquisa do atributo, defina **[!UICONTROL Search Weight]** como um número de 1 a 10, onde `10` tem a prioridade mais alta. Se nenhum valor for inserido, todos os atributos assumirão como padrão um peso de pesquisa de `1`.

   ![Peso de Pesquisa](./assets/search-weight.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Attribute]**.
