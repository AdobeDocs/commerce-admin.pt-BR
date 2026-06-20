---
title: URLs de mídia dinâmica
description: Saiba mais sobre como usar um URL de mídia dinâmica como uma referência relativa a uma imagem ou outro ativo de mídia.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/nml-pHTHdSPcvIVnRwlyjJPhEo2PWdTEKfkn2AFKjvA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# URLs de mídia dinâmica

Um URL de mídia dinâmica é uma referência relativa a uma imagem ou outro ativo de mídia. Quando habilitadas, as URLs de mídia dinâmica podem ser usadas para vincular diretamente aos ativos no servidor ou aos arquivos armazenados em uma [rede de entrega de conteúdo](media-storage-content-delivery-network.md). O uso de URLs de mídia dinâmica pode afetar o desempenho do catálogo, e o [editor](editor.md#configure-the-editor) pode ser configurado para usar URLs de mídia estática ou dinâmica.

Como em todas as [marcas de marcação](../systems/markup-tags.md), a diretiva é delimitada por chaves duplas. O formato de um URL de mídia dinâmica é semelhante ao seguinte:

`\{\{media url="path/to/image.jpg"}}`

As diretivas de URL dinâmicas são processadas a partir do conteúdo HTML salvo quando a página é renderizada na loja. Cada vez que a página é renderizada, o conteúdo é verificado em busca de `\{\{media url="..."}}` e cada diretiva é substituída pela URL de mídia correspondente.

{{$include /help/_includes/directives-caution.md}}

## Configurar URLs de mídia estática

Por padrão, as imagens inseridas no catálogo do editor do WYSIWYG têm URLs relativos e dinâmicos. Se preferir usar um URL estático, é possível alterar a definição da configuração.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Content Management]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL WYSIWYG Options]**.

   ![Opções do WYSIWYG](../configuration-reference/general/assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

>[!NOTE]
>
>O TinyMCE foi substituído pelo Hugerte como editor padrão do WYSIWYG no Magento 2.4.6 e versões posteriores.

1. Defina **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** como um dos seguintes:

   - `Yes` - Usa URLs estáticas para conteúdo de mídia inserido com o editor do WYSIWYG. As URLs estáticas são absolutas e quebradas se a [URL de base](../stores-purchase/store-urls.md) do armazenamento for alterada.

   - `No` - (Padrão) Usa URLs dinâmicas para conteúdo de mídia inserido com o editor do WYSIWYG, com base na diretiva `\{\{media url="..."}}`. Os URLs dinâmicos são relativos e não se quebram se o URL de base do armazenamento for alterado.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
