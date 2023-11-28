---
title: Regra de preço de catálogo com vários SKUs
description: Saiba como aplicar uma única regra de preço de catálogo a várias SKUs.
exl-id: 99023460-0501-45cd-8990-5f2b9ed7b4a2
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Regra de preço de catálogo com vários SKUs

Uma única regra de preço de catálogo pode ser aplicada a vários SKUs, o que permite criar várias promoções com base em um produto, marca ou categoria. Ao criar essa regra, você deseja definir condições que correspondam aos SKUs selecionados. Ao criar a regra, você pode navegar facilmente e selecionar SKUs na grade.

## Etapa 1. Verificar propriedades de vitrine do atributo de produto

Antes de começar, verifique se [Propriedades da vitrine](../catalog/attribute-product-create.md#step-4-describe-the-storefront-properties) do `sku` atributo estão definidos como `Use in Promo Rules`.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. No filtro de pesquisa, na parte superior da guia _[!UICONTROL Attribute Code]_coluna, insira `sku` e clique em **[!UICONTROL Search]**.

1. Clique para abrir a `sku` atributo no modo de edição.

1. No painel esquerdo, clique em **[!UICONTROL Storefront Properties]** e certifique-se de que **[!UICONTROL Use for Promo Rule Conditions]** está definida como `Yes`.

1. Se você alterou o valor da propriedade, clique em **[!UICONTROL Save Attribute]**.

## Etapa 2. Aplicar uma regra de preço a vários SKUs

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

1. Siga um destes procedimentos:

   - Siga as instruções para criar um [regra de preço de catálogo](price-rules-catalog.md).
   - Abra uma regra de preço de catálogo existente.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Conditions]** e faça o seguinte:

   - Na primeira linha, defina o primeiro parâmetro para `ANY`.

     ![Condição da regra de preço de catálogo - QUALQUER](./assets/multiple-skus-condition1.png){width="600" zoomable="yes"}

   - Clique em _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) no início da próxima linha e na lista em **[!UICONTROL Product Attribute]**, clique em `SKU`.

     ![Condição da regra de preço de catálogo - SKU é um de](./assets/multiple-skus-condition1a.png){width="600" zoomable="yes"}

   - Para a comparação, você tem opções. Se quiser localizar pelo menos um item de uma lista de SKUs, `select is one of`. Se quiser localizar um grupo de SKUs aos quais todos devem ser aplicados, selecione `is`. Recomendamos selecionar `is one of`.

     ![Condição da regra de preço de catálogo - SKU é um de](./assets/multiple-skus-condition1b.png){width="600" zoomable="yes"}

   - Para concluir a condição, clique no sinal de mais (**..**) e clique no link _Seletor_ (![Ícone de Lista](../assets/icon-list-chooser.png)) para obter a lista de produtos disponíveis.

     ![Condição de regra de preço de catálogo - várias SKUs](./assets/multiple-skus-condition2b.png){width="600" zoomable="yes"}

   - Procure, filtre ou pesquise para encontrar os SKUs que deseja adicionar. Na lista, marque a caixa de seleção de cada produto a ser incluído.

   - Clique em **[!UICONTROL Save and Apply]** para adicionar as SKUs à condição.

     ![Condição de regra de preço de catálogo - várias SKUs](./assets/multiple-skus-condition2.png){width="600" zoomable="yes"}

1. Complete a regra, incluindo qualquer [Ações](price-rules-catalog.md) a tomar quando as condições estiverem reunidas.

1. Quando a regra for concluída, clique em **[!UICONTROL Save]**.

{{new-price-rule}}
