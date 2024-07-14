---
title: Configuração da imagem do produto
description: Saiba como definir um tamanho máximo de pixel (largura e altura) e redimensionar automaticamente arquivos de imagem do produto durante o upload.
exl-id: d8fce5f8-eddf-4335-9a72-24036db077db
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---

# Configuração da imagem do produto

Se você planeja carregar imagens grandes para visualização na página _[!UICONTROL Product Details]_, considere definir um tamanho máximo de pixel (largura e altura) e redimensionar automaticamente os arquivos no carregamento. Para oferecer suporte a esse tipo de upload de imagem do produto, há uma opção para permitir o redimensionamento automático de arquivos de imagem maiores durante o upload. Para um produto que você deseja adicionar ao catálogo, mas ainda não tem um ativo de imagem para exibir, é possível configurar uma imagem de espaço reservado.

## Redimensionamento de imagem do produto

Ao carregar imagens de produtos, você pode adicionar imagens maiores com tamanhos variados para fornecer zoom detalhado de alta qualidade na página _[!UICONTROL Product Details]_. Para garantir que todas as imagens tenham tamanho e aparência semelhantes, há uma opção de redimensionamento de imagem para garantir que todas as imagens correspondam a um tamanho de pixel específico. Essa opção redimensiona automaticamente todas as imagens do produto usando as configurações, o que pode ajudar no desempenho do zoom, no carregamento mais rápido das imagens e na manutenção de uma aparência uniforme nas imagens do produto.

>[!NOTE]
>
>Para melhor compatibilidade, é recomendável carregar todas as imagens de produtos com o perfil de cores `sRGB`. Todos os outros perfis de cores são convertidos automaticamente para o perfil de cores `sRGB` durante o carregamento da imagem do produto, o que pode causar inconsistência de cores na imagem carregada.

A definição de uma largura e uma altura máximas de pixel redimensiona a imagem para as dimensões físicas por pixel. O Commerce redimensiona a imagem de acordo com a maior quantidade de largura ou altura, mantendo as proporções. A redução da quantidade de qualidade de imagens JPG de reduz o tamanho do arquivo.

Por exemplo, um JPG de 3000 x 2100 pixels com um de 100% pode ser um arquivo de imagem de 5 mb ou maior. O redimensionamento dessa imagem reduziria a largura para 1920 pixels, mantendo proporções e a qualidade para 80%, a fim de fornecer um tamanho de arquivo muito menor com alta qualidade.

### Ativar redimensionamento de imagem

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expanda o ![Seletor de expansão](../assets/icon-display-expand.png) a seção _Configuração de Carregamento de Imagens_.

   Para alterar as configurações padrão, desmarque a caixa de seleção **[!UICONTROL Use system value]**, se necessário.

   ![Configuração de Carregamento de Imagem](../configuration-reference/advanced/assets/system-image-upload-configuration.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada dessas definições de configuração, consulte [_Configuração de Carregamento de Imagem_](../configuration-reference/advanced/system.md#image-upload-configuration) na _Referência de Configuração_.

1. Para habilitar, verifique se **[!UICONTROL Enable Frontend Resize]** está definido como `Yes`.

1. Insira uma configuração **[!UICONTROL Quality]** entre `1` e `100`%.

   Uma configuração entre 80 e 90% é recomendada para um tamanho de arquivo reduzido e alta qualidade.

1. Defina o **[!UICONTROL Maximum Width]** em pixels para a imagem.

   Quando a imagem é redimensionada, ela não excede essa largura e mantém proporções.

1. Defina o **[!UICONTROL Maximum Height]** em pixels para a imagem.

   Quando a imagem é redimensionada, ela não excede essa altura e mantém proporções.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Descrições dos campos

| Campo | [Escopo](../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Quality] | Global | Determina a qualidade de JPG da imagem redimensionada. Uma qualidade inferior reduz o tamanho do arquivo. Recomenda-se de 80 a 90% para ajudar a reduzir o tamanho do arquivo com alta qualidade. Padrão: 80 |
| [!UICONTROL Enable Frontend Resize] | Global | Permite que o Commerce redimensione imagens grandes demais que você pode carregar para a página _[!UICONTROL Product Details]_. O Commerce redimensiona os arquivos de imagem usando o JavaScript ao fazer upload do arquivo. Quando a imagem é redimensionada, ela mantém as proporções exatas, para atender e não exceder o maior tamanho para Largura máxima ou Altura máxima. Padrão: `Yes` |
| [!UICONTROL Maximum Width] | Global | Determina a largura máxima em pixels para a imagem. Quando a imagem é redimensionada, ela não excede essa largura. Padrão: `1920` |
| [!UICONTROL Maximum Height] | Global | Determina a altura máxima em pixels para a imagem. Quando a imagem é redimensionada, ela não excede essa altura. Padrão: `1200` |

{style="table-layout:auto"}

## Espaços reservados para imagens

O Adobe Commerce e o Magento Open Source usam imagens temporárias como espaços reservados até que as imagens permanentes do produto fiquem disponíveis. Um espaço reservado diferente pode ser carregado para cada função. A imagem inicial do espaço reservado é um exemplo de logotipo, que pode ser substituído pela imagem de sua escolha.

![Espaço Reservado para Imagem](./assets/storefront-image-placeholder.png){width="600" zoomable="yes"}

**_Para carregar imagens de espaço reservado:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Expanda o ![ícone de Expansão](../assets/icon-display-expand.png) da seção **[!UICONTROL Product Image Placeholders]**.

   ![Marcadores de posição de imagem do produto](../configuration-reference/catalog/assets/catalog-product-image-placeholders.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada dessas definições de configuração, consulte [_Placeholders de Imagem de Produto_](../configuration-reference/catalog/catalog.md#product-image-placeholders) na _Referência de Configuração_.

1. Para cada função de imagem, clique em **[!UICONTROL Choose File]**, localize a imagem em seu computador e carregue o arquivo.

   Você pode usar a mesma imagem para todas as três funções ou pode fazer upload de uma imagem de espaço reservado diferente para cada função.

1. Quando terminar, clique em **[!UICONTROL Save]**.

Para obter informações sobre funções de imagem e tamanhos recomendados, consulte [Carregar uma imagem](product-image.md#upload-an-image).
