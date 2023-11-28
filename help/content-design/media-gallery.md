---
title: A variável [!DNL Media Gallery]
description: Use a Galeria de mídia para organizar e gerenciar seus arquivos de mídia no servidor.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# A variável [!DNL Media Gallery]

Com o Adobe Commerce ou o Magento Open Source 2.4, os comerciantes podem usar o novo _aprimorado_ [!DNL Media Gallery] para organizar e gerenciar os arquivos de mídia no servidor. Este novo [!DNL Media Gallery] O contém as mesmas funcionalidades que o armazenamento de mídia existente, mas inclui uma interface de usuário aprimorada e uma integração mais estreita com o [Adobe Stock][adobe-stock].

![Imagens exibidas na grade da Galeria de mídia](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Imagens do produto adicionadas à [_[!UICONTROL Images and Videos]_seção do produto](../catalog/product-image.md#upload-an-image) não são gerenciados pela [!DNL Media Gallery]. Somente imagens usadas na_[!UICONTROL Content]_ os campos de seção do produto são exibidos e filtrados no novo [!DNL Media Gallery].

## Ativar o novo [!DNL Media Gallery]

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![Configuração avançada - [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Enable Old Media Gallery]** para `No`.

1. Clique em **[!UICONTROL Save Config]**.

1. Quando solicitado, clique no link **[!UICONTROL Cache Management]** vincular na mensagem do sistema e atualizar o cache inválido.

   A variável [[!UICONTROL Content] menu](/help/content-design/content-menu.md) agora exibe o novo _[!UICONTROL Media Gallery]_opção.

>[!NOTE]
>
>Funcionalidade completa para novos [!DNL Media Gallery] exige `media.gallery.synchronization` e `media.content.synchronization` consumidores de fila a serem iniciados para sincronização inicial. Consulte [Gerenciar filas de mensagens](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) no _Guia de configuração_ para obter mais detalhes.

## Acesse o novo [!DNL Media Gallery]

O novo [!DNL Media Gallery] pode ser acessada pelo menu Conteúdo ou quando você [adicionar ou editar uma página](/help/content-design/page-add.md). Também é possível acessá-lo quando você [criar ou editar uma categoria](/help/catalog/category-create.md)ou quando você [inserir imagens usando o Editor de conteúdo](/help/content-design/editor-insert-image.md).

Para acessar o novo [!UICONTROL Media Gallery] por meio da [!UICONTROL Content] menu:

- No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

Para acessar a nova Galeria de mídia ao adicionar ou editar uma página:

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Clique em **[!UICONTROL Add a New Page]**.

   Se quiser editar uma página existente, use o _[!UICONTROL Action]_coluna para clicar **[!UICONTROL Select]**e escolha **[!UICONTROL Edit]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Content]** e faça o seguinte:

   - Se você tiver [Page Builder ativado](../page-builder/setup.md), expanda a **[!UICONTROL Media]** e arraste um **[!UICONTROL Image]** espaço reservado para o contêiner de destino. Clique em **[!UICONTROL Select from Gallery]**.

     ![Arrastar imagem para o estágio](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - Se você tiver o [Editor WYSIWYG habilitado](/help/content-design/editor.md), clique em **[!UICONTROL Show/Hide Editor]** e clique em **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] demonstração

Para saber mais sobre o [!DNL Media Gallery], assista a este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12)

[adobe-stock]: https://stock.adobe.com

