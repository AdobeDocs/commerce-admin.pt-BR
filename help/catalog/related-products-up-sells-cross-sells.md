---
title: Configurações do produto - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]
description: Para um produto, a variável [!UICONTROL Related Products, Up-Sells, and Cross-Sells] as configurações definem blocos promocionais simples na página do produto que destacam uma seleção de produtos adicionais.
exl-id: 5bd65fad-4e55-40db-8702-10c366261565
feature: Catalog Management, Products, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Configurações do produto - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]

Use o _[!UICONTROL Related Products, Up-Sells, and Cross-Sells]_para configurar blocos promocionais simples que apresentam uma seleção de produtos adicionais que podem ser de interesse do cliente. Para obter mais informações, consulte [Relacionamentos de produto](../merchandising-promotions/product-relationships.md).

![Produtos relacionados, venda adicional e venda cruzada](./assets/product-related-up-sell-cross-sell.png){width="600" zoomable="yes"}

Cada bloco consiste em uma lista de produtos que pertencem a uma opção específica.

| Campo | Descrição |
|--- |--- |
| [!UICONTROL ID] | Um identificador numérico exclusivo que é atribuído à entidade do produto. |
| [!UICONTROL Thumbnail] | Imagem em miniatura do produto. |
| [!UICONTROL Name] | O nome do produto. |
| [!UICONTROL Status] | Indica o status do produto. Opções: `Enabled` / `Disabled`. Os produtos desativados não são exibidos nos blocos do front-end. |
| [!UICONTROL Attribute Set] | O nome do conjunto de atributos usado como modelo para o produto. |
| [!UICONTROL SKU] | A Unidade de Manutenção de Estoque exclusiva atribuída ao produto. |
| [!UICONTROL Price] | O preço unitário do produto. |
| [!UICONTROL Action] | Opções: `Remove`. Remove um produto do bloco. |

{style="table-layout:auto"}

>[!TIP]
>
>![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) **Recommendations de produto desenvolvido pela Adobe Sensei** O simplifica o processo de definição de relacionamentos de produtos usando inteligência artificial e algoritmos de aprendizado de máquina do para executar uma análise profunda dos dados agregados do visitante. Esses dados, quando combinados com seu catálogo do Adobe Commerce, resultam em experiências altamente envolventes, relevantes e personalizadas para o comprador.
><br/>
>Para obter mais informações sobre como usar essa extensão desenvolvida para o Adobe como uma alternativa às recomendações de produto e vendas adicionais configuradas manualmente, consulte o _[Guia do produto Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)_.

## Produtos relacionados

Os produtos relacionados devem ser comprados além do item que o cliente está visualizando. O cliente pode colocar o item no carrinho de compras simplesmente clicando na caixa de seleção. A colocação da variável _Produtos relacionados_ O bloco varia de acordo com o tema e o layout da página definidos. No exemplo abaixo, a variável _Produtos relacionados_ é exibido na parte inferior do _Exibição do produto_ página. Com um layout de duas colunas, a variável _Produtos relacionados_ normalmente aparece na barra lateral direita.

![Produtos relacionados](./assets/storefront-product-related-products.png){width="600" zoomable="yes"}

Para configurar produtos relacionados:

1. Abra o produto no modo de edição.

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** seção.

1. Clique em **[!UICONTROL Add Related Products]**.

1. Use o [controles de filtro](../getting-started/admin-grid-controls.md) para encontrar os produtos desejados.

1. Na lista, marque a caixa de seleção de qualquer produto que deseja incluir como produto relacionado.

   ![Produtos relacionados](./assets/products-related-add.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Add Selected Products]**.

## Vendas adicionais

Os produtos de venda adicional são itens que o cliente pode preferir, em vez do produto considerado no momento. Um item oferecido como uma venda adicional pode ter uma qualidade mais alta, ser mais popular ou ter uma margem de lucro melhor. Os produtos de venda adicional aparecem na página do produto sob um cabeçalho, como _Você também pode estar interessado nos seguintes produtos_.

![Venda Suplementar](./assets/storefront-product-upsell.png){width="600" zoomable="yes"}

Para selecionar produtos de venda adicional:

1. Abra o produto no modo de edição.

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** seção.

1. Clique em **[!UICONTROL Add Up-Sell Products]**.

1. Use o [controles de filtro](../getting-started/admin-grid-controls.md) para encontrar os produtos desejados.

1. Na lista, marque a caixa de seleção de qualquer produto que deseja apresentar como um produto de venda adicional.

   ![Produtos de venda adicional](./assets/product-up-sell-add.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Add Selected Products]**.

## Vendas cruzadas

Os itens de venda cruzada são semelhantes às compras por impulso posicionadas ao lado da caixa registradora na linha de check-out. Os produtos oferecidos como venda cruzada aparecem na página do carrinho de compras, antes que o cliente inicie o processo de finalização.

>[!NOTE]
>
>Para mostrar ou ocultar itens de venda cruzada por exibição de loja, consulte a [Check-out > Carrinho de compras](../configuration-reference/sales/checkout.md) chamada de opção _[!UICONTROL Show Cross-sell Items]_no carrinho de compras. Talvez você queira ocultar as vendas cruzadas durante vendas específicas ou para testes A/B em uma exibição de loja.

![Vendas cruzadas no carrinho de compras](./assets/storefront-cart-cross-sells.png){width="600" zoomable="yes"}

**_Para selecionar produtos de venda cruzada:_**

1. Abra o produto no modo de edição.

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** seção.

1. Clique em **[!UICONTROL Add Cross-Sell Products]**.

1. Use o [controles de filtro](../getting-started/admin-grid-controls.md) para encontrar os produtos desejados.

1. Na lista, marque a caixa de seleção de qualquer produto que deseja incluir como produto de venda cruzada.

   ![Venda cruzada de produtos](./assets/product-cross-sell-add.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Add Selected Products]**.
