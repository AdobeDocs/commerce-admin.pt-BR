---
title: Produto baixável
description: Saiba como criar um produto para download que pode ser entregue como um arquivo digital.
exl-id: c3dd4c5f-adc1-4a8f-a9da-7f0dedd1ee34
feature: Catalog Management, Products
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 0%

---

# Produto baixável

Um produto para download pode ser qualquer item que você pode fornecer como um arquivo, como um eBook, música, vídeo, aplicativo de software ou atualização. Você pode oferecer um álbum para venda e vender cada música individualmente. Você também pode usar um produto para download para fornecer uma versão eletrônica do catálogo de produtos.

Como o download não estará disponível até a compra, você pode fornecer amostras, como um trecho de um livro, um clipe de um arquivo de áudio ou um trailer de um vídeo. Um exemplo é algo que o cliente pode experimentar antes de comprar o produto. Os arquivos que você disponibiliza para download podem ser carregados no seu servidor ou em um servidor diferente.

![Produto baixável](./assets/storefront-product-downloadable.png){width="700" zoomable="yes"}

Os produtos para download podem ser configurados para exigir que o cliente faça logon em uma conta para receber o link ou podem ser enviados por email e compartilhados com outras pessoas. O status do pedido antes que o download se torne disponível, os valores padrão e outras opções de delivery são definidos na configuração. Conforme você planeja fazer o download das adições ao catálogo, anote o seguinte:

- Os produtos baixáveis podem ser carregados no servidor ou vinculados a partir de outro servidor na Internet.

- Você pode determinar o número de vezes que um cliente pode baixar um produto.

- Os clientes que compram um produto para download podem precisar fazer logon antes de passar pelo checkout.

- A entrega de um produto para download pode ser feita quando o pedido estiver com o status `Pending` ou `Invoiced`.

- Como os produtos baixáveis não são remetidos, a etapa _Remessa_ do check-out é ignorada quando o carrinho contém somente o produto baixável.


## Configurar as opções de download

