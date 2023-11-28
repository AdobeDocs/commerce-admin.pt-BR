---
title: O URL da categoria substitui
description: Saiba como usar substituições de URL de categoria para redirecionar links para o URL de outra categoria na loja do Commerce.
exl-id: fc18f472-4aa8-4203-ade9-7ca576689d61
feature: Categories, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# O URL da categoria substitui

Se uma categoria for removida do catálogo, você poderá usar uma regravação de categoria para redirecionar links para o URL de outra categoria na loja. Pense em termos de _público alvo_ / _solicitação original_  ou _redirecionar para_ / _redirecionar de_. Embora as pessoas ainda possam navegar para a página anterior a partir de mecanismos de pesquisa ou links desatualizados, o redirecionamento faz com que sua loja alterne para o novo público-alvo.

Se [redirecionamentos automáticos](url-redirect-product-automatic.md) estão habilitados para sua loja, não há necessidade de criar uma regravação quando uma categoria [Chave do URL](../catalog/catalog-urls.md) foi alterado.

{{url-rewrite-skip}}

## Etapa 1. Planejar a reescrita

Para evitar erros, anote o _redirecionar para_ caminho e _redirecionar de_ e inclua a chave e o sufixo do URL (se aplicável).

Se não tiver certeza, abra cada página de categoria no armazenamento e copie o caminho da barra de endereços do navegador.

**Exemplo:**

Redirecionar para: `gear/backpacks-and-bags.html`

Redirecionar de: `gear/bags.html`

## Etapa 2. Criar a regravação

{{url-rewrite-params}}

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Antes de continuar, faça o seguinte para verificar se o caminho da solicitação está disponível:

   - No filtro de pesquisa, na parte superior da guia **[!UICONTROL Request Path]** insira a chave do URL da categoria que deve ser redirecionada e clique em **[!UICONTROL Search]**.

   - Se houver vários registros de redirecionamento para a página, localize aquele que corresponde à exibição de loja aplicável e abra o registro de redirecionamento no modo de edição.

   - No canto superior direito, clique em **[!UICONTROL Delete]**. Quando solicitado, clique em **[!UICONTROL OK]** para confirmar.

1. Quando você retornar ao _[!UICONTROL URL Rewrites]_clique em **[!UICONTROL Add URL Rewrite]**.

1. Definir **[!UICONTROL Create URL Rewrite]** para `For category` e escolha a categoria de público alvo na árvore que é o destino do redirecionamento.

   ![Reescrita de URL - escolha a categoria](./assets/url-rewrite-category-choose.png){width="700" zoomable="yes"}

1. No _Regravação de URL_ faça o seguinte:

   - Se você tiver vários armazenamentos, selecione o **[!UICONTROL Store]** onde a regravação se aplica.

   - Para **[!UICONTROL Request Path]**, insira a chave do URL da categoria que o cliente solicita. Este é o _redirecionar de_ categoria.

     >[!NOTE]
     >
     >O caminho da solicitação deve ser exclusivo para o armazenamento especificado. Se já houver um redirecionamento que use o mesmo caminho de solicitação, você receberá um erro ao tentar salvar o redirecionamento. O redirecionamento anterior precisa ser excluído para que você possa criar um.

   - Definir **[!UICONTROL Redirect]** a um dos seguintes:

      - `Temporary (302)`
      - `Permanent (301)`

   - Para sua referência, informe uma breve descrição da reescrita.

   ![Adicionar regravação de URL para categoria](./assets/url-rewrite-for-category.png){width="700" zoomable="yes"}

1. Antes de salvar o redirecionamento, revise o seguinte:

   - O link no canto superior esquerdo exibe o nome da categoria de público alvo.
   - O Caminho da solicitação contém o caminho para o original _redirecionar de_ categoria.

1. Quando terminar, clique em **[!UICONTROL Save]** botão.

   A nova regravação de categoria é exibida na parte superior da grade Regravações de URL.

## Etapa 3. Testar o resultado

1. Vá para a home page da loja.

1. Siga um destes procedimentos:

   - Navegar até o original _redirecionar de_ categoria.
   - Na barra de endereços do navegador, digite o caminho para o original _redirecionar de_ categoria imediatamente após o URL de armazenamento e pressione **[!UICONTROL Enter]**.

   A nova categoria de destino aparece em vez da solicitação de categoria original.

## Descrições dos campos

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Indica o tipo de reescrita. O tipo não pode ser alterado após a criação da regravação. Opções: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | A categoria a ser redirecionada. Dependendo da sua configuração, o caminho da solicitação pode incluir o sufixo .html ou .htm e a categoria principal. O caminho da solicitação deve ser exclusivo e não pode estar sendo usado por outro redirecionamento. Se você receber um erro de que o caminho da solicitação existe, exclua o redirecionamento existente e tente novamente. |
| [!UICONTROL Target Path] | O caminho interno usado pelo sistema para apontar para o destino do redirecionamento. O caminho de destino está esmaecido e não pode ser editado. |
| [!UICONTROL Redirect] | Determina o tipo de redirecionamento. Opções: <br/>**[!UICONTROL No]**- Nenhum redirecionamento especificado. Muitas operações criam solicitações de redirecionamento desse tipo. Por exemplo, toda vez que você adicionar produtos a uma categoria, um redirecionamento da variável `No` tipo é criado em cada exibição de loja.<br/>**[!UICONTROL Temporary (302)]** - Indica aos mecanismos de pesquisa que a regravação é por um tempo limitado. Os mecanismos de pesquisa geralmente não retêm informações de classificação de página para regravações temporárias. <br/>**[!UICONTROL Permanent (301)]**- Indica aos mecanismos de pesquisa que a regravação é permanente. Os mecanismos de pesquisa geralmente retêm informações de classificação de página para regravações permanentes. |
| [!UICONTROL Description] | Descreve a finalidade da regravação para referência interna. |

{style="table-layout:auto"}
