---
title: Produto configurável
description: Saiba como criar um produto configurável que forneça variações para seleção aos compradores.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '2416'
ht-degree: 0%

---

# Produto configurável

Um produto configurável se parece com um único produto com uma lista suspensa de cada variação. Cada item da lista é na verdade um produto simples separado com uma SKU exclusiva, o que permite rastrear o inventário para cada variação de produto. Você pode obter um efeito semelhante usando um produto simples com opções personalizadas, mas sem a capacidade de rastrear o inventário para cada variação.

As instruções a seguir demonstram o processo de criação de um produto configurável usando um [modelo do produto](attribute-sets.md), campos obrigatórios e configurações básicas. Cada campo obrigatório está marcado com um asterisco vermelho (`*`). Quando terminar as noções básicas, você poderá concluir as outras configurações do produto conforme necessário.

![Produto configurável](./assets/product-configurable.png){width="700" zoomable="yes"}

## Parte 1: Criação de um produto configurável

Embora um produto configurável use mais SKUs e possa, inicialmente, levar um pouco mais para ser configurado, ele pode economizar seu tempo no final. Se você planeja expandir seu negócio, o tipo de produto configurável é uma boa escolha para produtos com várias opções.

Antes de começar, prepare um [conjunto de atributos](attribute-sets.md) que inclui um atributo definido como um dos tipos de entrada permitidos para cada variação de produto. Por exemplo, o conjunto de atributos pode incluir atributos suspensos para cor e tamanho.

As propriedades de cada atributo usado para uma variação de produto configurável devem ter as seguintes configurações:

### Requisitos do atributo de variação de produto

| Propriedade | Configuração |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | O tipo de entrada de qualquer atributo usado para uma variação de produto deve ser um dos seguintes: `Dropdown`, `Visual Swatch`ou `Text Swatch`. |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

### Etapa 1: Escolher o tipo de produto

