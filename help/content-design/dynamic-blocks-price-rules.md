---
title: Blocos dinâmicos em regras de preço
description: Associar um bloco dinâmico a uma regra de preço promocional.
exl-id: e1564df2-1c06-4d11-a32d-6f5c0be974e3
feature: Page Content, Price Rules
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Blocos dinâmicos em regras de preço

{{ee-feature}}

Qualquer [bloco dinâmico](dynamic-blocks.md) que você criar poderá ser associado a uma promoção. Para fazer a associação, primeiro você deve criar o bloco dinâmico e a [regra de preço do catálogo](../merchandising-promotions/price-rules-catalog.md) ou a [regra de preço do carrinho](../merchandising-promotions/price-rules-cart.md). A associação pode ser feita ao trabalhar em uma regra de preço ou ao trabalhar em um bloco dinâmico.

>[!IMPORTANT]
>
>Após criar essa associação, o bloco dinâmico é exibido **somente** quando a regra é acionada. Se a promoção for direcionada para o segmento A, o bloco será exibido para o segmento A. Se a promoção não estiver ativa, o bloco não será exibido.

## Associar um bloco dinâmico a uma regra de preço

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_&#x200B;e escolha uma das seguintes opções:

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. Na grade, localize a regra que deseja associar ao bloco dinâmico e abra no modo de edição.

1. Role para baixo e expanda ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Related Dynamic Blocks]**.

1. Na primeira coluna, defina o filtro como `Any` e clique em **[!UICONTROL Reset Filter]**.

   A grade agora lista todos os blocos dinâmicos disponíveis.

1. Marque a caixa de seleção de cada bloco dinâmico que você deseja associar à regra.

   ![Adicionando blocos dinâmicos selecionados](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Associar uma regra de preço a um bloco dinâmico

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. Encontre o bloco dinâmico na grade e abra no modo de edição.

1. Role para baixo e expanda **[!UICONTROL Related Promotions]**.

   Todas as regras de preços atualmente associadas aparecem na grade.

1. Adicione uma nova regra associada ou remova uma associação atual.

   - Para associar uma promoção de carrinho de compras, clique em **[!UICONTROL Add Cart Price Rules]**.

   - Para associar uma promoção relacionada ao produto, clique em **[!UICONTROL Add Catalog Price Rules]**.

1. Na grade, marque a caixa de seleção de cada regra que deseja associar ao bloco dinâmico.

1. Clique em **[!UICONTROL Add Selected]**.

   ![Adicionando regras de preço selecionadas a um bloco dinâmico](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.
