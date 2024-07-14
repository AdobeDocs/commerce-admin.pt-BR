---
title: Editor WYSIWYG
description: Saiba como usar o editor e trabalhar com conteúdo em uma visualização _What You See Is What You Get_ (WYSIWYG).
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Editor WYSIWYG

O editor oferece a capacidade de inserir e formatar o conteúdo enquanto você trabalha em uma exibição _O que você vê é o que você obtém_ (WYSIWYG) do conteúdo. Se preferir trabalhar diretamente com o código de HTML subjacente, é possível alterar os modos facilmente. O editor pode ser usado para criar conteúdo para [páginas](pages.md), [blocos](blocks.md) e [descrições de produtos](../catalog/product-content.md). Ao trabalhar nos detalhes do produto, acesse o editor clicando em **[!UICONTROL Show / Hide Editor]**.

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

O editor WYSIWYG é ativado por padrão e pode ser usado para editar conteúdo em páginas e blocos CMS e em produtos e categorias. Na configuração, você pode ativar ou desativar o editor e optar por usar URLs estáticos, em vez de [dinâmicos](../catalog/catalog-urls.md#dynamic-url), para conteúdo de mídia nas descrições de produto e categoria.

![Opções WYSIWYG](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

Para obter uma descrição detalhada de todas as opções WYSIWYG, consulte [Gerenciamento de Conteúdo](../configuration-reference/general/content-management.md) na _Referência de Configuração_.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Content Management]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. Defina **[!UICONTROL Enable WYSIWYG Editor]** de acordo com sua preferência.

   O editor é ativado por padrão.

1. Defina **[!UICONTROL Static URLs for Media Content in WYSIWYG]** como sua preferência para todo o [conteúdo de mídia](../catalog/catalog-urls.md#static-url) inserido com o editor WYSIWYG.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
