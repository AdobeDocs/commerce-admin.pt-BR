---
title: '[!DNL Page Builder] Apresentação parte 3: conteúdo do catálogo'
description: Saiba como adicionar uma lista de produtos a um [!DNL Page Builder] página.
exl-id: f2a0dc29-6d8f-4b97-a947-72659c01d0cb
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '1481'
ht-degree: 0%

---

# [!DNL Page Builder] Apresentação parte 3: conteúdo do catálogo

Este exercício demonstra como é fácil adicionar uma lista de produtos a uma página, personalizar páginas de produtos e criar um atributo personalizado que adicione a [!DNL Page Builder] espaço de trabalho para um conjunto de atributos do produto.

![Lista de produtos](./assets/pb-add-content-products-list.png){width="600" zoomable="yes"}

Este exercício pressupõe que você tenha concluído [Parte 1: Página simples](1-simple-page.md) e [Parte 2: Blocos](2-blocks.md), incluindo os pré-requisitos e os arquivos de amostra baixados. Siga as três partes deste exercício em ordem.

## Parte 1: Adicionar uma lista de produtos

[!DNL Page Builder] O facilita a adição de uma lista de produtos ao estágio. Neste exemplo, a lista de produtos é adicionada diretamente a uma página.

### Etapa 1: adicionar uma lista de produtos ao estágio

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Localize o _Página simples_ que você criou no primeiro exercício e modificou no segundo, e selecionou **[!UICONTROL Edit]** no _[!UICONTROL Action]_coluna.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Content]** e clique em **[!UICONTROL Edit with Page Builder]** ou dentro da área de visualização de conteúdo.

1. No [!DNL Page Builder] painel em _[!UICONTROL Layout]_, arraste um **[!UICONTROL Row]**no topo do palco.

1. No [!DNL Page Builder] painel, expandir **[!UICONTROL Add Content]** e arraste uma **[!UICONTROL Products]** espaço reservado para a nova linha.

   ![Arrastar um espaço reservado de produtos para a linha](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

### Etapa 2: compor a condição

1. Passe o mouse sobre o contêiner de produtos vazio para exibir a caixa de ferramentas e escolher o _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

   ![Caixa de ferramentas Produtos](./assets/pb-add-content-products-toolbox.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Select Products By]**, escolha `Condition`.

1. Adicione uma condição:

   - Clique em _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) ícone.

   - Em _[!UICONTROL Product Attribute]_, escolha **[!UICONTROL Category]**.

     ![Escolha do atributo de categoria para a condição](./assets/pb-add-content-products-settings-condition.png){width="600" zoomable="yes"}

   - Conclua o _[!UICONTROL Category is].._ parte da condição clicando no ícone Mais (...) e clique no link _Seletor_ (![Ícone do seletor](../assets/icon-list-chooser.png)) ícone.

     ![Definição da condição](./assets/pb-add-content-products-settings-condition-category-is.png){width="600" zoomable="yes"}

   - Na árvore de categorias, faça drill-down para a **Mulheres > Topos** e selecione a **Árvores** caixa de seleção

     ![Escolha da categoria na árvore](./assets/pb-add-content-products-settings-condition-category-tree.png){width="600" zoomable="yes"}

   - Clique na marca de seleção (![Ícone de marca de seleção](../assets/icon-checkmark-green-circle.png)) ícone.

     A ID de categoria correspondente é exibida no campo para concluir a condição.

### Etapa 3: Concluir as configurações

1. Insira o **[!UICONTROL Number of Products to Display]**.

   Por padrão, a lista exibe cinco produtos.

1. Conclua as configurações restantes conforme necessário.

   Se necessário, use as descrições de campo no final da [Adicionar conteúdo - Produtos](products.md) página para referência.

1. Quando terminar, clique em **[!UICONTROL Save]** para salvar as configurações e retornar para a [!DNL Page Builder] espaço de trabalho.

   ![Lista de produtos no estágio](./assets/pb-add-content-products-list-stage.png){width="600" zoomable="yes"}

