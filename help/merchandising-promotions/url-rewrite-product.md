---
title: Substituições de URL do produto
description: Saiba como usar substituições de URL de produto para redirecionar links para o URL de outro produto na loja da Commerce.
exl-id: 42b28ff7-e148-44f2-b6b4-63a38458e752
feature: Products, Configuration
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# Substituições de URL do produto

Antes de começar, verifique se você entende exatamente o que o redirecionamento deve realizar. Pense em termos de _destino_ / _solicitação original_ ou _redirecionar para_ / _redirecionar de_. Embora as pessoas ainda possam navegar para a página anterior a partir de mecanismos de pesquisa ou links desatualizados, o redirecionamento faz com que sua loja alterne para o novo público-alvo.

Se os [redirecionamentos automáticos](url-redirect-product-automatic.md) estiverem habilitados para sua loja, não será necessário criar uma regravação quando a [Chave da URL](../catalog/catalog-urls.md) do produto for alterada.

{{url-rewrite-skip}}

## Etapa 1. Planejar a reescrita

Para evitar erros, anote o caminho _redirecionar para_ e o caminho _redirecionar de_ e inclua a chave e o sufixo da URL (se aplicável).

Caso não tenha certeza, abra cada página de produto da loja e copie o caminho da barra de endereços do navegador. Ao criar um redirecionamento de produto, você pode incluir ou excluir o [caminho da categoria](../catalog/catalog-urls.md). Neste exemplo, criamos um redirecionamento de produto sem um caminho de categoria.

### Produto com caminho de categoria

Redirecionar para: `gear/bags/impulse-duffle.html`

Redirecionar de: `gear/bags/overnight-duffle.html`

### Produto sem caminho de categoria

Redirecionar para: `impulse-duffle.html`

Redirecionar de: `overnight-duffle.html`

## Etapa 2. Criar a regravação

{{url-rewrite-params}}

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Antes de continuar, faça o seguinte para verificar se o caminho da solicitação está disponível.

   - No filtro de pesquisa na parte superior da coluna **[!UICONTROL Request Path]**, digite a chave da URL da página a ser redirecionada e clique em **[!UICONTROL Search]**.

   - Se houver vários registros de redirecionamento para a página, localize aquele que corresponde à exibição de loja aplicável e abra-o no modo de edição.

   - No canto superior direito, clique em **[!UICONTROL Delete]**. Quando solicitado, clique em **[!UICONTROL OK]** para confirmar.

1. No canto superior direito da página Regravações de URL, clique em **Adicionar regravação de URL**.

1. Defina **[!UICONTROL Create URL Rewrite]** como `For product`.

1. Na grade, localize o produto que é o destino (destino) do redirecionamento e clique na linha.

   ![substituições de URL - produto](./assets/url-rewrite-product.png){width="700" zoomable="yes"}

1. Abaixo da árvore de categorias, clique em **[!UICONTROL Skip Category Selection]**.

   Neste exemplo, o redirecionamento não inclui uma categoria.

   ![Reescrita da URL do produto - ignorar seleção de categoria](./assets/url-rewrite-skip-category-selection.png){width="600" zoomable="yes"}

   A página Adicionar regravação de URL para um produto exibe um link para o destino no canto superior esquerdo, e o campo Caminho de destino exibe a versão do sistema do caminho, que não pode ser alterada. Inicialmente, o campo Caminho de redirecionamento também exibe o caminho de destino.

   - Se você tiver várias exibições de armazenamento, defina **[!UICONTROL Store]** como a exibição à qual a regravação se aplica. Caso contrário, uma regravação será criada para cada exibição.

   - Para **[!UICONTROL Request Path]**, substitua o padrão inserindo a chave e o sufixo (se aplicável) da URL da solicitação do produto original. Este é o _redirecionamento do_ produto que você identificou na etapa de planejamento.

     >[!NOTE]
     >
     >O caminho da solicitação deve ser exclusivo para o armazenamento especificado. Se já houver um redirecionamento que use o mesmo caminho de solicitação, você receberá um erro ao tentar salvar o redirecionamento. O redirecionamento anterior precisa ser excluído para que você possa criar um.

   - Defina **[!UICONTROL Redirect Type]** como um dos seguintes:

      - `Temporary (302)`
      - `Permanent (301)`

   - Para sua própria referência, insira um breve **[!UICONTROL Description]** da regravação.

   ![Reescrita da URL do produto - informações](./assets/url-rewrite-product-permanent-301.png){width="600" zoomable="yes"}

