---
title: Licenciar uma imagem do Adobe Stock
description: Para garantir acesso legal e eliminar a marca d'água do Adobe Stock, licencie suas imagens do Adobe Stock.
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Licenciar uma imagem do Adobe Stock

Os ativos do Adobe Stock que você deseja usar para suas lojas de produção da Adobe Commerce e da Magento Open Source devem ser licenciados. Essa licença garante que você tenha acesso legal à imagem e elimina a marca d&#39;água do Adobe Stock presente em todas as [visualizações de imagem](./adobe-stock-save-preview.md). Para licenciar imagens ou salvar imagens já licenciadas, você deve estar conectado à sua conta da Adobe.

O novo [[!DNL Media Gallery]](media-gallery.md) fornece uma integração direta com o Adobe Stock, facilitando a licença de suas imagens diretamente da página da galeria.

>[!BEGINSHADEBOX]

**Pré-requisitos**

O recurso de licenciamento do Adobe Stock só estará disponível se a [Integração do Adobe Stock](./adobe-stock.md) estiver instalada e configurada. O licenciamento de imagens do [Adobe Stock](https://stock.adobe.com) exige um plano Adobe Stock pago e uma [conta Adobe](https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html).

>[!ENDSHADEBOX]

## Licenciar uma imagem do novo [!DNL Media Gallery]

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Siga as etapas em [Usando Imagens do Adobe Stock](./adobe-stock-manage.md) para fazer logon e salvar as imagens de visualização no [armazenamento de mídia](./media-storage.md).

   ![Imagem de visualização salva](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. Clique nos três pontos abaixo da imagem (![ícone do menu Ativo](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}) e clique em **[!UICONTROL License]**.

   ![Ações de imagem do Adobe Stock](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se você não estiver conectado, o formulário de logon será exibido. Para obter mais informações sobre logon, consulte [Usando Imagens do Adobe Stock](./adobe-stock-manage.md).

1. Na caixa de diálogo de confirmação de licenciamento, clique em **[!UICONTROL Confirm]** para licenciar a imagem.

   ![Confirmação de Licença](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >Você deve ter [créditos de Adobe Stock](https://helpx.adobe.com/stock/help/credit-packs.html) disponíveis em sua conta para licenciar a imagem.

## Licenciar uma imagem do armazenamento de mídia padrão

1. [Acesse a grade do Adobe Stock Search][adobe-stock-manage.md].

1. Para [exibir os detalhes da imagem][adobe-stock-manage.md#view-image-details], clique em uma imagem na grade de pesquisa na ordem.

1. Dependendo do status de licenciamento atual da imagem, execute um dos procedimentos a seguir:

   - Se a imagem já estiver licenciada, clique em **[!UICONTROL Save]**.

   - Se a imagem for _não_ licenciada, clique em **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >Você deve ter [créditos de Adobe Stock](https://helpx.adobe.com/stock/help/credit-packs.html) disponíveis em sua conta para licenciar a imagem.

   Esta ação exibe um prompt para que você especifique um nome de arquivo que seja usado para salvar a imagem no [armazenamento de mídia](./media-storage.md). Um nome de arquivo padrão é fornecido, mas você pode personalizar o nome de acordo com suas preferências.

   ![Salvar imagem licenciada do Adobe Stock](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. Clique em **[!UICONTROL Confirm]**.

   A página é redirecionada para o armazenamento de mídia e a visualização salva é exibida.
