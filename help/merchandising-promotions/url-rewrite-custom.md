---
title: Substituições de URL personalizadas
description: Saiba como usar substituições de URL personalizadas para gerenciar redirecionamentos diversos na loja do Commerce.
exl-id: b15054be-e463-48e6-b6c1-0a8a2141cc01
feature: Search, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Substituições de URL personalizadas

Uma regravação personalizada pode ser usada para gerenciar redirecionamentos diversos, como o redirecionamento de uma página da sua loja para um site externo. Por exemplo, você pode ter dois sites do Commerce, cada um com seu próprio domínio. Você pode usar um redirecionamento personalizado para redirecionar solicitações de um produto, categoria ou página para outro site. Ao contrário de outros tipos de redirecionamento, o destino de um redirecionamento personalizado não é escolhido em uma lista de páginas existentes na loja.

Antes de começar, verifique se você entende exatamente o que o redirecionamento deve realizar. Pense em termos de _público alvo_ / _origem_ ou _redirecionar para_ / _redirecionar de_. Embora as pessoas ainda possam navegar para a página anterior a partir de mecanismos de pesquisa ou links desatualizados, o redirecionamento faz com que sua loja alterne para o novo público-alvo.

## Etapa 1. Planejar a reescrita

Para evitar erros, anote o URL do _redirecionar para_ e a chave de URL da _redirecionar de_ página.

Caso não tenha certeza, abra cada página e copie o URL da barra de endereços do seu navegador.

**Exemplo**

Redirecionar para:

    http://www.different-website.com/page.html

Redirecionar de:

    cms-page
    category.html
    category/subcategory.html
    product.html
    category/product.html

## Etapa 2. Criar a regravação

{{url-rewrite-params}}

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Antes de continuar, faça o seguinte para verificar se o caminho da solicitação está disponível:

   - No filtro de pesquisa, na parte superior da guia **[!UICONTROL Request Path]** insira a chave do URL da página que deve ser redirecionada e clique em **[!UICONTROL Search]**.

   - Se houver vários registros de redirecionamento para a página, localize aquele que corresponde à exibição de loja aplicável e abra-o no modo de edição.

   - No canto superior direito, clique em **[!UICONTROL Delete]**. Quando solicitado, clique em **[!UICONTROL OK]** para confirmar.

1. Ao retornar para a página Regravações de URL, clique em **[!UICONTROL Add URL Rewrite]**.

1. Definir **[!UICONTROL Create URL Rewrite]** para `Custom`.

   ![Substituições de URL - personalizadas](./assets/url-rewrite-custom.png){width="600" zoomable="yes"}

1. Em Informações de regravação de URL, faça o seguinte:

   - Se você tiver várias exibições de loja, selecione a variável **[!UICONTROL Store]** onde a regravação se aplica.

   - Para **[!UICONTROL Request Path]**, insira a chave e o caminho do URL, se aplicável, do produto, categoria ou página do CMS que deve ser redirecionado.

     >[!NOTE]
     >
     >O caminho da solicitação deve ser exclusivo para o armazenamento especificado. Se já houver um redirecionamento que use o mesmo caminho de solicitação, você receberá um erro ao tentar salvar o redirecionamento. O redirecionamento anterior precisa ser excluído para que você possa criar um.

   - Para **[!UICONTROL Target Path]**, insira o URL do destino. Se o público-alvo estiver em outro site, insira o URL totalmente qualificado.

   - Definir **Redirecionar** a um dos seguintes:

      - `Temporary (302)`
      - `Permanent (301)`

   - Para sua referência, informe uma breve descrição da reescrita.

1. Antes de salvar o redirecionamento, revise o seguinte:

   - A variável [!UICONTROL Request Path] contém a chave ou o caminho do URL do original _redirecionar de_ página.
   - A variável [!UICONTROL Target Path] contém o URL do _redirecionar para_ página.

1. Quando terminar, clique em **[!UICONTROL Save]**.

   A nova regravação aparece na grade na parte superior da lista.

## Etapa 3. Testar o resultado

1. Vá para a home page da loja.

1. Siga um destes procedimentos:

   - Navegar até o original _redirecionar de_ página.
   - Na barra de endereços do navegador, digite o nome do original _redirecionar de_ imediatamente após o URL de armazenamento e pressione **Enter**.

   A nova página de destino é exibida em vez da solicitação da página original.

## Descrições dos campos

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Indica o tipo de reescrita. O tipo não pode ser alterado após a criação da regravação. Opções: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | A página que deve ser redirecionada. O caminho da solicitação deve ser exclusivo e não pode estar sendo usado por outro redirecionamento. Se você receber uma mensagem de erro informando que o caminho da solicitação existe, exclua o redirecionamento existente e tente novamente. |
| [!UICONTROL Target Path] | O caminho interno usado pelo sistema para apontar para o destino. O caminho de destino está esmaecido e não pode ser editado. |
| [!UICONTROL Redirect] | Determina o tipo de redirecionamento. Opções: <br/>**Não** - Nenhum redirecionamento especificado. <br/>**[!UICONTROL Temporary (302)]**- Indica aos mecanismos de pesquisa que a regravação é por um tempo limitado. Os mecanismos de pesquisa geralmente não retêm informações de classificação de página para regravações temporárias.<br/>**[!UICONTROL Permanent (301)]** - Indica aos mecanismos de pesquisa que a regravação é permanente. Os mecanismos de pesquisa geralmente retêm informações de classificação de página para regravações permanentes. |
| [!UICONTROL Description] | Descreve a finalidade da regravação para referência interna. |

{style="table-layout:auto"}
