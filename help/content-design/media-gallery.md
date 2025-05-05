---
title: O  [!DNL Media Gallery]
description: Use a Galeria de mídia para organizar e gerenciar seus arquivos de mídia no servidor.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# O [!DNL Media Gallery]

Com o Adobe Commerce ou o Magento Open Source 2.4, os comerciantes podem usar o novo _enhanced_ [!DNL Media Gallery] para organizar e gerenciar seus arquivos de mídia no servidor. Este novo [!DNL Media Gallery] contém as mesmas funcionalidades que o armazenamento de mídia existente, mas inclui uma interface de usuário aprimorada e uma integração mais próxima com o [Adobe Stock][adobe-stock].

![Imagens exibidas na grade da Galeria de Mídia](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Imagens de produtos adicionadas à seção de produtos [_[!UICONTROL Images and Videos]_](../catalog/product-image.md#upload-an-image) não são gerenciadas pelo [!DNL Media Gallery]. Somente imagens usadas nos campos da seção do produto&#x200B;_[!UICONTROL Content]_ são exibidas e filtradas no novo [!DNL Media Gallery].

## Habilitar o novo [!DNL Media Gallery]

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![Configuração avançada - [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Enable Old Media Gallery]** como `No`.

1. Clique em **[!UICONTROL Save Config]**.

1. Quando solicitado, clique no link **[!UICONTROL Cache Management]** na mensagem do sistema e atualize o cache inválido.

   O menu [[!UICONTROL Content] ](/help/content-design/content-menu.md) agora exibe a nova opção _[!UICONTROL Media Gallery]_.

>[!NOTE]
>
>A funcionalidade completa para o novo [!DNL Media Gallery] requer que os consumidores de fila `media.gallery.synchronization` e `media.content.synchronization` sejam iniciados para sincronização inicial. Consulte [Gerenciar filas de mensagens](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) no _Guia de Configuração_ para obter mais detalhes.

## Acessar o novo [!DNL Media Gallery]

O novo [!DNL Media Gallery] pode ser acessado no menu Conteúdo ou quando você [adiciona ou edita uma página](/help/content-design/page-add.md). Você também pode acessá-las ao [criar ou editar uma categoria](/help/catalog/category-create.md) ou ao [inserir imagens usando o Editor de Conteúdo](/help/content-design/editor-insert-image.md).

Para acessar o novo [!UICONTROL Media Gallery] pelo menu [!UICONTROL Content]:

- Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

Para acessar a nova Galeria de mídia ao adicionar ou editar uma página:

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Clique em **[!UICONTROL Add a New Page]**.

   Se quiser editar uma página existente, use a coluna _[!UICONTROL Action]_&#x200B;para clicar em **[!UICONTROL Select]**&#x200B;e escolher **[!UICONTROL Edit]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Content]** e faça o seguinte:

   - Se você tiver o [Page Builder habilitado](../page-builder/setup.md), expanda o painel **[!UICONTROL Media]** e arraste um espaço reservado **[!UICONTROL Image]** para o contêiner de destino. Depois clique em **[!UICONTROL Select from Gallery]**.

     ![Arraste a imagem para o estágio](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - Se o [editor do WYSIWYG](/help/content-design/editor.md) estiver habilitado, clique em **[!UICONTROL Show/Hide Editor]** e em **[!UICONTROL Insert Image]**.

## Demonstração do [!DNL Media Gallery]

Para saber mais sobre o [!DNL Media Gallery], assista a este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12&learn=on)

[adobe-stock]: https://stock.adobe.com

