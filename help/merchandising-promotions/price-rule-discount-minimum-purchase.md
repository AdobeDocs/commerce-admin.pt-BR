---
title: Exemplo de regra de preço do carrinho - desconto com preço mínimo do produto
description: Revise um exemplo de uso de uma regra de preço do carrinho para oferecer um desconto com um preço mínimo do produto.
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 1a784e894e02090cfa3bc9edc47149b35d935e8e
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Exemplo de regra de preço do carrinho - desconto com preço mínimo do produto

As regras de preço do carrinho podem ser usadas para oferecer um desconto percentual com base em um preço mínimo do produto no carrinho. No exemplo a seguir, um desconto de 10% é aplicado a todos os produtos em todo o carrinho quando pelo menos um produto com um preço superior a US$ 30,00 de uma categoria especificada é adicionado ao carrinho. O formato do desconto é o seguinte:

X% de desconto no carrinho inteiro quando pelo menos 1 produto é da categoria Y e seu preço é superior a US$ Z.

## Etapa 1. Criar uma regra de carrinho

Siga as [instruções](price-rules-cart.md) básicas para criar uma regra de carrinho.

## Etapa 2. Definir as condições

1. Role para baixo e expanda ![Seletor de expansão](../assets/icon-display-expand.png) na seção **[!UICONTROL Conditions]**.

1. Clique em _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) e escolha **[!UICONTROL Product Attribute Combination]**.

   ![Condição de regra de preço do carrinho - combinação de atributo de produto](./assets/condition1.png){width="500" zoomable="yes"}

1. Clique em _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) no início da próxima linha e, na lista abaixo de **[!UICONTROL Product Attribute]**, escolha **[!UICONTROL Category]**.

   - Clique no link (**...**) _mais_ para exibir opções adicionais.

     ![Condição de regra de preço do carrinho - opções de categoria](./assets/condition3.png){width="600" zoomable="yes"}

   - Clique no ícone _Seletor_ (![Ícone de Lista](../assets/icon-list-chooser.png)) para ver as categorias disponíveis. Na árvore de categorias, marque a caixa de seleção de cada categoria que você deseja incluir. Clique no ícone de verificação para aceitar as seleções de categoria.

     ![Condição de regra de preço do carrinho - categoria](./assets/condition4.png){width="600" zoomable="yes"}

1. Clique em _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) no início da próxima linha e faça o seguinte:

   - Na lista abaixo de **[!UICONTROL Cart Item Attribute]**, escolha **[!UICONTROL Price in cart]**.

     ![Condição de regra de preço do carrinho - atributo de item do carrinho](./assets/condition5.png){width="500"}

   - Clique em **é** e escolha `equals or greater than`.

   - Clique em **...** e insira o valor que o Preço no Carrinho deve ser para atender à condição. Por exemplo, digite `30`.

     ![Condição de regra de preço do carrinho - preço no carrinho](./assets/condition6.png){width="500"}

1. Clique em **[!UICONTROL Save and Continue Edit]**.

## Etapa 3. Definir as ações

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Actions]** e faça o seguinte:

   ![Ações de regra de preço do carrinho](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - Defina **[!UICONTROL Apply]** como `Percent of product price discount`.

   - Insira o **[!UICONTROL Discount Amount]**. Por exemplo, insira `10` para um desconto de 10%.

   - Para evitar que promoções adicionais sejam aplicadas à compra, defina **[!UICONTROL Discard subsequent rules]** como `Yes`.

1. Clique em **[!UICONTROL Save and Continue Edit]** e conclua a regra conforme necessário.

## Etapa 4. Preencha os rótulos

Conclua a [Etapa 4](price-rules-cart.md) das instruções de regra de preço do carrinho para inserir rótulos que apareçam durante o check-out.

## Etapa 5: salvar e testar a regra

{{new-price-rule}}

1. Quando a regra estiver concluída, clique em **[!UICONTROL Save Rule]**.
1. Teste a regra para verificar se ela funciona corretamente.