1. Antes de salvar o redirecionamento, revise o seguinte:

   - O link no canto superior esquerdo exibe o nome do produto de destino.
   - O Caminho da Solicitação contém o caminho para o produto _redirecionamento_ original.

1. Quando terminar, clique em **[!UICONTROL Save]**.

   A nova regravação do produto agora é exibida na parte superior da grade Regravações de URL.

## Etapa 3. Testar o resultado

1. Vá para a home page da loja.

1. Siga um destes procedimentos:

   - Navegue até a página original de solicitação de produto _redirecionar de_.
   - Na barra de endereços do navegador, digite o caminho para o produto _redirecionar de_ original imediatamente após a URL da loja e pressione **Enter**.

   O novo produto de destino é exibido em vez da solicitação do produto original.

## Descrições dos campos

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Indica o tipo de reescrita. O tipo não pode ser alterado após a criação da regravação. Opções: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | O produto a ser redirecionado. Dependendo da sua configuração, o Caminho da Solicitação pode incluir o sufixo `.html` ou `.htm` e a categoria. O Caminho da solicitação deve ser exclusivo e não pode estar sendo usado por outro redirecionamento. Se você receber um erro de que o Caminho da solicitação existe, exclua o redirecionamento existente e tente novamente. |
| [!UICONTROL Target Path] | O caminho interno usado pelo sistema para apontar para o destino do redirecionamento. O caminho de destino está esmaecido e não pode ser editado. |
| [!UICONTROL Redirect] | Determina o tipo de redirecionamento. Opções: <br/>**[!UICONTROL No]**- Nenhum redirecionamento especificado. Muitas operações criam solicitações de redirecionamento desse tipo. Por exemplo, toda vez que você adiciona produtos a uma categoria, um redirecionamento do tipo `No` é criado em cada exibição da loja.<br/>**[!UICONTROL Temporary (302)]** - Indica aos mecanismos de pesquisa que a regravação é por um tempo limitado. Os mecanismos de pesquisa geralmente não retêm informações de classificação de página para regravações temporárias. <br/>**[!UICONTROL Permanent (301)]**- Indica aos mecanismos de pesquisa que a regravação é permanente. Os mecanismos de pesquisa geralmente retêm informações de classificação de página para regravações permanentes. |
| [!UICONTROL Description] | Descreve a finalidade da regravação para referência interna. |

{style="table-layout:auto"}

## Várias substituições de URL

Você pode atualizar rapidamente substituições de URL para vários ou todos os produtos simultaneamente usando as etapas a seguir.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecione todos os produtos para os quais deseja atualizar regravações de URL.

1. Em _[!UICONTROL Actions]_, escolha **[!UICONTROL Update attributes]**&#x200B;para atualizar várias ou todas as regravações.

1. Em _[!UICONTROL PRODUCTS INFORMATION]_, clique na guia **[!UICONTROL Websites]**.

1. Na seção _[!UICONTROL Add Product To Websites]_, selecione todos os sites para os quais deseja restaurar regravações de URL.

1. Quando estiver pronto para atualizar, clique em **[!UICONTROL Save]**.

>[!NOTE]
>
>Todos os produtos selecionados são lidos nos sites selecionados e as regravações de URL são geradas novamente.

![Atualizar Atributos - atualizar várias regravações de URL](./assets/url-rewrites-update.png){width="600" zoomable="yes"}
