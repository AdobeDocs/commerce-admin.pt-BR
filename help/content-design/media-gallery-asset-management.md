---
title: Gerenciamento de ativos da Galeria de mídia
description: Saiba como gerenciar arquivos de mídia carregados e ativos adquiridos por meio de uma integração com o Adobe Stock.
exl-id: 4fc489ae-b1e5-4aa4-832d-cd88c58d103a
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# Gerenciamento de ativos da Galeria de mídia

A nova [Galeria de Mídia](media-gallery.md) fornece ferramentas para gerenciar arquivos de mídia carregados e ativos adquiridos por meio de uma [integração com o Adobe Stock](adobe-stock.md). Se você tiver salvo uma [visualização de imagem](adobe-stock-save-preview.md) do Adobe Stock, também poderá [licenciar](adobe-stock-license-image.md) a imagem na nova Galeria de Mídia.

## Fazer upload de um ativo

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Clique em **[!UICONTROL Upload Image]**.

1. Selecione o arquivo a ser carregado.

   O ativo selecionado é carregado automaticamente na pasta selecionada (ou na raiz de armazenamento se nenhuma pasta for selecionada).

## Exibir detalhes do ativo

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Clique nos três pontos abaixo do ativo (![ícone de Detalhes](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}) e clique em **[!UICONTROL View Details]**.

   ![Ações de ativos](./assets/media-gallery-asset-actions.png){width="600" zoomable="yes"}

   Os detalhes do ativo são exibidos em um painel deslizante. Eles incluem as informações em que o ativo está sendo usado:

   - **[!UICONTROL Categories]**
   - **[!UICONTROL Products]**
   - **[!UICONTROL Pages]**
   - **[!UICONTROL Blocks]**

   ![Detalhes do ativo](./assets/media-gallery-asset-details.png){width="600" zoomable="yes"}

   Para ver os detalhes, clique nos links **[!UICONTROL Used In]**. A grade no exemplo a seguir mostra todas as categorias em que um ativo específico é usado.

   ![Grade de Categorias](./assets/media-gallery-asset-categories.png){width="600" zoomable="yes"}

   Também é possível excluir o ativo da seção _Exibir detalhes_.

## Editar um ativo

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Clique nos três pontos abaixo do ativo (![ícone do menu Ativo](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}) e clique em **[!UICONTROL Edit]**.

   ![Editar ativo](./assets/media-gallery-edit-asset.png){width="600" zoomable="yes"}

1. Se necessário, altere um dos seguintes valores de metadados:

   - **[!UICONTROL Title]**
   - **[!UICONTROL Description]**
   - **[!UICONTROL Tags/Keywords]**

   Esses dados são salvos na base de dados e nos próprios metadados do arquivo. Atualmente, os formatos XMP e IPTC são compatíveis.

   Você pode baixar a imagem com os metadados atualizados.

## Usar um ativo

O Assets pode ser usado extensivamente pelo Administrador, como [adicionar ou editar uma página](page-add.md), [criar ou editar uma categoria](../catalog/category-create.md) ou [inserir imagens do Editor de Conteúdo](editor-insert-image.md).

1. Acesse a nova Galeria de mídia em uma área que permite usar ativos de mídia.

1. Selecione o ativo e clique em **[!UICONTROL Add Selected]**.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

## Excluir ativos

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Clique em **[!UICONTROL Delete Images...]** e marque a caixa de seleção de cada ativo que deseja excluir.

1. No diálogo de confirmação, clique em **[!UICONTROL Delete Image]**.

   ![Confirmação de Exclusão](./assets/media-gallery-bulk-delete-confirm.png){width="500" zoomable="yes"}

## Pesquisar por ativos

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Use a entrada **[!UICONTROL Search by keywords]** para executar a pesquisa de imagem por palavras-chave/tags.

   A pesquisa no exemplo a seguir encontra ativos que contêm uma marca específica (`mountain`).

   ![Pesquisa de ativos](./assets/media-gallery-asset-search.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Para saber como atualizar marcas de imagem, consulte a seção _[Editar um ativo](#edit-an-asset)_.

## Filtrar ativos

>[!NOTE]
>
>A funcionalidade _Usada em_ requer que [!UICONTROL Media Gallery Image Optimization] esteja habilitada nas [configurações](media-gallery-image-optimization.md).

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Clique na guia **[!UICONTROL Filters]**.

   ![Filtros](./assets/media-gallery-filters.png){width="600" zoomable="yes"}

1. Defina as opções de filtro.

   Você pode filtrar os ativos de acordo com o uso pelas entidades:

   - **[!UICONTROL Used in Categories]**
   - **[!UICONTROL Used in Products]**
   - **[!UICONTROL Used in Pages]**
   - **[!UICONTROL Used in Blocks]**

   Você também pode filtrar os ativos por **[!UICONTROL Store View]**, **[!UICONTROL License Status]** e **[!UICONTROL Content Status]**. Defina um intervalo de datas para **[!UICONTROL Uploaded Date]** e/ou **[!UICONTROL Modification Date]** para filtrar ativos de acordo com as datas do arquivo.

1. Clique em **[!UICONTROL Apply Filters]** para ver os resultados.

   A filtragem no exemplo a seguir encontra ativos que são usados em uma categoria específica (`cars`) e estão habilitados.

   ![Filtrar Assets Habilitado por Categoria](./assets/media-gallery-filter-by-category.png){width="600" zoomable="yes"}

## Localizar duplicatas de imagem

1. Clique na guia **[!UICONTROL Filters]** e marque a caixa de seleção **[!UICONTROL Show duplicates]**.

1. Para ver os resultados, clique em **[!UICONTROL Apply Filters]**.
