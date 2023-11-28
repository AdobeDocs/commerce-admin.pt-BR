---
title: Adicionar atributos a um produto
description: Saiba como adicionar atributos aos produtos em seu catálogo.
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Adicionar atributos a um produto

Embora os atributos sejam gerenciados principalmente a partir do [Lojas](../stores-purchase/stores-menu.md) , também é possível adicionar novos atributos _em tempo real_ ao trabalhar em um produto. Você pode escolher na lista de atributos existentes ou criar um atributo. O novo atributo é adicionado à variável [conjunto de atributos](../catalog/attribute-sets.md) em que o produto se baseia.

## Etapa 1: Adicionar um atributo

1. Abra o produto no modo de edição.

1. No canto superior direito, clique em **[!UICONTROL Add Attribute]**.

   ![Novo produto com conjunto de atributos padrão](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. Para adicionar um atributo existente ao produto, use o [controles de filtro](../getting-started/admin-grid-controls.md) para localizar o atributo na grade e faça o seguinte:

   - Marque a caixa de seleção na primeira coluna de cada atributo a ser adicionado.

   - Clique em **[!UICONTROL Add Selected]**.

   ![Selecionar um atributo](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. Para definir um novo atributo, clique em **[!UICONTROL Create New Attribute]** e conclua os itens na Etapa 2.

## Etapa 2: Descrever as propriedades básicas do atributo

![Propriedades do atributo](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. Em _[!UICONTROL Attribute Properties]_, insira um **[!UICONTROL Attribute Label]**para identificar o atributo.

1. Definir **[!UICONTROL Catalog Input Type for Store Owner]** ao tipo de [controle de entrada](attributes-input-types.md) a ser usado para entrada de dados.

   Se o atributo for usado para um [produto configurável](product-create-configurable.md), escolha `Dropdown`. Em seguida, defina **[!UICONTROL Required]** para `Yes`.

1. Para `Dropdown` e `Multiple Select` tipos de entrada, faça o seguinte:

   - Em **[!UICONTROL Values]**, clique em **[!UICONTROL Add Value]**.

   - Insira o primeiro valor que você deseja que apareça na lista.

     Você pode inserir um valor para o Administrador e uma tradução do valor para cada exibição de loja. Se você tiver apenas uma visualização de loja, poderá inserir apenas o valor Admin e ele também será usado para a loja.

   - Clique em **[!UICONTROL Add Value]** e repita a etapa anterior para cada opção que desejar incluir na lista.

   - Selecionar **[!UICONTROL Is Default]** para usar a opção como valor padrão.

   ![Valores](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. Se você quiser que o cliente escolha uma opção antes que o produto possa ser comprado, defina **[!UICONTROL Required]** para `Yes`.

## Etapa 3: descrever as propriedades avançadas (opcional)

![Propriedades Avançadas de Atributo](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. Insira um único **[!UICONTROL Attribute Code]** em caracteres minúsculos e sem espaços.

1. Definir **[!UICONTROL Scope]** para indicar onde na hierarquia de armazenamento o atributo pode ser usado.

   Se o atributo for usado para um [produto configurável](product-create-configurable.md), escolha `Global`.

1. Se este atributo se aplicar somente a este produto, defina **[!UICONTROL Unique Value]** para `Yes`.

1. Para executar um teste de validade de quaisquer dados inseridos em um campo de texto, defina **[!UICONTROL Input Validation for Store Owner]** ao tipo de dados que o campo deve conter.

   Este campo não está disponível para tipos de entrada com valores selecionados. A validação de entrada pode ser usada para qualquer um dos seguintes:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Validação de entrada](./assets/product-attribute-input-validation.png){width="500"}

1. Se quiser incluir o atributo como uma coluna na grade Produtos, defina **[!UICONTROL Add to Column Options]** para `Yes`.

1. Se quiser filtrar a variável _[!UICONTROL Products]_grade por esta coluna, defina **[!UICONTROL Use in Filter Options]**para `Yes`.

## Etapa 4: insira o rótulo do campo

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Manage titles]** seção.

1. Insira um **[!UICONTROL Title]** para ser usado como rótulo para o campo.

   Se a loja estiver disponível em diferentes idiomas, você poderá inserir um título traduzido para cada exibição.

   ![Gerenciar títulos](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Etapa 5: descrever as propriedades da loja

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Storefront Properties]** seção.

   ![Propriedades da vitrine](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. Para disponibilizar o atributo para pesquisa, defina **[!UICONTROL Use in Search]** para `Yes`.

1. Para incluir o atributo na Comparação de Produtos, defina **[!UICONTROL Comparable on Storefront]** para `Yes`.

1. Para incluir lista suspensa, seleção múltipla ou atributos de preço na navegação em camadas, defina **[!UICONTROL Use in Search Results Layered Navigation]** a um dos seguintes:

   - `Filterable (with results)` - A navegação em camadas inclui apenas os filtros para os quais os produtos correspondentes podem ser encontrados. Qualquer valor de atributo que já se aplique a todos os produtos mostrados na lista não aparece como um filtro disponível. Valores de atributo com uma contagem de zero (0) correspondências de produto também são omitidos da lista de filtros disponíveis.<br/><br/>A lista de produtos filtrada inclui apenas os produtos que correspondem ao filtro. A lista de produtos é atualizada somente se os filtros selecionados alterarem o que é mostrado.

   - `Filterable (no results)` - A navegação em camadas inclui filtros para todos os valores de atributo disponíveis e suas contagens de produto, incluindo os produtos com zero (0) correspondências de produto. Se o valor do atributo for uma amostra, ele será exibido como um filtro, mas riscado.

1. Para usar na navegação em camadas nas páginas de resultados da pesquisa, defina **[!UICONTROL Use in Search Results Navigation]** para `Yes` e insira um número no campo **[!UICONTROL Position]** campo.

   O número da posição indica a posição relativa do atributo no bloco de navegação em camadas.

1. Para usar o atributo em regras de preço, defina **[!UICONTROL Use for Promo Rule Conditions]** para `Yes`.

1. Para permitir que o texto seja formatado com HTML, defina **[!UICONTROL Allow HTML Tags on Storefront]** para `Yes`.

   Essa configuração disponibiliza o editor WYSIWYG ao editar o campo.

1. Para incluir o atributo na página do produto, defina **[!UICONTROL Visible on Catalog Pages on Storefront]** para `Yes`.

1. Complete as configurações a seguir, conforme suportado pelo seu tema:

   - Para incluir o atributo em listagens de produtos, defina **[!UICONTROL Used in Product Listing]** para `Yes`.

   - Para usar o atributo como parâmetro de classificação para listagens de produtos, defina **[!UICONTROL Used for Sorting in Product Listing]** para `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Attribute]**.
