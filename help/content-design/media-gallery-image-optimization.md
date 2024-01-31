---
title: Otimização de imagem da Galeria de mídia
description: Saiba como usar a otimização de imagem para o seu [!DNL Commerce] ativos de mídia.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Otimização de imagem da Galeria de mídia

O novo [Galeria de mídia](media-gallery.md) fornece um _otimização de imagem_ o recurso, que melhora o desempenho e diminui o tamanho dos arquivos de mídia na loja. Essa otimização é habilitada por padrão e pode ser modificada nas configurações da loja.

## Configurar otimização de imagem

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** e faça o seguinte:

   - Definir **[!UICONTROL Enable Image Optimization]** para `Yes`.
   - Insira o **[!UICONTROL Maximum Width]** e **[!UICONTROL Maximum Height]** valores (em pixels) de acordo com suas necessidades.

## Comportamento

Quando a funcionalidade de otimização de imagem da Galeria de mídia está habilitada, uma cópia otimizada de uma imagem é inserida automaticamente no conteúdo do [Galeria de mídia](media-gallery.md) em vez do arquivo original.

Quando a variável _Largura máxima_ e _Altura máxima_ forem alterados na configuração, ela atualizará todas as imagens otimizadas existentes que foram inseridas anteriormente.

A Otimização de imagem da galeria de mídia exige que o `media.gallery.renditions.update` os consumidores da fila do estão executando para regenerar imagens otimizadas quando a configuração é alterada. Consulte [Gerenciar filas de mensagens](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) no _Guia de configuração_ para obter mais detalhes.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
