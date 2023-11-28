---
title: Atribuições de produto de categoria
description: Saiba mais sobre como usar o [!UICONTROL Products in Category] configurações para controlar quais produtos estão atualmente atribuídos à categoria.
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# Atribuições de produto de categoria

Para uma categoria, use o _[!UICONTROL Products in Category]_para analisar os produtos atualmente atribuídos à categoria. Os filtros de pesquisa na parte superior de cada coluna são usados para adicionar e remover produtos da categoria. Também é possível usar [regras de categoria](../merchandising-promotions/category-product-rules.md) ( ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce somente) para alterar dinamicamente a seleção do produto quando um conjunto de condições é atendido. Para saber mais, consulte [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md)).

>[!TIP]
>
>Durante a configuração da regra de categoria, os produtos são _classificado_, _correspondente_, _atribuído_, e _não atribuído_ de acordo com esta regra **_somente_** quando esta categoria é salva. Para garantir que um novo produto seja atribuído de acordo com a regra ao adicioná-lo ao catálogo, **deve salvar novamente cada categoria** que é definido para corresponder produtos por regra. Além disso, se qualquer status de estoque de produtos for alterado para `In Stock` ou `Out of Stock` e os produtos da categoria são _classificado_ de acordo com a **Classificação automática** regra, clique em **[!UICONTROL Save Category]**.

