---
title: Adicionar atributos a um produto
description: Saiba como adicionar atributos aos produtos em seu catálogo.
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 45d69ccc1a5a6a7b8d072465c19829a76dde826d
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# Adicionar atributos a um produto

Embora os atributos sejam gerenciados principalmente pelo menu [Lojas](../stores-purchase/stores-menu.md), você também pode adicionar novos atributos _imediatamente_ enquanto trabalha em um produto. Você pode escolher na lista de atributos existentes ou criar um atributo. O novo atributo é adicionado ao [conjunto de atributos](../catalog/attribute-sets.md) no qual o produto se baseia.

## Etapa 1: Adicionar um atributo

1. Abra o produto no modo de edição.

1. No canto superior direito, clique em **[!UICONTROL Add Attribute]**.

   ![Novo produto com conjunto de atributos padrão](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. Para adicionar um atributo existente ao produto, use os [controles de filtro](../getting-started/admin-grid-controls.md) para localizar o atributo na grade e faça o seguinte:

   - Marque a caixa de seleção na primeira coluna de cada atributo a ser adicionado.

   - Clique em **[!UICONTROL Add Selected]**.

   ![Selecione um atributo](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. Para definir um novo atributo, clique em **[!UICONTROL Create New Attribute]** e conclua os itens da Etapa 2.

## Etapa 2: Descrever as propriedades básicas do atributo

![Propriedades do atributo](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. Em _[!UICONTROL Attribute Properties]_, insira um **[!UICONTROL Attribute Label]**para identificar o atributo.

1. Defina **[!UICONTROL Catalog Input Type for Store Owner]** como o tipo de [controle de entrada](attributes-input-types.md) a ser usado para entrada de dados.

   Se o atributo for usado para um [produto configurável](product-create-configurable.md), escolha `Dropdown`. Em seguida, defina **[!UICONTROL Required]** como `Yes`.

1. Para os tipos de entrada `Dropdown` e `Multiple Select`, faça o seguinte:

   - Em **[!UICONTROL Values]**, clique em **[!UICONTROL Add Value]**.

   - Insira o primeiro valor que você deseja que apareça na lista.

     Você pode inserir um valor para o Administrador e uma tradução do valor para cada exibição de loja. Se você tiver apenas uma visualização de loja, poderá inserir apenas o valor Admin e ele também será usado para a loja.

   - Clique em **[!UICONTROL Add Value]** e repita a etapa anterior para cada opção que deseja incluir na lista.

   - Selecione **[!UICONTROL Is Default]** para usar a opção como valor padrão.

   ![Valores](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. Se você quiser que o cliente escolha uma opção antes da compra do produto, defina **[!UICONTROL Required]** como `Yes`.

## Etapa 3: descrever as propriedades avançadas (opcional)

![Propriedades Avançadas de Atributo](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. Insira um **[!UICONTROL Attribute Code]** exclusivo em caracteres minúsculos e sem espaços.

1. Defina **[!UICONTROL Scope]** para indicar onde na hierarquia de armazenamento o atributo pode ser usado.

   Se o atributo for usado para um [produto configurável](product-create-configurable.md), escolha `Global`.

1. Se este atributo se aplicar somente a este produto, defina **[!UICONTROL Unique Value]** como `Yes`.

1. Para executar um teste de validade de quaisquer dados inseridos em um campo de texto, defina **[!UICONTROL Input Validation for Store Owner]** como o tipo de dados que o campo deve conter.

   Este campo não está disponível para tipos de entrada com valores selecionados. A validação de entrada pode ser usada para qualquer um dos seguintes:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Validação de entrada](./assets/product-attribute-input-validation.png){width="500"}

1. Se quiser incluir o atributo como uma coluna na grade Produtos, defina **[!UICONTROL Add to Column Options]** como `Yes`.

1. Se quiser filtrar a grade _[!UICONTROL Products]_por esta coluna, defina **[!UICONTROL Use in Filter Options]**como `Yes`.

## Etapa 4: insira o rótulo do campo

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Manage titles]**.

1. Digite um **[!UICONTROL Title]** para ser usado como rótulo para o campo.

   Se a loja estiver disponível em diferentes idiomas, você poderá inserir um título traduzido para cada exibição.

   ![Gerenciar Títulos](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   > Se você planeja usar esse atributo como uma faceta no Live Search, você deve especificar um rótulo específico da loja. Sem ele, o nome do atributo pode não ser exibido corretamente na página de configuração da faceta. Para atualizar a configuração, edite manualmente o rótulo usando a [opção de edição na lista facetada do Live Search](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/facets/facets-add#step-2-edit-facet-properties-optional) no _Guia do Live Search_.

## Etapa 5: descrever as propriedades da loja

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Storefront Properties]**.

   ![Propriedades da vitrine](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. Para disponibilizar o atributo para pesquisa, defina **[!UICONTROL Use in Search]** como `Yes`.

1. Para incluir o atributo na Comparação de Produtos, defina **[!UICONTROL Comparable on Storefront]** como `Yes`.

1. Para incluir lista suspensa, seleção múltipla ou atributos de preço na navegação em camadas, defina **[!UICONTROL Use in Search Results Layered Navigation]** como um dos seguintes:

   - `Filterable (with results)` - A navegação em camadas inclui apenas os filtros para os quais os produtos correspondentes podem ser encontrados. Qualquer valor de atributo que já se aplique a todos os produtos mostrados na lista não aparece como um filtro disponível. Valores de atributo com uma contagem de zero (0) correspondências de produto também são omitidos da lista de filtros disponíveis.<br/><br/>A lista de produtos filtrada inclui somente os produtos que correspondem ao filtro. A lista de produtos é atualizada somente se os filtros selecionados alterarem o que é mostrado.

   - `Filterable (no results)` - A navegação em camadas inclui filtros para todos os valores de atributos disponíveis e suas contagens de produtos, incluindo os produtos com zero (0) correspondências de produto. Se o valor do atributo for uma amostra, ele será exibido como um filtro, mas riscado.

   >[!NOTE]
   >
   >Quando a configuração _[!UICONTROL Use in Search]_está definida como `No`, a configuração_[!UICONTROL Use in Search Results Layered Navigation]_ não é exibida e o atributo de produto não é usado na pesquisa com nenhum valor de configuração [!UICONTROL Use in Layered Navigation].

1. Para usar o atributo na navegação em camadas nas páginas de resultados da pesquisa, defina **[!UICONTROL Use in Search Results Layered Navigation]** como `Yes` e insira um número no campo **[!UICONTROL Position]**.

   O número da posição indica a posição relativa do atributo no bloco de navegação em camadas.

   >[!NOTE]
   >
   >O campo _[!UICONTROL Position]_está esmaecido por padrão e você deve salvar o atributo antes de modificar essa configuração.

1. Para usar o atributo em regras de preço, defina **[!UICONTROL Use for Promo Rule Conditions]** como `Yes`.

1. Para permitir que o texto seja formatado com HTML, defina **[!UICONTROL Allow HTML Tags on Storefront]** como `Yes`.

   Essa configuração disponibiliza o editor do WYSIWYG ao editar o campo.

1. Para incluir o atributo na página do produto, defina **[!UICONTROL Visible on Catalog Pages on Storefront]** como `Yes`.

1. Complete as configurações a seguir, conforme suportado pelo seu tema:

   - Para incluir o atributo nas listagens de produtos, defina **[!UICONTROL Used in Product Listing]** como `Yes`.

   - Para usar o atributo como parâmetro de classificação para as listagens de produtos, defina **[!UICONTROL Used for Sorting in Product Listing]** como `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Attribute]**.
