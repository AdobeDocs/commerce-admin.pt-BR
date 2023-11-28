---
title: Substituições de URL do produto
description: Saiba como usar substituições de URL de produto para redirecionar links para o URL de outro produto na sua loja de Commerce.
exl-id: 42b28ff7-e148-44f2-b6b4-63a38458e752
feature: Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 0%

---

# Substituições de URL do produto

Antes de começar, verifique se você entende exatamente o que o redirecionamento deve realizar. Pense em termos de _público alvo_ / _solicitação original_ ou _redirecionar para_ / _redirecionar de_. Embora as pessoas ainda possam navegar para a página anterior a partir de mecanismos de pesquisa ou links desatualizados, o redirecionamento faz com que sua loja alterne para o novo público-alvo.

Se [redirecionamentos automáticos](url-redirect-product-automatic.md) são ativados para sua loja, não há necessidade de criar uma regravação quando um produto [Chave do URL](../catalog/catalog-urls.md) foi alterado.

{{url-rewrite-skip}}

## Etapa 1. Planejar a reescrita

Para evitar erros, anote o _redirecionar para_ caminho e _redirecionar de_ e inclua a chave e o sufixo do URL (se aplicável).

Caso não tenha certeza, abra cada página de produto da loja e copie o caminho da barra de endereços do navegador. Ao criar um redirecionamento de produto, você pode incluir ou excluir o [caminho da categoria](../catalog/catalog-urls.md). Neste exemplo, criamos um redirecionamento de produto sem um caminho de categoria.

### Produto com caminho de categoria

Redirecionar para: `gear/bags/impulse-duffle.html`

Redirecionar de: `gear/bags/overnight-duffle.html`

### Produto sem caminho de categoria

Redirecionar para: `impulse-duffle.html`

Redirecionar de: `overnight-duffle.html`

## Etapa 2. Criar a regravação

{{url-rewrite-params}}

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Antes de continuar, faça o seguinte para verificar se o caminho da solicitação está disponível.

   - No filtro de pesquisa, na parte superior da guia **[!UICONTROL Request Path]** insira a chave de URL da página a ser redirecionada e clique em **[!UICONTROL Search]**.

   - Se houver vários registros de redirecionamento para a página, localize aquele que corresponde à exibição de loja aplicável e abra-o no modo de edição.

   - No canto superior direito, clique em **[!UICONTROL Delete]**. Quando solicitado, clique em **[!UICONTROL OK]** para confirmar.

1. No canto superior direito da página Regravações de URL, clique em **Adicionar regravação de URL**.

1. Definir **[!UICONTROL Create URL Rewrite]** para `For product`.

1. Na grade, localize o produto que é o destino (destino) do redirecionamento e clique na linha.

   ![Substituições de URL - produto](./assets/url-rewrite-product.png){width="700" zoomable="yes"}

1. Abaixo da árvore de categorias, clique em **[!UICONTROL Skip Category Selection]**.

   Neste exemplo, o redirecionamento não inclui uma categoria.

   ![Regravação de URL do produto - ignorar seleção de categoria](./assets/url-rewrite-skip-category-selection.png){width="600" zoomable="yes"}

   A página Adicionar regravação de URL para um produto exibe um link para o destino no canto superior esquerdo, e o campo Caminho de destino exibe a versão do sistema do caminho, que não pode ser alterada. Inicialmente, o campo Caminho de redirecionamento também exibe o caminho de destino.

   - Se você tiver várias exibições de loja, defina **[!UICONTROL Store]** à exibição em que a regravação se aplica. Caso contrário, uma regravação será criada para cada exibição.

   - Para **[!UICONTROL Request Path]**, substitua o padrão inserindo a chave e o sufixo do URL (se aplicável) da solicitação do produto original. Este é o _redirecionar de_ produto identificado na etapa de planejamento.

     >[!NOTE]
     >
     >O caminho da solicitação deve ser exclusivo para o armazenamento especificado. Se já houver um redirecionamento que use o mesmo caminho de solicitação, você receberá um erro ao tentar salvar o redirecionamento. O redirecionamento anterior precisa ser excluído para que você possa criar um.

   - Definir **[!UICONTROL Redirect Type]** a um dos seguintes:

      - `Temporary (302)`
      - `Permanent (301)`

   - Para sua própria referência, insira um resumo **[!UICONTROL Description]** da reescrita.

   ![Reescrita do URL do produto - informações](./assets/url-rewrite-product-permanent-301.png){width="600" zoomable="yes"}

