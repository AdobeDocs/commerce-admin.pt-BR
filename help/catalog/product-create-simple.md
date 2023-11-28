---
title: Produto simples
description: Saiba como criar um produto simples que pode ser vendido individualmente ou como parte de um produto agrupado, configurável ou combinado.
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# Produto simples

Uma das chaves para aproveitar o potencial dos tipos de produtos é saber quando usar um produto simples e independente. Um produto simples pode ser vendido individualmente ou como parte de um produto agrupado, configurável ou pacote. Um produto simples com opções personalizadas às vezes é chamado de _produto composto_.

As instruções a seguir demonstram o processo de criação de um produto simples usando um [modelo do produto](attribute-sets.md), campos obrigatórios e configurações básicas. Cada campo obrigatório está marcado com um asterisco vermelho (`*`). Quando terminar as noções básicas, você poderá concluir as outras configurações do produto conforme necessário.

![Produto simples](./assets/product-simple.png){width="700" zoomable="yes"}

## Etapa 1: Escolher o tipo de produto

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. No _[!UICONTROL Add Product]_( ![Seta de menu](../assets/icon-menu-down-arrow-red.png){width="25"} ) no canto superior direito, escolha **[!UICONTROL Simple Product]**.

   ![Adicionar produto simples](./assets/product-add-simple.png){width="700" zoomable="yes"}

## Etapa 2: Escolher o conjunto de atributos

Para escolher a variável [conjunto de atributos](attribute-sets.md) que é usado como modelo para o produto:

- Clique em **[!UICONTROL Attribute Set]** e insira todo ou parte do nome do conjunto de atributos.

- Na lista exibida, escolha o conjunto de atributos que deseja usar.

O formulário é atualizado para refletir a alteração.

![Escolher conjunto de atributos](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Etapa 3: concluir as configurações necessárias

1. Insira o **[!UICONTROL Product Name]**.

1. Aceitar o padrão **[!UICONTROL SKU]** que se baseia no nome do produto ou insira outro.

1. Insira o produto **[!UICONTROL Price]**.

1. Como o produto ainda não está pronto para publicação, defina a **[!UICONTROL Enable Product]** opção para `No`.

1. click **[!UICONTROL Save]** e continue.

   Quando o produto for salvo, a variável [Exibição da loja](introduction.md#product-scope) seletor aparece no canto superior esquerdo.

1. Escolha o **[!UICONTROL Store View]** onde o produto deve estar disponível.

   ![Escolher a exibição da loja](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Etapa 4: concluir as configurações básicas

1. Definir **[!UICONTROL Tax Class]** a um dos seguintes:

   - `None`
   - `Taxable Goods`
   - `Refund Adjustments`
   - `Gift Options`
   - `Order Gift Wrapping`
   - `Item Gift Wrapping`
   - `Printed Gift Card`
   - `Reward Points`
   - `VAT Reduced`
   - `VAT Standard`

1. Insira o **[!UICONTROL Quantity]** do produto que está em estoque.

   Por padrão, **[!UICONTROL Stock Status]** está definida como `In Stock`.

   >[!NOTE]
   >
   >Se você habilitar [Inventory management](../inventory-management/introduction.md), os comerciantes de Origem Única definem a quantidade nesta seção. Comerciantes de várias origens adicionam origens e quantidades na seção Origens. Consulte o seguinte _Atribuir Origens e Quantidades (Inventory management)_ seção.

1. Insira o **[!UICONTROL Weight]** do produto.

1. Aceitar o padrão **[!UICONTROL Visibility]** configuração de `Catalog, Search`.

1. Para atribuir _[!UICONTROL Categories]_ao produto, clique no link **[!UICONTROL Select…]**e siga um destes procedimentos:

   **Escolher uma categoria existente**:

   - Comece a digitar na caixa até encontrar uma correspondência.

   - Marque a caixa de seleção de cada categoria que deve ser atribuída.

   **Criar uma categoria**:

   - Clique em **[!UICONTROL New Category]**.

   - Insira o **[!UICONTROL Category Name]** e escolha o **[!UICONTROL Parent Category]**, que determina sua posição na estrutura de menu.

   - Clique em **[!UICONTROL Create Category]**.

1. Para incluir o produto na lista de [novos produtos](../content-design/widget-new-products-list.md), selecione o **[!UICONTROL Set Product as New]** caixa de seleção

1. Escolha o **[!UICONTROL Country of Manufacture]**.

Pode haver atributos individuais adicionais que descrevam o produto. A seleção varia de acordo com o conjunto de atributos, e você pode concluí-los posteriormente.

### Atribuir origens e quantidades ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Etapa 5: Preencher as informações do produto

Role para baixo e preencha as informações nas seguintes seções, conforme necessário:

- [Conteúdo](product-content.md)
- [Imagens e vídeos](product-images-and-video.md)
- [Produtos relacionados, venda adicional e venda cruzada](related-products-up-sells-cross-sells.md)
- [Otimização do mecanismo de pesquisa](product-search-engine-optimization.md)
- [Opções personalizáveis](settings-advanced-custom-options.md)
- [Produtos em sites](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Opções de presente](product-gift-options.md)

## Etapa 6: publicar o produto

1. Se estiver pronto para publicar o produto no catálogo, defina as **[!UICONTROL Enable Product]** alternar para `Yes`.

1. Siga um destes procedimentos:

   - **Método 1:** Salvar e visualizar

      - No canto superior direito, clique em **[!UICONTROL Save]**.

      - Para exibir o produto em sua loja, escolha **[!UICONTROL Customer View]** no _Admin_ (![Seta de menu](../assets/icon-menu-down-arrow-black.png)).

     A loja é aberta em uma nova guia do navegador.

     ![Visualização do cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Método 2:** Salvar e fechar

     No _[!UICONTROL Save]_ ( ![Seta de menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), escolha **[!UICONTROL Save & Close]**.

## Coisas para lembrar

- Produtos simples podem ser incluídos em tipos de produtos configuráveis, agrupados e agrupados.

- A configuração simples de um produto substitui as configurações configuráveis de um produto específico.

- Um produto simples pode ter opções personalizadas com vários tipos de entrada, o que permite vender muitas variações de produto de uma única SKU.
