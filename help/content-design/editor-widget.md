---
title: Inserir um widget no editor
description: Adicione vários elementos de conteúdo a uma página usando a ferramenta widget no editor do WYSIWYG.
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# Inserir um widget no editor

A ferramenta [widget](widget-create.md) pode ser usada para adicionar vários elementos de conteúdo à página, incluindo links para qualquer página de conteúdo ou nó, produto ou categoria do Commerce. Os links podem ser posicionados na página em formato de bloco ou incorporados diretamente ao conteúdo. Você pode usar a ferramenta Widget para criar links para os seguintes tipos de conteúdo:

- [Páginas de conteúdo](pages.md)
- [Categorias de catálogo](../catalog/categories.md)
- [Catálogo de produtos](../catalog/product-create.md)

Por padrão, os links herdam seu estilo da folha de estilos do tema.

{{$include /help/_includes/directives-caution.md}}

1. Abra uma página, um bloco ou um bloco dinâmico no modo de edição.

1. Vá para a seção _[!UICONTROL Content]_&#x200B;e clique em qualquer elemento compatível com o editor.

1. Posicione o cursor onde deseja que o widget apareça e clique no ícone _Inserir Widget_.

   ![Barra de ferramentas do editor - Inserir widget](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   Se você não tiver o Page Builder habilitado e preferir trabalhar com o código, clique em **[!UICONTROL Show / Hide Editor]**. Posicione o ponto de inserção no texto no qual você deseja que o widget apareça. Em seguida, clique em **[!UICONTROL Insert Widget]**.

1. Escolha o **[!UICONTROL Widget Type]**.

   Para obter mais informações sobre essas opções, consulte [Tipos de widget](widgets.md#widget-types). As etapas a seguir usam um exemplo para inserir um link em um produto.

1. Para usar o nome do produto, deixe o campo **[!UICONTROL Anchor Custom Text]** vazio.

1. Insira um **[!UICONTROL Anchor Custom Title]** para a prática recomendada de SEO.

   Este título não está visível na página.

1. Defina **[!UICONTROL Template]** como um dos seguintes:

   - Para incorporar o link ao texto, selecione `Product Link Inline Template`.

   - Para colocar o link em uma linha separada, selecione `Product Link Block Template`.

1. Clique em **[!UICONTROL Select Product]** e faça o seguinte:

   - Na árvore, navegue até a categoria desejada.

   - Na lista, escolha o produto vinculado.

1. Clique em **[!UICONTROL Insert Widget]** para colocar o link na página.

   Se você estiver trabalhando com código HTML, uma [marca de marcação](../systems/markup-tags.md) para o link aparecerá na parte superior da página, entre chaves duplas. Se necessário, use _Recortar e Colar_ para posicionar a marca de marcação no código onde deseja que o link apareça.

1. Quando as edições de conteúdo forem concluídas, clique em **[!UICONTROL Save]**.