1. Antes de salvar o redirecionamento, revise o seguinte:

   - O link no canto superior esquerdo exibe o nome do produto de destino.
   - O Caminho da solicitação contém o caminho para o original _redirecionar de_ produto.

1. Quando terminar, clique em **[!UICONTROL Save]**.

   A nova regravação do produto agora é exibida na parte superior da grade Regravações de URL.

## Etapa 3. Testar o resultado

1. Vá para a home page da loja.

1. Siga um destes procedimentos:

   - Navegar até o original _redirecionar de_ página de solicitação do produto.
   - Na barra de endereços do navegador, digite o caminho para o original _redirecionar de_ produto imediatamente após o URL da loja e pressione **Enter**.

   O novo produto de destino é exibido em vez da solicitação do produto original.

## Descrições dos campos

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Indica o tipo de reescrita. O tipo não pode ser alterado após a criação da regravação. Opções: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | O produto a ser redirecionado. Dependendo da sua configuração, o Caminho da solicitação pode incluir a variável `.html` ou `.htm` sufixo e categoria. O Caminho da solicitação deve ser exclusivo e não pode estar sendo usado por outro redirecionamento. Se você receber um erro de que o Caminho da solicitação existe, exclua o redirecionamento existente e tente novamente. |
| [!UICONTROL Target Path] | O caminho interno usado pelo sistema para apontar para o destino do redirecionamento. O caminho de destino está esmaecido e não pode ser editado. |
| [!UICONTROL Redirect] | Determina o tipo de redirecionamento. Opções: <br/>**[!UICONTROL No]**- Nenhum redirecionamento especificado. Muitas operações criam solicitações de redirecionamento desse tipo. Por exemplo, toda vez que você adicionar produtos a uma categoria, um redirecionamento da variável `No` tipo é criado em cada exibição de loja.<br/>**[!UICONTROL Temporary (302)]** - Indica aos mecanismos de pesquisa que a regravação é por um tempo limitado. Os mecanismos de pesquisa geralmente não retêm informações de classificação de página para regravações temporárias. <br/>**[!UICONTROL Permanent (301)]**- Indica aos mecanismos de pesquisa que a regravação é permanente. Os mecanismos de pesquisa geralmente retêm informações de classificação de página para regravações permanentes. |
| [!UICONTROL Description] | Descreve a finalidade da regravação para referência interna. |

{style="table-layout:auto"}

## Várias substituições de URL

Você pode atualizar rapidamente substituições de URL para vários ou todos os produtos simultaneamente usando as etapas a seguir.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecione todos os produtos para os quais deseja atualizar regravações de URL.

1. Em _[!UICONTROL Actions]_, escolha **[!UICONTROL Update attributes]**para atualizar várias ou todas as regravações.

1. Em _[!UICONTROL PRODUCTS INFORMATION]_, clique no link **[!UICONTROL Websites]**guia.

1. No _[!UICONTROL Add Product To Websites]_selecione todos os sites para os quais deseja restaurar regravações de URL.

1. Quando estiver pronto para atualizar, clique em **[!UICONTROL Save]**.

>[!NOTE]
>
>Todos os produtos selecionados são lidos nos sites selecionados e as regravações de URL são geradas novamente.

![Atualizar atributos - atualizar várias regravações de URL](./assets/url-rewrites-update.png){width="600" zoomable="yes"}