![Categoria Produtos](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Nas páginas de categoria, `Out of stock` os produtos são sempre exibidos **_após_** `In Stock` produtos na lista de produtos com todos os tipos de classificação.

>[!NOTE]
>
>A variável _Stock_ exibe a quantidade de produtos comercializáveis para _**escopo de categoria selecionado**_ somente. Quando vários estoques são gerenciados para produtos, você deve alternar entre os escopos correspondentes para exibir outros _Stock_ valores da coluna na _Categoria Produtos_ grade.

## Aplicar uma regra de categoria

{{ee-feature}}

1. Definir **[!UICONTROL Match products by rule]** para `Yes`.

   As opções de classificação e condição automáticas são exibidas.

   ![Para corresponder produtos por regra](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. Defina o **[!UICONTROL Automatic Sorting]** pedido.

   Essa classificação automática baseia-se nas condições atuais.

   - `Stock level` - Mover para cima ou para baixo.
   - `Special price` - Mover para cima ou para baixo.
   - `New Products` - Listar primeiro os produtos mais recentes.
   - `Color` - Classificar alfabeticamente por cor.
   - `Name` - Classifique em ordem crescente ou decrescente por Nome.
   - `SKU` - Classificar em ordem crescente ou decrescente por SKU
   - `Price` - Classifique em ordem crescente ou decrescente por Preço.

1. Clique em **[!UICONTROL Add Condition]** e faça o seguinte:

   - Escolha o **[!UICONTROL Attribute]** é essa a base da condição.
   - Escolha o **[!UICONTROL Operator]** necessário para formar a expressão.
   - Insira o **[!UICONTROL Value]** que deve ser correspondido.

   ![Adicionar condição à regra de categoria](./assets/category-rule-create.png){width="600" zoomable="yes"}

   Repita esse processo para cada atributo a ser usado para descrever as condições a serem atendidas. Por exemplo, para corresponder a produtos que foram criados de 7 a 30 dias atrás, faça o seguinte:

   - Definir **[!UICONTROL Date Created]** para `Less than 30`.
   - Definir **[!UICONTROL Logic]** para `AND`.
   - Definir **[!UICONTROL Date Modified]** para `Greater than 7`.

1. Quando terminar, clique em **[!UICONTROL Save Category]**.

### Opções de página

| Opção | Descrição |
|--- |--- |
| [!UICONTROL Match products by rule] | Determina se a lista de produtos na categoria é gerada dinamicamente por uma regra de categoria. Opções: `Yes` / `No` |
| [!UICONTROL Automatic Sorting] | Aplica automaticamente uma ordem de classificação à lista de produtos da categoria. Opções: <br/>`None`<br/>`Move low stock to top`<br/>`Move low stock to bottom`<br/>`Special price to top`<br/>`Special price to bottom`<br/>`Newest products first`<br/>`Sort by color`<br/>`Name: A - Z`<br/>`Name: Z - A`<br/>`SKU: Ascending`<br/>`SKU: Descending`<br/>`Price: High to Low`<br/>`Price: Low to High` |
| [!UICONTROL Add Condition] | Adiciona outra condição à regra. |

{style="table-layout:auto"}

### Condições da página

| Opção | Descrição |
|--- |--- |
| [!UICONTROL Attribute] | Determina o atributo usado como a base da condição. Opções: <br/>**[!UICONTROL Clone Category ID(s)]**- Clona dinamicamente produtos, sem sua classificação e ordem, de várias categorias com base na ID de categoria.<br/>**[!UICONTROL Color]** - Inclui produtos com base na cor. <br/>**[!UICONTROL Date Created (days ago)]**- Inclui produtos com base no número de dias desde que os produtos foram adicionados ao catálogo.<br/>**[!UICONTROL Date Modified (days ago)]** - Inclui produtos com base no número de dias desde a última modificação dos produtos. <br/>**[!UICONTROL Name]**- Inclui produtos com base no nome do produto.<br/>**[!UICONTROL Price]** - Inclui produtos com base no preço. <br/>**[!UICONTROL Quantity]**- Inclui produtos com base na quantidade em estoque.<br/>** SKU **- Inclui produtos baseados em SKU. |
| [!UICONTROL Operator] | Especifica o operador que é aplicado ao valor do atributo para atender à condição. A menos que um operador seja especificado, `Equal` é usado como padrão. Opções: `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | Especifica o valor que o atributo deve ter para atender à condição. |
| [!UICONTROL Logic] | Usado para definir várias condições e é exibido apenas quando outra condição é adicionada. Opções: `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>A quantidade de um produto configurável com opções filho é calculada combinando todas as quantidades de produtos filho dimensionáveis. Considere um exemplo de um produto configurável _Tanque de fitness de resistência_ com opções de cor roxa, vermelha e amarela e quantidades diferentes de cada uma. Nesse cenário, a quantidade de produto principal é a quantidade de vendas combinada dos produtos secundários de cores roxa, vermelha e amarela.

## Controles


## Controles de página

{{ee-feature}}

| Controle | Descrição |
|----------|--------------|
| ![Exibir como lista](../assets/icon-view-list.png) | Exibir como lista |
| ![Exibir como blocos](../assets/icon-view-tiles.png) | Exibir como mosaico |
| ![Alternar não](../assets/toggle-no.png) | Corresponder por Regra - Não |
| ![Alternar sim](../assets/toggle-yes.png) | Corresponder por Regra - Sim |
| ![Controlador de movimentação](../assets/icon-move.png) | O controle de arrastar e soltar permite que você capture um produto e mova-o para outra posição na página atual da grade. Para saber mais, consulte [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md). |
| ![Controlador de posição](../assets/control-position.png) | Determina a posição do produto na lista. |

{style="table-layout:auto"}

## Controles de página

{{ce-feature}}

| Controle | Descrição |
|----------|--------------|
| ![Caixa de seleção Selecionada](../assets/checkbox-selected.png) | Use a caixa de seleção no cabeçalho da primeira coluna para selecionar todos os produtos ou desmarcar todas as seleções. O controle na primeira linha determina o tipo de pesquisa e pode ser definido para incluir qualquer registro ou incluir apenas os registros que estão atribuídos ou não à categoria. A caixa de seleção na primeira coluna de cada linha identifica produtos a serem adicionados à categoria. Opções: `Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | Os controles de filtro na parte superior de cada coluna podem ser usados para inserir valores específicos que você deseja incluir ou omitir na lista, dependendo da configuração Selecionar tudo. |
| [!UICONTROL Reset Filter] | Limpa todos os filtros de pesquisa. |
| [!UICONTROL Search] | Pesquisa o catálogo com base nos critérios de filtro e exibe o resultado. |

{style="table-layout:auto"}
