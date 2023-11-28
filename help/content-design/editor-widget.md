---
title: Inserir um widget no editor
description: Adicione vários elementos de conteúdo a uma página usando a ferramenta widget no editor WYSIWYG.
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Inserir um widget no editor

A variável [widget](widget-create.md) A ferramenta pode ser usada para adicionar vários elementos de conteúdo à página, incluindo links para qualquer página de conteúdo do Commerce ou nó, produto ou categoria. Os links podem ser posicionados na página em formato de bloco ou incorporados diretamente ao conteúdo. Você pode usar a ferramenta Widget para criar links para os seguintes tipos de conteúdo:

- [Páginas de conteúdo](pages.md)
- [Categorias de catálogo](../catalog/categories.md)
- [Catálogo de produtos](../catalog/product-create.md)

Por padrão, os links herdam seu estilo da folha de estilos do tema.

{{$include /help/_includes/directives-caution.md}}

1. Abra uma página, um bloco ou um bloco dinâmico no modo de edição.

1. Vá para a _[!UICONTROL Content]_e clique em qualquer elemento compatível com o editor.

1. Posicione o cursor onde deseja que o widget apareça e clique no botão _Inserir widget_ ícone.

   ![Barra de ferramentas do editor - Inserir widget](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   Se você não tiver o Page Builder ativado e preferir trabalhar com o código, clique em **[!UICONTROL Show / Hide Editor]**. Posicione o ponto de inserção no texto no qual você deseja que o widget apareça. Em seguida, clique em **[!UICONTROL Insert Widget]**.

1. Escolha o **[!UICONTROL Widget Type]**.

   Para obter mais informações sobre essas opções, consulte [Tipos de widget](widgets.md#widget-types). As etapas a seguir usam um exemplo para inserir um link em um produto.

1. Para usar o nome do produto, deixe o campo **[!UICONTROL Anchor Custom Text]** campo vazio.

1. Insira um **[!UICONTROL Anchor Custom Title]** para práticas recomendadas de SEO.

   Este título não está visível na página.

1. Definir **[!UICONTROL Template]** a um dos seguintes:

   - Para incorporar o link ao texto, selecione `Product Link Inline Template`.

   - Para colocar o link em uma linha separada, selecione `Product Link Block Template`.

1. Clique em **[!UICONTROL Select Product]** e faça o seguinte:

   - Na árvore, navegue até a categoria desejada.

   - Na lista, escolha o produto vinculado.

1. Clique em **[!UICONTROL Insert Widget]** para colocar o link na página.

   Se estiver trabalhando com código HTML, uma variável [tag de marcação](../systems/markup-tags.md) para que o link seja exibido na parte superior da página, entre chaves duplas. Se necessário, use _Recortar e colar_ para posicionar a tag de marcação no código em que deseja que o link apareça.

1. Quando as edições de conteúdo estiverem concluídas, clique em **[!UICONTROL Save]**.