1. No canto superior direito do estágio, clique na guia _Fechar tela cheia_ ( ![Ícone Fechar tela inteira](./assets/pb-icon-reduce.png){width="20"} ) ícone.

   Clicar nesse ícone retornará para a _[!UICONTROL Content]_para a página com a pré-visualização exibida.

1. No canto superior direito, clique na guia **[!UICONTROL Save]** seta e escolha **[!UICONTROL Save & Close]**.

## Parte 2: Personalizar a página do produto

>[!NOTE]
>
>Um usuário administrador deve ter [!UICONTROL Content] permissões para seus [escopo da função](../systems/permissions-user-roles.md) para ver [!UICONTROL Edit with Page Builder] e poder usar o Page Builder.

Nesta parte do exercício, você aprenderá como é fácil personalizar uma página de produto ao colocar um vídeo abaixo do conjunto de guias na página do produto. O processo a ser atualizado [página de categoria](../catalog/categories-content-settings.md) o conteúdo é basicamente o mesmo.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Encontre um produto simples que você pode usar para este exemplo e abra-o no modo de edição.

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Content]** seção.

1. Ao lado de _[!UICONTROL Description]_, clique em **[!UICONTROL Edit with Page Builder]**.

   ![Conteúdo da descrição do produto](./assets/pb-catalog-product-content.png){width="600" zoomable="yes"}

   Se a descrição do produto foi inserida anteriormente sem [!DNL Page Builder], a descrição atual aparece como HTML em um [Código HTML](html-code.md) recipiente. Com o tema Luma, a descrição do produto aparece na guia Detail.

1. No [!DNL Page Builder] painel em _[!UICONTROL Layout]_, arraste um **[!UICONTROL Row]**para o estágio, colocando-o abaixo do contêiner de código HTML.

   Procure a diretriz vermelha para aparecer quando a linha estiver na posição correta.

   ![Arrastar uma linha para o estágio](./assets/catalog-product-content-stage-row-drag.png){width="600" zoomable="yes"}

1. No [!DNL Page Builder] painel, expandir **[!UICONTROL Media]** e arraste uma **[!UICONTROL Video]** espaço reservado para a nova linha.

   ![Espaço reservado do vídeo na linha](./assets/tutorial3-product-drag-video.png){width="600" zoomable="yes"}

1. Passe o mouse sobre o contêiner de vídeo vazio para exibir a caixa de ferramentas e escolher o _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

   ![Caixa de ferramentas Vídeo](./assets/pb-tutorial3-product-video-toolbox.png){width="500" zoomable="yes"}

1. Insira o **[!UICONTROL Video URL]**.

   O vídeo pode ser hospedado em [YouTube][1] ou [Vimeo][2]. O vídeo deste exemplo pode ser encontrado no YouTube no seguinte URL:

   `https://www.youtube.com/watch?v=ZpFrNyD4100`

   ![Edição do vídeo](./assets/pb-tutorial3-product-edit-video.png){width="500" zoomable="yes"}

1. Insira o **[!UICONTROL Maximum Width]** em pixels para a exibição do vídeo.

   Se você deixar essa opção em branco, o vídeo preencherá o espaço disponível.

1. Clique em **[!UICONTROL Save]** para salvar as configurações e retornar para a [!DNL Page Builder] espaço de trabalho.

   ![Vídeo no estágio de conteúdo](./assets/pb-tutorial3-product-video.png){width="600" zoomable="yes"}

1. No canto superior direito do estágio, clique na guia _Fechar tela cheia_ ( ![Ícone Fechar tela inteira](./assets/pb-icon-reduce.png){width="20"} ) ícone.

   Clicar nesse ícone retornará para a _[!UICONTROL Content]_para a página com a pré-visualização exibida.

1. No canto superior direito, clique na guia **[!UICONTROL Save]** seta e escolha **[!UICONTROL Save & Close]**.

Na loja, o vídeo é exibido abaixo do conjunto de guias. Para ver a aparência da página em um dispositivo móvel, é possível redimensionar a janela.

![Vídeo exibido na página do produto](./assets/pb-tutorial3-product-video-storefront.png){width="600" zoomable="yes"}

