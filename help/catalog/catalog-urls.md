---
title: URLs de catálogo e produto
description: Saiba mais sobre os tipos de formato de URL para seus produtos de catálogo e como configurá-los.
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 1edab49fd8d52a1b7414eb207a21c5c03200e75e
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# URLs de catálogo e produto

Os URLs atribuídos a produtos e categorias desempenham um papel importante para determinar o desempenho de indexação do site por mecanismos de pesquisa. Antes de começar a criar seu catálogo, considere as opções disponíveis. Para exibir o formato de URL atual, vá para a loja e navegue para qualquer produto no catálogo. O formato do URL depende das definições de configuração atuais e do método usado para localizar a página.

## Formatos de URL

### URL dinâmico

Uma URL dinâmica é criada _imediatamente_ e pode incluir uma cadeia de caracteres de consulta com variáveis para a ID do produto, ordem de classificação e página onde a solicitação foi feita. Quando um cliente pesquisa um produto em sua loja, o URL resultante pode ser semelhante ao seguinte:

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### URL estático

Um URL estático é um endereço fixo para uma página específica. Uma URL estática pode ser exibida em um formato compatível com o mecanismo de pesquisa ou que faça referência a produtos e categorias por ID. Esses URLs incluem palavras que as pessoas podem usar para procurar um produto e exigem regravações do servidor da Web para serem ativadas. Arquivos com URLs estáticos são normalmente usados para páginas de produto e categoria, páginas de conteúdo e [ativos de tema](../content-design/theme-assets.md).

- `http://mystore.com/antonia-racer-tank.html`

## Componentes do URL

### Chave do URL

A chave do URL é a parte de um URL estático que descreve o produto ou categoria. Ao criar um produto ou categoria, uma chave de URL inicial é gerada automaticamente, com base no nome. Para alterar a chave da URL, consulte a seção [Otimização do Mecanismo de Pesquisa](product-search-engine-optimization.md) das informações do produto.

>[!NOTE]
>
>Por padrão, caracteres especiais acentuados são substituídos automaticamente por suas versões regulares sem acentos na chave do URL. Por exemplo, `ñ` é automaticamente substituído por `n`. Este comportamento pode ser desabilitado definindo a opção de configuração _[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_&#x200B;como `No`. Consulte [Configurar URLs de catálogo](#configure-catalog-urls).

A chave do URL deve consistir em caracteres minúsculos com hifens não à direita entre esses caracteres para separar palavras. Não são permitidos hifens no início ou no final da chave de URL. Uma chave de URL bem projetada e &quot;compatível com mecanismo de pesquisa&quot; pode incluir o nome do produto e palavras-chave para melhorar a maneira como é indexada por mecanismos de pesquisa. A chave do URL pode ser configurada para criar um redirecionamento automático se a chave do URL mudar.

>[!NOTE]
>
>Para estender as personalizações de URL, como URLs localizadas, consulte [Substituições de URL](../merchandising-promotions/url-rewrite.md) para obter mais informações.

### Sufixo HTML

Seu catálogo pode ser configurado para incluir ou excluir o sufixo como parte da categoria e dos URLs do produto. Há vários motivos pelos quais as pessoas podem optar por usar ou omitir o sufixo. Alguns acreditam que o sufixo não serve mais qualquer propósito útil, e que as páginas sem um sufixo são indexadas mais efetivamente por mecanismos de pesquisa. No entanto, sua empresa pode ter um formato padronizado para URLs que exigem um sufixo.

Como o sufixo é controlado pela configuração do sistema, você nunca deve digitá-lo diretamente na chave do URL de uma categoria ou produto. (Isso resulta em um sufixo duplo no final do URL.) Se você decidir usar ou não o sufixo, seja consistente e use a mesma configuração para todas as páginas de produto e categoria. Estes são exemplos de URLs com (e sem) um sufixo.

#### URL com sufixo HTML

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### URL sem sufixo HTML

- `http://mystore.com/helena-hooded-fleece`

### Caminho da categoria

Você pode configurar os URLs do produto para incluir ou excluir o caminho da categoria com base em suas preferências. Por padrão, o caminho da categoria não é incluído nos URLs do produto. No entanto, as categorias aninhadas sempre exibirão o caminho completo da categoria em seus URLs na loja, garantindo clareza e consistência na navegação da categoria. Os exemplos a seguir mostram o mesmo URL de produto com e sem o caminho da categoria.

#### URL do produto com caminho da categoria

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### URL do produto sem caminho de categoria

- `http://mystore.com/helena-hooded-fleece.html`

Para impedir que mecanismos de pesquisa indexem vários URLs que levam ao mesmo conteúdo, você pode excluir o caminho da categoria do URL. Outro método é usar uma meta tag canônica para informar aos mecanismos de pesquisa quais URLs devem ser indexados e quais devem ser ignorados. Por padrão, o Commerce não inclui o caminho da categoria nos URLs do produto.

## Configurar URLs de catálogo

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Search Engine Optimizations]** e defina as opções:

   - Defina **[!UICONTROL Product URL Suffix]** como `html` ou `htm`. Insira o sufixo sem um ponto, pois ele é aplicado automaticamente.

   - Defina **[!UICONTROL Category URL Suffix]** como `html` ou `htm`. Insira o sufixo sem um ponto, pois ele é aplicado automaticamente.

   - Defina **[!UICONTROL Use Categories Path for Product URLs]** de acordo com sua preferência.

   ![Otimização do Mecanismo de Pesquisa](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada dessas opções, consulte [Otimização do Mecanismo de Pesquisa](../configuration-reference/catalog/catalog.md#search-engine-optimization) na _Referência de Configuração_.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Quando solicitado, clique no link **[!UICONTROL Cache Management]** na mensagem do sistema e atualize o cache inválido.

   ![Atualizar cache](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   Para obter mais informações sobre essas opções, consulte [Atualizar caches](../systems/cache-management.md#refresh-specific-caches).

## Configurar formato de URL da mídia de catálogo

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL General]** e escolha **[!UICONTROL Web]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Url Options]** e defina as opções:

![Web > Opções Gerais](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| Campo | [Escopo](../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | Global | Se as substituições do servidor Web estiverem ativadas, habilitar essa configuração inserirá o Código de armazenamento da exibição atual no URL. Opções: `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | Global | (Para configurações de loja única) Se houver um link quebrado em seu site, isso redirecionará o tráfego para o URL base em vez de para uma página com uma mensagem &quot;Página 404 não encontrada&quot;. Opções: `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_Importante!_**&#x200B;Não use o redirecionamento automático para a URL de base para configurações de várias lojas. |
| [!UICONTROL Catalog media URL format] | Global | Define o formato de URL atribuído aos produtos e categorias. Opções: <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**- Define o nome de arquivo convertido como um valor de hash exclusivo.<br />**[!UICONTROL Image optimization based on query parameters]** - Define o processo [otimização de imagem](../content-design/media-gallery-image-optimization.md), dependendo dos parâmetros de consulta. |

{style="table-layout:auto"}
