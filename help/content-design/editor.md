---
title: Editor WYSIWYG
description: Saiba como usar o editor e trabalhar com conteúdo em uma visualização _What You See Is What You Get_ (WYSIWYG).
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Editor WYSIWYG

O editor oferece a capacidade de inserir e formatar enquanto trabalha em um _O Que Você Vê É O Que Você Obtém_ (WYSIWYG) do conteúdo. Se preferir trabalhar diretamente com o código de HTML subjacente, é possível alterar os modos facilmente. O editor pode ser usado para criar conteúdo para [páginas](pages.md), [blocos](blocks.md), e [descrições do produto](../catalog/product-content.md). Ao trabalhar nos detalhes do produto, acesse o editor clicando em **[!UICONTROL Show / Hide Editor]**.

>[!NOTE]
>
>TinyMCE 5 é o editor WYSIWYG padrão. Uma atualização para a biblioteca TinyMCE 5.10 no Adobe Commerce e no Magento Open Source 2.4.5 resolve uma vulnerabilidade que permitia a execução arbitrária do JavaScript ao atualizar uma imagem ou link usando alguns tipos de URLs. O TinyMCE 3 foi descontinuado na versão 2.4.0 e removido na versão 2.4.3. O TinyMCE 4 foi removido na versão 2.4.4.

![Barra de ferramentas do editor](./assets/editor-toolbar.png){width="700" zoomable="yes"}

Os tópicos a seguir fornecem informações detalhadas sobre o uso do editor:

- [Inserção de um link](editor-insert-link.md)
- [Inserção de uma imagem](editor-insert-image.md)
- [Inserir um widget](editor-widget.md)
- [Inserção de uma variável](editor-insert-variable.md)

## Configurar o editor

O editor WYSIWYG é ativado por padrão e pode ser usado para editar conteúdo em páginas e blocos CMS e em produtos e categorias. Na configuração do, você pode ativar ou desativar o editor e optar por usar estático, em vez de [dinâmico](../catalog/catalog-urls.md#dynamic-url), URLs para conteúdo de mídia nas descrições de produto e categoria.

![Opções WYSIWYG](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

Para obter uma descrição detalhada de todas as opções WYSIWYG, consulte [Gestão de conteúdo](../configuration-reference/general/content-management.md) no _Referência de configuração_.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Content Management]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. Definir **[!UICONTROL Enable WYSIWYG Editor]** de acordo com sua preferência.

   O editor é ativado por padrão.

1. Definir **[!UICONTROL Static URLs for Media Content in WYSIWYG]** de acordo com sua preferência por todos [conteúdo de mídia](../catalog/catalog-urls.md#static-url) que é inserido com o editor WYSIWYG.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
