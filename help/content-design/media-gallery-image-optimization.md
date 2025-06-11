---
title: Otimização de imagem da Galeria de mídia
description: Saiba como usar a otimização de imagens para seus [!DNL Commerce] ativos de mídia.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Otimização de imagem da Galeria de mídia

A nova [Galeria de Mídia](media-gallery.md) fornece um recurso de _otimização de imagem_, que melhora o desempenho e diminui o tamanho dos arquivos de mídia na loja. Essa otimização é habilitada por padrão e pode ser modificada nas configurações da loja.

## Configurar otimização de imagem

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** e faça o seguinte:

   - Defina **[!UICONTROL Enable Image Optimization]** como `Yes`.
   - Insira os valores de **[!UICONTROL Maximum Width]** e **[!UICONTROL Maximum Height]** (em pixels) de acordo com suas necessidades.

## Comportamento

Quando a funcionalidade de otimização de imagem da Galeria de Mídia está habilitada, uma cópia otimizada de uma imagem é inserida automaticamente no conteúdo da [Galeria de Mídia](media-gallery.md) em vez do arquivo original.

Quando os valores de _Largura Máxima_ e _Altura Máxima_ são alterados na configuração, ele atualiza todas as imagens otimizadas existentes que foram inseridas anteriormente.

A Otimização de Imagens da Galeria de Mídia exige que os `media.gallery.renditions.update` consumidores da fila estejam em execução para regenerar imagens otimizadas quando a configuração for alterada. Consulte [Gerenciar filas de mensagens](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) no _Guia de Configuração_ para obter mais detalhes.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