1. No _Admin_ barra lateral, vá para  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. No _[!UICONTROL Add Product]_( ![Seta de menu](../assets/icon-menu-down-arrow-red.png){width="25"} ) no canto superior direito, escolha **[!UICONTROL Configurable Product]**.

   ![Adicionar produto configurável](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### Etapa 2: Escolher o conjunto de atributos

A variável [conjunto de atributos](attribute-sets.md) determina a seleção de campos usados no produto. O conjunto de atributos usado no exemplo a seguir tem atributos para cor e tamanho. O nome do conjunto de atributos é indicado na parte superior da página e é inicialmente definido como `Default`.

1. Para escolher o conjunto de atributos do produto, clique no campo na parte superior da página e siga um destes procedimentos:

   - Para **[!UICONTROL Search]**, insira o nome do conjunto de atributos.
   - Na lista, escolha o conjunto de atributos que deseja usar.

   O formulário é atualizado para refletir a alteração.

1. Se quiser adicionar outro atributo ao conjunto de atributos, clique em **[!UICONTROL Add Attribute]** e siga as instruções em [Adicionar um atributo](product-attributes-add.md).

   ![Escolher modelo](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### Etapa 3: concluir as configurações necessárias

1. Insira o produto **[!UICONTROL Product Name]**.

1. Aceitar o padrão **[!UICONTROL SKU]** que se baseia no nome do produto ou insira outro.

1. Insira o produto **[!UICONTROL Price]**.

1. Como o produto ainda não está pronto para publicação, defina **[!UICONTROL Enable Product]** para `No`.

1. click **[!UICONTROL Save]** e continue.

   Quando o produto for salvo, a variável [Exibição da loja](introduction.md#product-scope) seletor aparece no canto superior esquerdo.

1. Escolha o **[!UICONTROL Store View]** onde o produto deve estar disponível.

   ![Escolher a exibição da loja](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Etapa 4: concluir as configurações básicas

1. Definir **[!UICONTROL Tax Class]** a um dos seguintes:

   - `None`
   - `Taxable Goods`

1. A variável **[!UICONTROL Quantity]** é determinado pelas variações de produto, portanto, você pode deixá-lo em branco.

1. Deixe a **[!UICONTROL Stock Status]** como definido.

   O status do estoque de um produto configurável é determinado por cada configuração associada. Como o produto foi salvo sem inserir uma quantidade, a variável **[!UICONTROL Stock Status]** está definida como `Out of Stock`.

   >[!NOTE]
   >
   >A variável **Status do estoque** do produto configurável é um **_semimensalmente_** configuração controlada. É parcialmente controlada pelo status de estoque de seus produtos derivados. Faz parte de um **_vários critérios_** cálculo do status do estoque, descrito na seção [Configurar o status do estoque](#configure-the-stock-status) seção.

1. Insira o produto **[!UICONTROL Weight]**.

>[!NOTE]
>
>Um produto configurável deve sempre ter um peso. Se você selecionar **[!UICONTROL This item has no weight]** na lista suspensa, é alterado automaticamente para **[!UICONTROL This item has weight]** depois de salvar o produto.

1. Aceitar o padrão **[!UICONTROL Visibility]** configuração de `Catalog, Search`.

1. Para incluir o produto na lista de [novos produtos](../content-design/widget-new-products-list.md), selecione o **[!UICONTROL Set Product as New]** caixa de seleção

1. Para atribuir Categorias ao produto, clique no link **[!UICONTROL Select…]** e siga um destes procedimentos:

   **Escolher uma categoria existente**:

   - Comece a digitar na caixa até encontrar uma correspondência.

   - Marque a caixa de seleção da categoria a ser atribuída.

   ![Selecione uma ou mais categorias para o produto do pacote](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Criar uma categoria**:

   - Clique em **[!UICONTROL New Category]**.

   - Insira o **[!UICONTROL Category Name]** e escolha o **[!UICONTROL Parent Category]**, que determina sua posição na estrutura de menu.

   s- Clique **[!UICONTROL Create Category]**.

1. Escolha o **[!UICONTROL Country of Manufacture]**.

   Pode haver atributos adicionais usados para descrever o produto. A seleção varia de acordo com o conjunto de atributos, e você pode concluí-los posteriormente.

### Etapa 5: salvar e continuar

Agora é um bom momento para salvar seu trabalho. No canto superior direito, clique em **[!UICONTROL Save]**. Nas próximas etapas, você definirá as configurações para cada variação do produto.

## Parte 2: Adição de configurações

O exemplo a seguir mostra como adicionar configurações para três cores e três tamanhos. Ao todo, nove produtos simples são criados com SKUs exclusivas para abranger todas as combinações possíveis de variações. Por padrão, o nome do produto e o SKU de cada variação se baseiam no valor do atributo e no nome do produto principal ou SKU.

A barra de progresso na parte superior da página mostra onde você está no processo e o orienta em cada etapa.

### Etapa 1: Escolher os atributos

1. Continuando de cima, role para baixo até a _[!UICONTROL Configurations]_e clique em **[!UICONTROL Create Configurations]**.

   ![Configurações](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. Marque a caixa de seleção de cada atributo que você deseja incluir como uma configuração.

   Neste exemplo, `color` e `size` são selecionados.

   ![Selecionar atributos](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   A lista inclui todos os atributos do conjunto de atributos que podem ser usados em um produto configurável.

1. Se quiser adicionar um atributo, clique em **[!UICONTROL Create New Attribute]** e faça o seguinte:

   - Complete as propriedades do atributo.

   - Clique em **[!UICONTROL Save Attribute]**.

   - Marque a caixa de seleção do atributo.

1. No canto superior direito, clique em **[!UICONTROL Next]**.

### Etapa 2: Inserir os valores de atributo

1. Para cada atributo, marque a caixa de seleção dos valores que se aplicam ao produto.

   ![Valores de atributo](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. Para reorganizar os atributos, segure _Reordenar_ ( ![Ícone de ordem de classificação](../assets/icon-sort-order.png) ) e mova a seção para uma nova posição.

   A ordem determina a posição das listas suspensas na página do produto.

1. Na barra de progresso, clique em **[!UICONTROL Next]**.

### Etapa 3: configurar as imagens, o preço e a quantidade

Essa etapa determina as imagens, os preços e a quantidade de cada configuração. As opções disponíveis são as mesmas para cada uma e você pode escolher apenas uma. Você pode aplicar a mesma configuração a todos os SKUs, aplicar uma configuração exclusiva a cada SKU ou ignorar as configurações por enquanto.

Escolha as opções de configuração que se aplicam.

Use um dos métodos a seguir para configurar o **[!UICONTROL images]**:

**Método 1:** Aplicar um único conjunto de imagens a todos os SKUs

1. Selecionar **[!UICONTROL Apply single set of images to all SKUs]**.

1. Navegue até cada imagem que deseja incluir na galeria de produtos ou arraste-as para a caixa.

![Usar as mesmas imagens para todos os SKUs](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**Método 2:** Aplicar imagens exclusivas para cada SKU

Como a imagem do produto principal já foi carregada, você pode usar essa opção para carregar uma imagem de cada cor. É possível adicionar uma imagem diferente que aparece no carrinho de compras quando alguém compra o item em uma cor específica.

1. Selecionar **[!UICONTROL Apply unique images by attribute to each SKU]**.

1. Selecione o **[!UICONTROL Attribute]** que as imagens ilustram, como `color`.

1. Para cada valor de atributo, navegue até as imagens que deseja usar para essa configuração ou arraste-as para a caixa.

   Se você arrastar a imagem para uma caixa de valor, ela também aparecerá nas seções para os outros valores. Para excluir uma imagem, clique no link _Lixeira_ (![Ícone de lixeira](../assets/icon-delete-trashcan-solid.png)) ícone.

   ![Imagens exclusivas por SKU](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

Use um dos métodos a seguir para configurar o **[!UICONTROL prices]**:

**Método 1:** Aplicar o mesmo preço a todos os SKUs

1. Se o preço for o mesmo para todas as variações, selecione **[!UICONTROL Apply single price to all SKUs]**.

1. Insira o **[!UICONTROL Price]**.

   ![Mesmo preço por SKU](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**Método 2:** Aplicar um preço diferente para cada SKU

1. Se o preço for diferente para cada produto ou para algumas variações do produto, selecione **[!UICONTROL Apply unique prices by attribute to each SKU]**.

1. Selecione o **[!UICONTROL Attribute]** é a base da diferença de preço.

1. Insira o **[!UICONTROL Price]** para cada valor de atributo.

   Neste exemplo, o tamanho XL custa mais.

   ![Preço único por SKU](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

Use um dos métodos a seguir para configurar o **[!UICONTROL Quantity]**:

**Método 1:** Aplicar a mesma quantidade a todos os SKUs

Se a quantidade for a mesma para todos os SKUs, selecione **[!UICONTROL Apply single quantity to each SKU]** e especifique a quantidade.

_Comerciantes de origem única_ - Insira o **[!UICONTROL Quantity]**.

_Comerciantes de várias origens usando [Inventory management](../inventory-management/introduction.md)_ - Atribuir origens e adicionar quantidades para todas as grades de produtos geradas:

1. Selecione o **[!UICONTROL Apply single quantity to each SKU]** opção.

1. Para adicionar uma origem, clique em **[!UICONTROL Assign Sources]**.

1. Procure ou procure uma origem que deseja adicionar. Marque a caixa de seleção ao lado das fontes que deseja adicionar ao produto.

1. Informe uma quantia de inventário em estoque por origem.

   ![Quantidade Única para Todos os SKUs, atribuir origem](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**Método 2:** Aplicar quantidade diferente por atributo

_Comerciantes de origem única_ - Insira o **[!UICONTROL Quantity]**.

_Comerciantes de várias origens usando [Inventory management](../inventory-management/introduction.md)_ - Atribuir origens e adicionar quantidades para todas as grades de produtos geradas:

1. Se a quantidade for diferente para cada SKU, selecione **[!UICONTROL Apply unique quantity by attribute to each SKU]**.

1. Insira o **[!UICONTROL Quantity]** para cada.

   ![Quantidades diferentes por atributo](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

Quando a configuração de imagens, preço e quantidade estiver concluída, clique em **[!UICONTROL Next]** no canto superior direito.

### Etapa 4: gerar as configurações do produto

Aguarde um momento para que a lista de produtos seja exibida e siga um destes procedimentos:

- Se estiver satisfeito com as configurações, clique em **[!UICONTROL Generate Products]**.

- Para fazer correções, clique em **[!UICONTROL Back]**.

![Revisar resumo antes de gerar variações de produto](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

As atuais variações de produtos aparecem na parte inferior do _Configuração_ seção.

![Configurações atuais](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### Etapa 5: adicionar imagens de produtos

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o _[!UICONTROL Images and Videos]_seção.

1. Clique em _Câmera_ lado a lado e navegue até a imagem principal que deseja usar para o produto configurável.

Para obter mais informações, consulte [Imagens e vídeo](product-images-and-video.md).

### Etapa 6: Preencher as informações do produto

Role para baixo e preencha as informações nas seguintes seções, conforme necessário:

- [Conteúdo](product-content.md)

- [Produtos relacionados, venda adicional e venda cruzada](related-products-up-sells-cross-sells.md)

- [Otimização do mecanismo de pesquisa](product-search-engine-optimization.md)

- [Opções personalizáveis](settings-advanced-custom-options.md)

- [Produtos em sites](settings-basic-websites.md)

- [Design](settings-advanced-design.md)

- [Opções de presente](product-gift-options.md)

### Etapa 7: publicar o produto

1. Se estiver pronto para publicar o produto no catálogo, defina **[!UICONTROL Enable Product]** para `Yes` e siga um destes procedimentos:

   - **Método 1:** Salvar e visualizar

      - No canto superior direito, clique em **[!UICONTROL Save]**.

      - Para exibir o produto em sua loja, escolha **[!UICONTROL Customer View]** no _Admin_ ( ![Seta de menu](../assets/icon-menu-down-arrow-black.png) ).

     A loja é aberta em uma nova guia do navegador.

     ![Visualização do cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Método 2:** Salvar e fechar

     No _[!UICONTROL Save]_( ![Seta de menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), escolha **[!UICONTROL Save & Close]**.

### Etapa 8: configurar as miniaturas do carrinho

Se você tiver uma imagem diferente para cada variação, poderá definir a configuração para usar a imagem correta para a miniatura do carrinho de compras.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Checkout]** por baixo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o _[!UICONTROL Shopping Cart]_seção.

1. Definir **[!UICONTROL Configurable Product Image]** para `Product Thumbnail Itself`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

   ![Carrinho de compras - Imagem do produto configurável](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## Configurar o status do estoque

O status do estoque de produtos configuráveis é diferente do status do estoque do produto simples, onde é uma representação direta da disponibilidade do produto. Para um produto configurável, o status do estoque faz parte de um **_vários critérios_** cálculo do status do estoque.

### Visão geral

Os princípios mais importantes dos relacionamentos de Status do Estoque são os seguintes:

- Quando você altera a variável **[!UICONTROL Stock Status]** do produto configurável como `Out of Stock` e clique em **[!UICONTROL Save]**, é **_não controlado_** pelos status de estoque de seus produtos derivados. É sempre exibido como `Out of Stock` no Admin e na Loja.

- Ao definir a variável **[!UICONTROL Stock Status]** do produto configurável como `In Stock` e clique em **[!UICONTROL Save]**, é **_apenas parcialmente controlado_** pelos status de estoque de seus produtos derivados, que são refletidos na Admin e na Loja.

### Descrição detalhada

A variável _Status do estoque_ do produto configurável é parcialmente controlado pelo Status do Estoque de seus produtos derivados e de acordo com o seguinte **_vários critérios_** cálculos do status do estoque:

#### Somente com origem/estoque padrão:

- Se o Status do Estoque do produto configurável for **_manualmente_** definir como `Out of Stock` por um usuário administrador, importação de arquivo ou chamada de API, permanece como `Out of Stock` em ambos os **_Admin_** e **_Loja_** até que seja  **_manualmente_** alterado para `In stock` por um usuário administrador, importação de arquivo ou chamada de API. Ela não pode ser controlada pelo status de estoque de seus produtos derivados.

- Se o Status do Estoque do produto configurável for **_manualmente_** definir como `In Stock` por um usuário administrador, importação de arquivo ou chamada de API, o status do estoque é **_automaticamente_** controlado pelo status de estoque de seus produtos derivados em ambos os **_Admin_** e **_Loja_**.

>[!NOTE]
>
>As existências e fontes personalizadas fazem parte do [Inventory management](../inventory-management/sources-stocks.md) e é altamente recomendável usar essa ferramenta exclusivamente para gerenciar estoque e fonte. As funções de estoque e fonte padrão fazem parte da `CatalogInventory` módulo, que agora está obsoleto.

#### Com pelo menos uma fonte/estoque personalizado:

- Se o valor configurável do Status do estoque do produto for **_manualmente_** definir como `Out of Stock` por um usuário administrador, importação de arquivo ou chamada de API, permanece como `Out of Stock` em ambos os **_Admin_** e **_Loja_** até que seja **_manualmente_** alterado para `In Stock` por um usuário administrador, importação de arquivo ou chamada de API. É **_não é possível_** ser controlado pelo status de estoque de seus produtos derivados.

- Se o valor configurável do Status do estoque do produto for **_manualmente_** definir como `In Stock` por um usuário administrador, importação de arquivo ou chamada de API, o status do estoque é **_automaticamente_** controlado pelo status de estoque de seus produtos derivados no **_Loja_** somente.

- Se o valor configurável do Status do estoque do produto for **_manualmente_** definir como `In Stock` por um usuário administrador, importação de arquivo ou chamada de API, permanece como `In Stock` no **_Admin_** até que seja **_manualmente_** alterado para `Out of Stock` por um usuário administrador, importação de arquivo ou chamada de API. É **_não é possível_** ser controlado pelo status de estoque de seus produtos derivados.

## Coisas para lembrar

- Um produto configurável permite que o comprador escolha opções entre tipos de entrada suspensos, de seleção múltipla, de amostra visual e de amostra de texto. Cada opção é um produto simples e separado.

- [Status do estoque](../inventory-management/sources-stocks.md) para um produto configurável, é uma configuração controlada semimanualmente. É diferente do status do estoque do produto simples, onde é uma representação direta da disponibilidade do produto. Para um produto configurável, o status do estoque faz parte de um cálculo de status do estoque com vários critérios.

- Os produtos secundários configuráveis podem ser produtos simples ou virtuais **sem opções personalizadas**. Para tornar virtuais os produtos personalizados secundários, você deve selecionar `Тhis item has no weight` para o **[!UICONTROL Weight]** para cada uma delas.

- Os atributos usados para variações de produtos devem ter um escopo global e o cliente deve ser solicitado a escolher um valor. Os atributos de variação do produto devem ser incluídos no conjunto de atributos usado como modelo para o produto configurável.

- O conjunto de atributos usado como modelo para um produto configurável deve incluir os atributos que contêm os valores necessários para cada variação de produto.

- A imagem em miniatura no carrinho de compras pode ser definida para exibir a imagem do registro do produto configurável ou da variação do produto.

- [Atributos de amostra](swatches.md#create-swatches-for-products) pode ser configurado para não exibir imagens do produto simples correspondentes quando a amostra for selecionada ao configurar o **[!UICONTROL Update Product Preview Image]** valor da opção para `No` na página de edição de atributos no Admin.

- O tema controla como a Galeria de imagens se comporta quando um usuário alterna entre as configurações do produto. O comportamento padrão para a variável _Em branco_ o tema é substituir as imagens do produto configuráveis principais pela variação do produto selecionado. Para o tema Luma, o comportamento padrão é anexar as imagens de variação do produto selecionado às imagens do produto configuráveis principais.
