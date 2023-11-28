---
title: Licenciar uma imagem do Adobe Stock
description: Para garantir acesso legal e eliminar a marca d'água do Adobe Stock, licencie suas imagens do Adobe Stock.
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Licenciar uma imagem do Adobe Stock

Os ativos do Adobe Stock que você deseja usar para suas lojas de produção Adobe Commerce e Magento Open Source devem ser licenciados. Essa licença garante que você tenha acesso legal à imagem e elimine a marca d&#39;água do Adobe Stock presente em todos [visualizações de imagem][save-preview]. Para licenciar imagens ou salvar imagens já licenciadas, você precisa estar conectado à sua conta Adobe.

O novo [[!DNL Media Gallery]](media-gallery.md) O fornece uma integração direta com o Adobe Stock, facilitando o licenciamento de imagens diretamente da página da galeria.

## Pré-requisitos

Esse recurso exige o [Integração do Adobe Stock][adobe-stock-integration] módulo e configuração. Licenciamento [Adobe Stock][adobe-stock] imagens exige um plano Adobe Stock pago e uma [conta Adobe][adobe-signin].

## Licenciar uma imagem do novo [!DNL Media Gallery]

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Siga as etapas em [Uso de imagens do Adobe Stock][using-adobe-stock] para fazer logon e salvar as imagens de visualização na [armazenamento de mídia][media-storage].

   ![Imagem de visualização salva](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. Clique nos três pontos abaixo da imagem (![Ícone do menu Ativo](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}) e clique em **[!UICONTROL License]**.

   ![Ações de imagem do Adobe Stock](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se você não estiver conectado, o formulário de logon será exibido. Para obter mais informações sobre logon, consulte [Uso de imagens do Adobe Stock][using-adobe-stock].

1. Na caixa de diálogo de confirmação de licenciamento, clique em **[!UICONTROL Confirm]** para licenciar a imagem.

   ![Confirmação de licença](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >Você deve ter o disponível [Créditos do Adobe Stock][stock-credits] em sua conta para licenciar a imagem.

## Licenciar uma imagem do armazenamento de mídia padrão

1. [Acessar a grade do Adobe Stock Search][access-search].

1. Para [exibir os detalhes da imagem][view-details], clique em uma imagem na grade de pesquisa em ordem.

1. Dependendo do status de licenciamento atual da imagem, execute um dos procedimentos a seguir:

   - Se a imagem já estiver licenciada, clique em **[!UICONTROL Save]**.

   - Se a imagem for _não_ licenciado, clique em **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >Você deve ter o disponível [Créditos do Adobe Stock][stock-credits] em sua conta para licenciar a imagem.

   Essa ação exibe um prompt para que você especifique um nome de arquivo que seja usado para salvar a imagem na [armazenamento de mídia][media-storage]. Um nome de arquivo padrão é fornecido, mas você pode personalizar o nome de acordo com suas preferências.

   ![Salvar imagem licenciada do Adobe Stock](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. Clique em **[!UICONTROL Confirm]**.

   A página é redirecionada para o armazenamento de mídia e a visualização salva é exibida.

[adobe-stock-integration]: adobe-stock.md
[media-storage]: media-storage.md
[using-adobe-stock]: adobe-stock-manage.md
[save-preview]: adobe-stock-save-preview.md
[access-search]: adobe-stock-manage.md#access-the-adobe-stock-search-grid
[view-details]: adobe-stock-manage.md#view-image-details
[stock-credits]: https://helpx.adobe.com/stock/help/credit-packs.html
[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
