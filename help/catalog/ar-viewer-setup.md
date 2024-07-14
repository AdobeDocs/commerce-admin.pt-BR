---
title: '[!DNL AR Viewer] para instalação do Adobe Commerce'
description: Saiba mais sobre como gerenciar ativos de modelo 3D usando a extensão  [!DNL AR Viewer]  para suas listas de produtos.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '293'
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
> Para uma série de vídeos de demonstração de um usuário que adiciona um modelo 3d a um produto, consulte a página [Visualizador de AR para Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) em _Vídeos e Tutorials do Commerce_.