As definições de configuração para download determinam os valores padrão e as opções de entrega para produtos para download e especificam se os convidados podem comprar downloads.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção _[!UICONTROL Downloadable Product Options]_.

   ![Opções de Produto Baixáveis](../configuration-reference/catalog/assets/catalog-downloadable-product-options.png){width="700" zoomable="yes"}

   Para obter uma lista detalhada dessas opções de configuração, consulte [_Opções de Produto Baixáveis_](../configuration-reference/catalog/catalog.md#downloadable-product-options) na _Referência de Configuração_.

1. Para determinar o status do processo do pedido quando o download se tornar disponível, defina **[!UICONTROL Order Item Status to Enable Downloads]** como um dos seguintes:

   - `Pending`
   - `Invoiced`

1. Para definir um limite padrão no número de downloads que um único cliente pode fazer, insira o número para **[!UICONTROL Default Maximum Number of Downloads]**.

1. Defina **[!UICONTROL Shareable]** como um dos seguintes:

   - `Yes` - Permite que os clientes enviem o link de download por email para outras pessoas.
   - `No` - Impede que os clientes compartilhem o link de download com outras pessoas, exigindo que os clientes façam logon em suas contas para acessar os links de download.

1. Para **[!UICONTROL Default Sample Title]**, insira o cabeçalho que você deseja exibir acima da seleção de amostras.

   ![Título de exemplo](./assets/product-downloadable-config-sample-title.png){width="400"}

1. Para **[!UICONTROL Default Link Title]**, insira o texto padrão que deseja usar para os links de download.

1. Se quiser que o link de download seja aberto em uma nova janela do navegador, defina **[!UICONTROL Opens Links in New Window]** como `Yes`.

   Essa configuração é usada para manter a janela do navegador aberta para sua loja.

1. Para determinar como o conteúdo para download é entregue, defina **[!UICONTROL Use Content Disposition]** como um dos seguintes:

   - `Attachment` - Entrega o link de download por email como um anexo.
   - `Inline` - Fornece o link de download como um link em uma página da Web.

1. Se você quiser exigir que os compradores se registrem em uma conta de cliente e façam logon antes de comprar um download, defina **[!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items]** como `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Criar um produto para download

As instruções a seguir demonstram o processo de criação de um produto para download usando um [modelo de produto](attribute-sets.md), campos obrigatórios e configurações básicas. Cada campo obrigatório está marcado com um asterisco vermelho (`*`). Quando terminar as noções básicas, você poderá concluir as outras configurações do produto conforme necessário.

>[!NOTE]
>
>Os nomes de arquivos para download podem incluir letras e números. Um caractere de traço ou sublinhado pode ser usado para representar um espaço entre palavras. Todos os caracteres inválidos no nome do arquivo são substituídos por um sublinhado.

### Etapa 1: Escolher o tipo de produto

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. No menu _[!UICONTROL Add Product]_( ![Seta do menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), no canto superior direito, escolha `Downloadable Product`.

   ![Adicionar Produto Baixável](./assets/product-add-downloadable.png){width="700" zoomable="yes"}

### Etapa 2: Escolher o conjunto de atributos

Os dados de exemplo incluem um [conjunto de atributos](attribute-sets.md) chamado _Baixável_ que tem campos especiais para produtos baixáveis. É possível usar um modelo existente ou criar outro antes de salvar o produto.

Para escolher o conjunto de atributos usado como modelo para o produto, siga um destes procedimentos:

- Para **[!UICONTROL Search]**, insira o nome do conjunto de atributos.

- Na lista, escolha o conjunto de atributos `Downloadable`.

O formulário é atualizado para refletir a alteração.

![Escolher Conjunto de Atributos](./assets/product-create-choose-attribute-set-downloadable.png){width="600" zoomable="yes"}

### Etapa 3: concluir as configurações necessárias

1. Insira o **[!UICONTROL Product Name]**.

1. Aceite o **[!UICONTROL SKU]** padrão que é baseado no nome do produto ou digite outro.

1. Insira o produto **[!UICONTROL Price]**.

1. Como o produto ainda não está pronto para publicação, defina **[!UICONTROL Enable Product]** como `No`.

1. clique em **[!UICONTROL Save]** e continue.

   Quando o produto é salvo, o seletor de [Exibição da loja](introduction.md#product-scope) aparece no canto superior esquerdo.

1. Escolha o **[!UICONTROL Store View]** onde o produto deve estar disponível.

   ![Escolher exibição da loja](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Etapa 4: concluir as configurações básicas

1. Defina **[!UICONTROL Tax Class]** como um dos seguintes:

   - `None`
   - `Taxable Goods`

1. Insira o **[!UICONTROL Quantity]** do produto em estoque.

   Anote o seguinte:

   - Por padrão, **[!UICONTROL Stock Status]** está definido como `Out of Stock`.

   - Como os produtos baixáveis não são remetidos, o campo **[!UICONTROL Weight]** não é usado. Se você habilitar este recurso, ele se tornará um [Produto simples](product-create-simple.md) e o _Este produto pode ser baixado?A guia_ não pode ser usada.

   >[!NOTE]
   >
   >Se você habilitar o [Inventory management](../inventory-management/introduction.md), os comerciantes do Single Source definirão a quantidade nesta seção. Vários comerciantes do Source adicionam origens e quantidades na seção Origens. Consulte a seguinte seção _Atribuir Fontes e Quantidades (Inventory management)_.

1. Aceite a configuração padrão **[!UICONTROL Visibility]** de `Catalog, Search`.

1. Para incluir o produto na [lista de novos produtos](../content-design/widget-new-products-list.md), marque a caixa de seleção **[!UICONTROL Set Product as New]**.

1. Para atribuir _[!UICONTROL Categories]_&#x200B;ao produto, clique na caixa **[!UICONTROL Select…]**&#x200B;e siga um destes procedimentos:

   **Escolha uma categoria existente**:

   - Comece a digitar na caixa até encontrar uma correspondência.

   - Marque a caixa de seleção de cada categoria que deve ser atribuída.

   **Criar uma categoria**:

   - Clique em **[!UICONTROL New Category]**.

   - Insira o **[!UICONTROL Category Name]** e escolha o **[!UICONTROL Parent Category]**, que determina sua posição na [estrutura de menu](category-root.md).

   - Clique em **[!UICONTROL Create Category]**.

1. Defina **[!UICONTROL Format]** como um dos seguintes:

   - `Download`
   - `DVD`

   Se necessário, você pode editar o [atributo](attribute-product-create.md) para adicionar mais valores.

   Pode haver atributos adicionais que descrevam o produto. A seleção varia de acordo com o conjunto de atributos e você pode concluí-los posteriormente.

#### Atribuir fontes e quantidades ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

### Etapa 5: Preencha as informações baixáveis

Role para baixo, expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção _[!UICONTROL Downloadable Information]_&#x200B;e marque a caixa de seleção **[!UICONTROL Is this downloadable product?]**.

Quando habilitada, a seção _[!UICONTROL Downloadable Information]_&#x200B;tem duas partes. A primeira parte descreve cada link de download e a segunda parte descreve cada arquivo de amostra. O valor padrão para muitas dessas opções pode ser definido na [configuração](#configure-the-download-options).

![Informações para Download](./assets/product-downloadable-information.png){width="600" zoomable="yes"}

#### Complete os links

1. Na seção _[!UICONTROL Links]_, insira o **[!UICONTROL Title]**&#x200B;que deseja usar como cabeçalho para os links de download.

1. Se aplicável, marque a caixa de seleção **[!UICONTROL Links can be purchased separately]**.

1. Clique em **[!UICONTROL Add Link]** e faça o seguinte:

   - Insira os **[!UICONTROL Title]** e **[!UICONTROL Price]** do download.

   - Para os arquivos **[!UICONTROL File]** e **[!UICONTROL Sample]**, escolha um dos seguintes métodos de distribuição para os downloads:

      - `Upload File` - Escolha este método para carregar o arquivo de distribuição no servidor. Navegue até o arquivo e selecione-o para upload.
      - `URL` - Escolha este método para acessar o arquivo de distribuição de uma URL. Insira o URL completo para o arquivo de download.

   >[!NOTE]
   >
   >Não é possível usar links para recursos externos como produtos baixáveis. Domínios de link válidos são predefinidos programaticamente no arquivo `env.php` (consulte [env.php reference](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/files/config-reference-envphp.html) no _Guia de Configuração_).

   - Defina **[!UICONTROL Shareable]** como um dos seguintes:

      - `No` - Requer que os clientes façam logon em suas contas para acessar o link de download.

      - `Yes` - Envia o link por email, que os clientes podem compartilhar com outras pessoas.

      - `Use Config` - Usa o método especificado na configuração [Opções de Produto para Download](../configuration-reference/catalog/catalog.md).

   - Siga um destes procedimentos:

      - Para limitar os downloads por cliente, insira o número máximo de **[!UICONTROL Max. Downloads]**.
      - Para permitir downloads ilimitados, marque a caixa de seleção **[!UICONTROL Unlimited]**.

   ![Detalhes do link](./assets/product-downloadable-link-detail.png){width="600" zoomable="yes"}

1. Para adicionar outro link, clique em **[!UICONTROL Add Link]** e repita essas etapas.

#### Complete as amostras

1. Na seção _[!UICONTROL Samples]_, insira o **[!UICONTROL Title]**&#x200B;que você deseja usar como cabeçalho para as amostras.

1. Para completar as informações de cada amostra, clique em **[!UICONTROL Add Link]**.

   ![Amostras](./assets/product-downloadable-samples.png){width="600" zoomable="yes"}

1. Preencha os detalhes do link da seguinte maneira:

   - Insira o **[!UICONTROL Title]** da amostra individual.

   - Escolha um dos seguintes métodos de distribuição:

      - `Upload File` - Escolha este método para carregar o arquivo de distribuição no servidor. Navegue até o arquivo e selecione-o para upload.
      - `URL` - Escolha este método para acessar o arquivo de distribuição de uma URL. Insira o URL completo para o arquivo de download.

   - Para adicionar outra amostra, clique em **[!UICONTROL Add Link]** e repita essas etapas.

   - Para alterar a ordem das amostras, pegue o ícone _Ordem de alteração_ ( ![Controlador de posição](../assets/icon-sort-order.png) ) e arraste a amostra para uma nova posição.

### Etapa 6: Preencher as informações do produto

Role para baixo e preencha as informações nas seguintes seções, conforme necessário:

- [Conteúdo](product-content.md)
- [Imagens e vídeos](product-images-and-video.md)
- [Otimização do mecanismo de pesquisa](product-search-engine-optimization.md)
- [Produtos relacionados, venda adicional e venda cruzada](related-products-up-sells-cross-sells.md)
- [Opções personalizáveis](settings-advanced-custom-options.md)
- [Produtos em sites](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Opções de presente](product-gift-options.md)

### Etapa 7: publicar o produto

Se você estiver pronto para publicar o produto no catálogo, defina **[!UICONTROL Enable Product]** como `Yes` e siga um destes procedimentos:

**Método 1:** Salvar e Visualizar

- No canto superior direito, clique em **[!UICONTROL Save]**.

- Para exibir o produto em sua loja, escolha **[!UICONTROL Customer View]** no menu _Admin_ ( ![Seta de menu](../assets/icon-menu-down-arrow-black.png) ).

  A loja é aberta em uma nova guia do navegador.

  ![Visualização de Cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

**Método 2:** Salvar e Fechar

No menu _[!UICONTROL Save]_( ![Seta do menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), escolha **[!UICONTROL Save & Close]**.

## Experiência da vitrine

No painel da conta do cliente, a página _[!UICONTROL My Downloadable Products]_&#x200B;é vinculada a cada ordem de produtos baixáveis. Os downloads ficam disponíveis na conta do cliente quando o pedido é concluído.

![Meus Produtos Baixáveis](./assets/customer-account-my-downloadable-products.png){width="700" zoomable="yes"}

A tabela a seguir descreve os valores de _Meus Produtos para Download_:

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL Order#] | O [pedido](../stores-purchase/orders.md) no qual o produto baixável foi comprado. Fornece um link para os detalhes do pedido. |
| [!UICONTROL Date] | Data de criação do pedido. |
| [!UICONTROL Title] | O nome do produto para download adquirido com o pedido. Fornece um link para o produto que pode ser baixado. |
| [!UICONTROL Status] | Status de processamento do pedido. |
| [!UICONTROL Remaining Downloads] | Número de downloads disponíveis do produto baixado. |

_&#x200B;**Para baixar um arquivo de produto do painel de contas**&#x200B;_

1. No painel de conta, o cliente escolhe **[!UICONTROL My Downloadable Products]**.

1. Localiza a ordem na lista e clica no link após o título.

1. No canto inferior direito da janela de download, clique no ícone _download_.

1. Localiza o arquivo no local de downloads e o salva no local desejado.

<!-- Last updated from includes: 2023-05-19 17:14:58 -->