**Parabéns!** Você concluiu a segunda parte do tutorial Conteúdo do catálogo. Manter o trabalho criado para que você possa consultá-lo posteriormente.

## Parte 3: Adicionar atributos personalizados

Use o [!DNL Page Builder] atributo personalizado para adicionar um atributo totalmente [!DNL Page Builder] espaço de trabalho para uma página de produto, que você pode usar para criar conteúdo envolvente. Nesta parte do exercício, você aprenderá a criar um atributo personalizado usando o [!DNL Page Builder] tipo de entrada e aplique-o às páginas de produto no catálogo. Para obter mais informações sobre esses atributos, consulte [Atributos do produto](../catalog/product-attributes.md).

### Etapa 1: criar um produto

Para evitar alterações na loja em tempo real, crie um produto usando as propriedades descritas.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. No canto superior direito, clique em **[!UICONTROL Add Product]**.

1. Crie o produto com as seguintes propriedades:

   - 
     [!UICONTROL Conjunto de atributos]: Default
   - [!UICONTROL Product Name]: Meu produto
   - 
     [!UICONTROL SKU]: Tutorial
   - 
     [!UICONTROL Price]: 75.00
   - 
     [!UICONTROL Quantity]: 100
   - [!UICONTROL Stock Status]: Em estoque
   - 
     [!UICONTROL Weight]: 1
   - [!UICONTROL Categories]: Mulheres > Topos > Tees

1. No canto superior direito, clique na guia **[!UICONTROL Save]** seta e escolha **[!UICONTROL Save & Close]**.

### Etapa 2: Criar atributos personalizados

Nesta etapa, você cria dois novos atributos personalizados para mostrar como a [!DNL Page Builder] e os tipos de entrada do Editor de texto podem ser usados.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. No canto superior direito, clique em **[!UICONTROL Add New Attribute]**.

1. Insira um **[!UICONTROL Default Label]** para o atributo.

   Neste exemplo, use `My Page Builder Attribute` para o rótulo.

1. Definir **[!UICONTROL Catalog Input Type for Store Owner]** para `Page Builder`.

   Ao criar um atributo personalizado, você pode especificar o editor mais adequado para o aplicativo como `Page Builder` ou o padrão, WYSIWYG `Text Editor`.

   ![[!DNL Page Builder] Tipo de entrada](./assets/pb-attribute-page-builder.png){width="600" zoomable="yes"}

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Advanced Attribute Properties]** e faça as seguintes configurações:

   - [!UICONTROL Attribute Code]: insira um código de atributo em caracteres minúsculos, usando hifens em vez de espaços. Neste exemplo, use `my_page_builder_attribute`.
   - [!UICONTROL Scope]: aceite o valor padrão, `Store View`.
   - [!UICONTROL Default Value]: Insira um valor padrão para o atributo.
   - 
     [!UICONTROL Unique Value]: `No`
   - 
     [!UICONTROL Add to Column Options]: `No`
   - 
     [!UICONTROL Use in Filter Options]: `Yes`

1. No _[!UICONTROL Attribute Information]_à esquerda, escolha **[!UICONTROL Storefront Properties]**e faça as seguintes configurações:

   - 
     [!UICONTROL Use for Promo Rule Conditions]: `Yes`
   - 
     [!UICONTROL Visible on Catalog Pages on Storefront]: `Yes`
   - 
     [!UICONTROL Used in Product Listing]: `Yes`

1. Quando terminar, clique em **[!UICONTROL Save Attribute]**.

1. Repita as etapas anteriores para criar um segundo atributo com as mesmas propriedades básicas, mas com o tipo de entrada Editor de texto da seguinte maneira:

   - [!UICONTROL Default Label]: Meu atributo do editor de texto
   - [!UICONTROL Catalog Input Type for Store Owner]: Editor de texto
   - 
     [!UICONTROL Código de atributo]: `my_text_editor_attribute`

