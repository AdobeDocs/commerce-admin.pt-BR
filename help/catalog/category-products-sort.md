---
title: Classificar produtos da categoria
description: Saiba como definir o posicionamento de produtos em uma categoria manualmente ou aplicando uma ordem de classificação predefinida.
exl-id: 09c66a5d-57d4-4e78-a8d8-e3047c1bd35a
feature: Catalog Management, Categories, Products
source-git-commit: 14c3eb7d54776382bfa196efdac446d42c8dc940
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Classificar produtos da categoria

{{ee-feature}}

A posição dos produtos em uma categoria pode ser especificada manualmente arrastando e soltando produtos na posição ou aplicando uma ordem de classificação predefinida. Por padrão, os produtos podem ser classificados por nível de estoque, idade, cor, nome, SKU e preço. A classificação automática substitui a ordem de classificação atual e redefine as posições de arrastar e soltar definidas manualmente. A ordem de classificação das cores e o nível mínimo de estoque que pode ser necessário para os produtos a serem incluídos na lista são definidos no [Visual Merchandiser](../configuration-reference/catalog/visual-merchandiser.md) configuração.

>[!NOTE]
>
>Nas páginas de categoria, `Out of stock` os produtos são sempre exibidos **_após_** `In Stock` produtos na lista de produtos com todos os tipos de classificação.

É possível configurar as opções de categoria separadamente para cada [exibição de loja](../stores-purchase/stores.md#add-stores) para determinar a seleção de produtos, sua posição relativa na lista e os atributos disponíveis para regras de categoria. No entanto, existe um único **_global_** ordem de classificação e posição do produto no catálogo e são compartilhados entre todos [exibições de loja](../stores-purchase/store-views.md), lojas e sites.

## Etapa 1: definir o escopo da configuração

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Se necessário, escolha o **[!UICONTROL Store View]** onde as configurações se aplicam.

   Para uma instalação de várias lojas, a variável _[!UICONTROL Store View]_essa configuração aplica a ordem de classificação a todas as exibições disponíveis no armazenamento.

1. Na árvore de categorias à esquerda, escolha a categoria que deseja editar.

   ![Árvore de categoria](./assets/category-selected.png){width="700" zoomable="yes"}

## Etapa 2: Classificar os produtos

>[!NOTE]
>
>Ao classificar uma categoria por um atributo de produto, os produtos com os mesmos valores de atributo também são classificados por seus _[!UICONTROL Product ID]_na ordem crescente.

No _[!UICONTROL Products in Category]_clique nos blocos ( ![Exibir blocos](../assets/icon-view-tiles.png) ) para mostrar os blocos gráficos do produto em uma grade. Use o método manual ou automático para classificar os produtos.

![Mosaicos do produto](./assets/category-products-tiles.png){width="600" zoomable="yes"}

### Método 1: classificação manual

1. Definir **[!UICONTROL Sort Order]** de acordo com sua preferência.

   ![Ordem de classificação](./assets/category-edit-sort-order.png){width="600" zoomable="yes"}

1. Para aplicar a nova ordem de classificação, clique em **[!UICONTROL Sort]**.

1. Para salvar a ordem de classificação, clique em **[!UICONTROL Save Category]**.

1. Quando solicitado, atualize todos os indexadores inválidos.

### Método 2: classificação automática

1. Definir **[!UICONTROL Match products by rule]** (![Alternar sim](../assets/toggle-yes.png)) para `Yes`.


1. Definir **[!UICONTROL Automatic Sorting]** de acordo com sua preferência.

1. Para criar uma regra de categoria, siga as instruções na próxima etapa.

## Etapa 3: criar uma regra de categoria

1. Definir **[!UICONTROL Match products by rule]** (![Alternar sim](../assets/toggle-yes.png)) para `Yes`.

1. Clique em **[!UICONTROL Add Condition]**.

1. Escolha o **[!UICONTROL Attribute]** é essa a base da condição.

1. Definir **[!UICONTROL Operator]** a um dos seguintes:

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Insira o apropriado **[!UICONTROL Value]**.

   ![Condição de categoria](./assets/category-rule-create.png){width="600" zoomable="yes"}

1. Para adicionar outra condição, clique em **[!UICONTROL Add Condition]** e repita o processo.

## Etapa 4: salvar, atualizar e verificar

1. Quando terminar, clique em **[!UICONTROL Save Category]**.

1. Quando for solicitado atualizar o cache, clique em **[!UICONTROL Cache Management]** e atualizar cada cache inválido.

1. Na loja, verifique se a seleção do produto, a classificação e as regras de categoria funcionam corretamente.

   Se precisar fazer ajustes, altere as configurações e tente novamente.
