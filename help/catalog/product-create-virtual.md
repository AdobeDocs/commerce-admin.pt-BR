---
title: Produto virtual
description: Saiba como criar um produto virtual que represente um item não tangível, como uma associação, serviço, garantia ou assinatura.
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Produto virtual

Os produtos virtuais, ou bens digitais, representam itens não tangíveis, como associações, serviços, garantias ou assinaturas e downloads digitais de livros, músicas, vídeos ou outros produtos. Os produtos virtuais podem ser vendidos individualmente ou incluídos como parte da [Produto agrupado](product-create-grouped.md), [Produto configurável](product-create-configurable.md)ou [Produto do pacote](product-create-bundle.md) tipos do produto.

Para além da ausência de _[!UICONTROL Weight]_, o processo de criação de um produto virtual e um produto simples é o mesmo. As instruções a seguir demonstram o processo de criação de um produto virtual usando um [modelo do produto](attribute-sets.md), campos obrigatórios e configurações básicas. Quando terminar as noções básicas, você poderá concluir as outras configurações do produto conforme necessário.

>[!NOTE]
>
>O PayPal descontinuou o suporte para a venda de produtos digitais por meio do Check-out expresso do PayPal. Eles recomendam usar [PayPal Payments Standard](../stores-purchase/paypal-payments-standard.md) ou qualquer outro gateway de pagamento PayPal para processar qualquer pedido que inclua produtos virtuais.

![Produto virtual](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## Etapa 1: Escolher o tipo de produto

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. No _[!UICONTROL Add Product]_( ![Seta de menu](../assets/icon-menu-down-arrow-red.png){width="25"} ) no canto superior direito, escolha **[!UICONTROL Virtual Product]**.

   ![Adicionar produto virtual](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## Etapa 2: Escolher o conjunto de atributos

Para escolher a variável [conjunto de atributos](attribute-sets.md) que é usado como modelo para o produto, siga um destes procedimentos:

- Clique em **[!UICONTROL Attribute Set]** e insira todo ou parte do nome do conjunto de atributos.

- Na lista exibida, escolha o conjunto de atributos que deseja usar.

O formulário é atualizado para refletir a alteração.

![Escolher Conjunto de Atributos](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Etapa 3: concluir as configurações necessárias

1. Insira o **[!UICONTROL Product Name]**.

1. Aceitar o padrão **[!UICONTROL SKU]** que se baseia no nome do produto ou insira outro.

1. Insira o produto **[!UICONTROL Price]**.

1. Como o produto ainda não está pronto para publicação, defina **[!UICONTROL Enable Product]** para `No`.

1. Clique em **[!UICONTROL Save]** e continue.

   Quando o produto for salvo, a variável [Exibição da loja](introduction.md#product-scope) seletor aparece no canto superior esquerdo.

1. Escolha o **[!UICONTROL Store View]** onde o produto deve estar disponível.

   ![Escolher exibição da loja](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Etapa 4: concluir as configurações básicas

1. Definir **[!UICONTROL Tax Class]** a um dos seguintes:

   - `None`
   - `Taxable Goods`

1. Insira o **[!UICONTROL Quantity]** do produto em estoque e faça o seguinte:

   - Aceitar o padrão **[!UICONTROL Stock Status]** configuração de `In Stock`.

     Como um produto virtual não é enviado, o **[!UICONTROL Weight]** não é usado.

   - Aceitar o padrão **[!UICONTROL Visibility]** configuração de `Catalog, Search`.

   >[!NOTE]
   >
   >Se você habilitar [Inventory management](../inventory-management/introduction.md), comerciantes de origem única definem a quantidade nesta seção. Comerciantes de várias origens adicionam origens e quantidades na seção Origens. Consulte o seguinte _Atribuir Origens e Quantidades (Inventory management)_ seção.

1. Para atribuir **[!UICONTROL Categories]** ao produto, clique no link **[!UICONTROL Select…]** e siga um destes procedimentos:

   **Escolher uma categoria existente**:

   - Comece a digitar na caixa até encontrar uma correspondência.

   - Marque a caixa de seleção da categoria a ser atribuída.

   **Criar uma categoria**:

   - Clique em **[!UICONTROL New Category]**.

   - Insira o **[!UICONTROL Category Name]** e escolha o **[!UICONTROL Parent Category]**, que determina sua posição na estrutura de menu.

   - Clique em **[!UICONTROL Create Category]**.

   Pode haver atributos individuais adicionais que descrevam o produto. A seleção varia de acordo com o conjunto de atributos e você pode concluí-los posteriormente.

### Atribuir origens e quantidades ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Etapa 5: Preencher as informações do produto

Preencha as informações nas seguintes seções conforme necessário:

- [Conteúdo](product-content.md)
- [Imagens e vídeos](product-images-and-video.md)
- [Otimização do mecanismo de pesquisa](product-search-engine-optimization.md)
- [Produtos relacionados, venda adicional e venda cruzada](related-products-up-sells-cross-sells.md)
- [Opções personalizáveis](settings-advanced-custom-options.md)
- [Produtos em sites](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Opções de presente](product-gift-options.md)

>[!NOTE]
>
>A variável _[!UICONTROL Is this downloadable product?]_está desativada por padrão. Habilitar esse recurso para um produto virtual torna o produto [Baixável](product-create-downloadable.md#downloadable-product).

## Etapa 6: publicar o produto

1. Se estiver pronto para publicar o produto no catálogo, defina **[!UICONTROL Enable Product]** para `Yes`.

1. Siga um destes procedimentos:

   - **Método 1:** Salvar e visualizar

      - No canto superior direito, clique em **[!UICONTROL Save]**.

      - Para exibir o produto em sua loja, escolha **[!UICONTROL Customer View]** no _Admin_ ( ![Seta de menu](../assets/icon-menu-down-arrow-black.png) ).

     A loja é aberta em uma nova guia do navegador.

     ![Visualização do cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Método 2:** Salvar e fechar

     No _[!UICONTROL Save]_(![Seta de menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), escolha **[!UICONTROL Save & Close]**.

## Coisas para lembrar

- Os produtos virtuais são usados para produtos incorpóreos, como serviços, assinaturas e garantias.

- Os produtos virtuais são muito parecidos com produtos simples, mas sem peso.

- As opções de envio não aparecem durante o check-out, a menos que haja um produto tangível no carrinho.
