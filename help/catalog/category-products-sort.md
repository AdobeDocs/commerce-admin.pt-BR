---
title: Classificar produtos da categoria
description: Saiba como definir o posicionamento de produtos em uma categoria manualmente ou aplicando uma ordem de classificação predefinida.
exl-id: 09c66a5d-57d4-4e78-a8d8-e3047c1bd35a
feature: Catalog Management, Categories, Products
TQID: https://experienceleague.adobe.com/Co2sHVc4YaLqjVrc-Varq9-ssecBB-C2mL3MTAPuQbU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 424
ht-degree: 0%

---

# Classificar produtos da categoria

{{ee-feature}}

A posição dos produtos em uma categoria pode ser especificada manualmente arrastando e soltando produtos na posição ou aplicando uma ordem de classificação predefinida. Por padrão, os produtos podem ser classificados por nível de estoque, idade, cor, nome, SKU e preço. A classificação automática substitui a ordem de classificação atual e redefine as posições de arrastar e soltar definidas manualmente. A ordem de classificação das cores e o nível mínimo de estoque que pode ser necessário para os produtos a serem incluídos na lista são definidos na configuração do [Visual Merchandiser](../configuration-reference/catalog/visual-merchandiser.md).

Você pode configurar as opções de categoria separadamente para cada [exibição da loja](../stores-purchase/stores.md#add-stores) para determinar a seleção de produtos, sua posição relativa na lista e os atributos disponíveis para regras de categoria. Entretanto, há uma única ordem de classificação **_global_** e uma posição de produto no catálogo e elas são compartilhadas em todas as [exibições de loja](../stores-purchase/store-views.md), lojas e sites.

## Etapa 1: definir o escopo da configuração

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Se necessário, escolha a **[!UICONTROL Store View]** à qual as configurações se aplicam.

   Para uma instalação com vários armazenamentos, a configuração _[!UICONTROL Store View]_&#x200B;aplica a ordem de classificação a todas as exibições disponíveis no armazenamento.

1. Na árvore de categorias à esquerda, escolha a categoria que deseja editar.

   ![Árvore de categorias](./assets/category-selected.png){width="700" zoomable="yes"}

## Etapa 2: Classificar os produtos

>[!NOTE]
>
>Ao classificar uma categoria por um atributo de produto, os produtos com os mesmos valores de atributo também são classificados por seu _[!UICONTROL Product ID]_&#x200B;na ordem crescente.

Na seção _[!UICONTROL Products in Category]_, clique no ícone de blocos ( ![Exibir blocos](../assets/icon-view-tiles.png) ) para mostrar os blocos de produtos em uma grade. Use o método manual ou automático para classificar os produtos.

![Blocos de produtos](./assets/category-products-tiles.png){width="600" zoomable="yes"}

### Método 1: classificação manual

1. Defina **[!UICONTROL Sort Order]** de acordo com sua preferência.

   ![Ordem de classificação](./assets/category-edit-sort-order.png){width="600" zoomable="yes"}

1. Para aplicar a nova ordem de classificação, clique em **[!UICONTROL Sort]**.

1. Para salvar a ordem de classificação, clique em **[!UICONTROL Save Category]**.

1. Quando solicitado, atualize todos os indexadores inválidos.

### Método 2: classificação automática

1. Defina **[!UICONTROL Match products by rule]** (![Alternar sim](../assets/toggle-yes.png)) para `Yes`.


1. Defina **[!UICONTROL Automatic Sorting]** de acordo com sua preferência.

1. Para criar uma regra de categoria, siga as instruções na próxima etapa.

## Etapa 3: criar uma regra de categoria

1. Defina **[!UICONTROL Match products by rule]** (![Alternar sim](../assets/toggle-yes.png)) para `Yes`.

1. Clique em **[!UICONTROL Add Condition]**.

1. Escolha o **[!UICONTROL Attribute]** que é a base da condição.

1. Defina **[!UICONTROL Operator]** como um dos seguintes:

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Digite o **[!UICONTROL Value]** apropriado.

   ![Condição de categoria](./assets/category-rule-create.png){width="600" zoomable="yes"}

1. Para adicionar outra condição, clique em **[!UICONTROL Add Condition]** e repita o processo.

## Etapa 4: salvar, atualizar e verificar

1. Quando terminar, clique em **[!UICONTROL Save Category]**.

1. Quando solicitado a atualizar o cache, clique em **[!UICONTROL Cache Management]** e atualize cada cache inválido.

1. Na loja, verifique se a seleção do produto, a classificação e as regras de categoria funcionam corretamente.

   Se precisar fazer ajustes, altere as configurações e tente novamente.