### Etapa 3: atualizar o conjunto de atributos do produto

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

   Neste exemplo, adicione temporariamente os novos atributos à variável `default` conjunto de atributos. No final deste exercício, remova os atributos do conjunto de atributos para não afetar seu catálogo.

   >[!NOTE]
   >
   >Se você não quiser alterar o armazenamento ao vivo, poderá acompanhar sem atualizar o conjunto de atributos.

1. Localize o _[!UICONTROL Default]_atributo definido na lista e clique duas vezes nele para abri-lo no modo de edição.

1. No _Atributos não atribuídos_ , localize os novos atributos criados e arraste cada um para a _[!UICONTROL Groups]_coluna, abaixo **[!UICONTROL Content]**.

   A localização do atributo na variável [!UICONTROL Groups] determina onde ele aparece na página.

   ![Novos atributos adicionados ao grupo de conteúdo](./assets/pb-product-attribute-set.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save]** para retornar à lista Conjuntos de atributos.

1. Quando solicitado, clique no link **[!UICONTROL Cache Management]** vincular na parte superior da página e atualizar qualquer cache inválido.

### Etapa 4: atualizar o produto

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Na grade Produtos, localize _Meu produto_ e abra-o no modo de edição.

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Content]** seção.

   Na parte superior da seção, há dois atributos padrão para o conteúdo do produto:

   - _Descrição curta_, que usa o padrão WYSIWYG [editor](../content-design/editor.md).
   - _Descrição_, que exibe o [!DNL Page Builder] visualização.

   ![Conteúdo do produto](./assets/pb-product-content-edit-with-page-builder.png){width="600" zoomable="yes"}

   À medida que você rolar a tela para a metade inferior da seção, há dois atributos que você criou e atribuiu:

   - _Meus [!DNL Page Builder] Atributo_, que exibe o [!DNL Page Builder] visualização.
   - _Meu atributo do editor de texto_, que usa o editor WYSIWYG padrão.

   ![Edição de conteúdo do produto](./assets/pb-product-content-my-attributes.png){width="600" zoomable="yes"}

1. No **Meu atributo do editor de texto** editor, insira `Text Editor Attribute placeholder text`.

   - No canto superior direito, clique na guia **[!UICONTROL Save]** seta e escolha **[!UICONTROL Save & Close]**.

1. Para **Meu atributo do Page Builder**, clique em **[!UICONTROL Edit with Page Builder]** e adicione o texto de descrição:

   - No [!DNL Page Builder] painel, expandir **[!UICONTROL Elements]** e arraste uma **[!UICONTROL Text object]** para o estágio.

   - Enter `Page Builder attribute placeholder text`.

   - No canto superior direito do estágio, clique na guia _Fechar tela cheia_ ( ![Ícone Fechar tela inteira](./assets/pb-icon-reduce.png){width="20"} ) ícone.

     ![Atributos personalizados com texto de espaço reservado](./assets/pb-product-content-attributes.png){width="600" zoomable="yes"}

1. Rolar para cima até **[!UICONTROL Description]**, clique em **[!UICONTROL Edit with Page Builder]** e adicione qualquer texto que desejar usando o mesmo método da etapa anterior.

1. No canto superior direito da página do produto, clique na guia **[!UICONTROL Save]** seta e escolha **[!UICONTROL Save & Close]**.

1. Se solicitado, clique no link **[!UICONTROL Cache Management]** vincular na mensagem na parte superior da página e atualizar qualquer cache inválido.

### Etapa 5: visualizar o resultado

1. Navegue até a página de exemplo do produto na vitrine.

   Neste exemplo, o produto pode ser encontrado na navegação superior em Mulheres > Topos > Árvores.

1. Role para baixo até _Meu atributo do Page Builder_ informações.

   A posição dos atributos na página do produto é determinada pelo tema. No tema Luma, os novos atributos estão localizados logo após a descrição do produto.

   ![[!DNL Page Builder] e atributos do Editor de texto na loja](./assets/pb-storefront-product-attribute.png){width="600" zoomable="yes"}

Você concluiu o [!DNL Page Builder] Exercício Conteúdo de catálogo. Manter o trabalho criado para que você possa consultá-lo posteriormente.

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
