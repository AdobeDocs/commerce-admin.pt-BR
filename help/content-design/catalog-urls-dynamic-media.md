---
title: URLs de mídia dinâmica
description: Saiba mais sobre como usar um URL de mídia dinâmica como uma referência relativa a uma imagem ou outro ativo de mídia.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
source-git-commit: d3b9b4cd0d12f8d5feb2bad0bf601970f9ee1a36
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# URLs de mídia dinâmica

Um URL de mídia dinâmica é uma referência relativa a uma imagem ou outro ativo de mídia. Quando ativados, os URLs de mídia dinâmica podem ser usados para vincular diretamente aos ativos no servidor ou aos arquivos armazenados em um [rede de entrega de conteúdo](media-storage-content-delivery-network.md). O uso de URLs de mídia dinâmica pode afetar o desempenho do catálogo e a [editor](editor.md#configure-the-editor) O pode ser configurado para usar URLs de mídia estática ou dinâmica.

Como em todos [tags de marcação](../systems/markup-tags.md), a diretiva está entre chaves duplas. O formato de um URL de mídia dinâmica é semelhante ao seguinte:

`\{\{media url="path/to/image.jpg"}}`

As diretivas de URL dinâmicas são processadas a partir do conteúdo de HTML salvo quando a página é renderizada na loja. Cada vez que a página é renderizada, o conteúdo é verificado `\{\{media url="..."}}` e cada diretiva é substituída pelo URL de mídia correspondente.

{{$include /help/_includes/directives-caution.md}}

## Configurar URLs de mídia estática

Por padrão, as imagens inseridas no catálogo do editor WYSIWYG têm URLs relativos e dinâmicos. Se preferir usar um URL estático, é possível alterar a definição da configuração.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Content Management]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL WYSIWYG Options]** seção.

   ![Opções WYSIWYG](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** a um dos seguintes:

   - `Yes` - Usa URLs estáticos para conteúdo de mídia inserido com o editor WYSIWYG. Os URLs estáticos são absolutos e quebrados se a variável [URL base](../stores-purchase/store-urls.md) das alterações no armazenamento.

   - `No` - (Padrão) Usa URLs dinâmicos para conteúdo de mídia inserido com o editor WYSIWYG, com base no `\{\{media url="..."}}` diretiva. Os URLs dinâmicos são relativos e não se quebram se o URL de base do armazenamento for alterado.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
