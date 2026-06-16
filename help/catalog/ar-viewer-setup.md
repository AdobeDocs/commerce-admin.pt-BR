---
title: '[!DNL AR Viewer] para configuração do Adobe Commerce'
description: Saiba mais sobre como gerenciar ativos de modelo 3D usando a extensão  [!DNL AR Viewer]  para suas listas de produtos.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
TQID: https://experienceleague.adobe.com/6OlcZ4Psm3INgVm7f-Y9JvqfUdmR6Rg48tcigLAHiaE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 313
ht-degree: 0%

---

# Gerenciar modelos de produtos 3D com o [!DNL AR Viewer] for Adobe Commerce

Para cada produto, você pode carregar um arquivo `.USDZ` que permite que os modelos AR e 3D sejam usados em sua lista de produtos.

O [!DNL AR Viewer] dá suporte apenas a `.USDZ` arquivos.

## Instalar a extensão

[!DNL AR Viewer] está instalado como uma extensão do [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

Consulte o [_Guia de Instalação_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) para obter mais informações sobre o processo de instalação da extensão.

Depois que a extensão [!DNL AR Viewer] for instalada e configurada, os usuários administradores poderão configurar, personalizar e gerenciar listas de produtos para incluir modelos 3D.

## Adicionar um modelo 3D

1. Abra o produto no modo de edição.

1. Para trabalhar com uma exibição de loja específica, defina o seletor de **[!UICONTROL Store View]** como a exibição aplicável.

   >[!NOTE]
   >
   >Os novos modelos de produtos 3D são _sempre_ carregados e visíveis em _todos_ visualizações da loja, mesmo se o escopo `All Store Views` não for usado para carregamento. <br/><br/>Para ocultar modelos 3D de produtos de um modo de exibição de loja específico, alterne para o Modo de Exibição de Loja, marque a caixa de seleção **[!UICONTROL Hide from Product Page]** do modelo 3D e clique em **[!UICONTROL Save]**.

1. Role para baixo e expanda a seção _[!UICONTROL Product 3D Model]_.

   ![Menu Pop-up](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Adicione o modelo 3D (arquivo `.USDZ`) do produto.

1. Clique em **[!UICONTROL Save]**.

### Excluir um modelo 3D

Para remover um modelo 3D dos detalhes do produto:

1. Clique em **[!UICONTROL Delete]**.

1. Clique em **[!UICONTROL Save]**.

## Exibir modelos de produto 3D

Quando os detalhes do produto forem atualizados com o modelo 3D:

1. O [!DNL AR Viewer] gera um código QR na descrição do produto que codifica o arquivo AR.

1. Um cliente pode ver esse código QR na página do produto.

1. Quando os clientes digitalizam o código QR com seus dispositivos móveis, uma experiência de AR é renderizada no dispositivo móvel.

>[!NOTE]
>
> Para obter uma série de vídeos de demonstração de um usuário que adiciona um modelo 3d a um produto, consulte a página [Visualizador de AR para Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) em _Vídeos e tutoriais do Commerce_.
