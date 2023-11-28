---
title: '[!DNL AR Viewer] para configuração do Adobe Commerce'
description: Saiba mais sobre como gerenciar ativos de modelo 3D usando o [!DNL AR Viewer] para suas listagens de produtos.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Gerenciar modelos de produtos 3D com o [!DNL AR Viewer] para Adobe Commerce

Para cada produto, você pode fazer upload de um `.USDZ` arquivo que permite que modelos AR e 3D sejam usados em sua lista de produtos.

A variável [!DNL AR Viewer] apenas suporta `.USDZ` arquivos.

## Instalar a extensão

[!DNL AR Viewer] O é instalado como uma extensão do [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

Consulte a [_Guia de instalação_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) para obter mais informações sobre o processo de instalação da extensão.

Depois que a variável [!DNL AR Viewer] for instalada e configurada, os usuários administradores poderão configurar, personalizar e gerenciar listas de produtos para incluir modelos 3D.

## Adicionar um modelo 3D

1. Abra o produto no modo de edição.

1. Para trabalhar com uma visualização de loja específica, defina a **[!UICONTROL Store View]** escolha para a exibição aplicável.

   >[!NOTE]
   >
   >Os novos modelos de produto 3D são _sempre_ carregado e visível no _all_ exibições de loja, mesmo se a variável `All Store Views` o escopo não é usado para upload. <br/><br/>Para ocultar modelos 3D de produtos de uma exibição de loja específica, é necessário alternar para a Exibição de loja, selecione a **[!UICONTROL Hide from Product Page]** para o modelo 3D e clique em **[!UICONTROL Save]**.

1. Role para baixo e expanda a _[!UICONTROL Product 3D Model]_seção.

   ![Menu Pop-up](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Adicionar o modelo 3D (`.USDZ` do produto.

1. Clique em **[!UICONTROL Save]**.

### Excluir um modelo 3D

Para remover um modelo 3D dos detalhes do produto:

1. Clique em **[!UICONTROL Delete]**.

1. Clique em **[!UICONTROL Save]**.

## Exibir modelos de produto 3D

Quando os detalhes do produto forem atualizados com o modelo 3D:

1. A variável [!DNL AR Viewer] O gera um código QR na descrição do produto que codifica o arquivo AR.

1. Um cliente pode ver esse código QR na página do produto.

1. Quando os clientes digitalizam o código QR com seus dispositivos móveis, uma experiência de AR é renderizada no dispositivo móvel.

>[!NOTE]
>
> Para obter uma série de vídeos de demonstração de um usuário adicionando um modelo 3d a um produto, consulte a [Visualizador de AR para Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) página em _Vídeos e Tutorials do Commerce_.
