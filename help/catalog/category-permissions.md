---
title: Permissões de categoria
description: Saiba como usar categorias para controlar a exibição de preços de produtos, determinar quais grupos de clientes podem adicionar produtos ao carrinho e especificar a página inicial.
exl-id: d80a0545-918e-4c08-9f37-4aa3cd7771f4
feature: Catalog Management, Categories, Customers, Configuration
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 0%

---

# Permissões de categoria

{{ee-feature}}

O acesso à categoria pode ser limitado a grupos específicos de clientes ou totalmente restrito. Você pode controlar a exibição de preços de produtos, determinar quais grupos de clientes podem adicionar produtos ao carrinho e especificar a página inicial.

>[!NOTE]
>
>As Permissões de categoria têm um escopo global e, quando habilitadas, restringem o acesso a cada categoria de acordo com suas permissões individuais. Por padrão, as Permissões de categoria não estão habilitadas.

Por exemplo, se você vender somente para clientes grossistas, poderá permitir que qualquer pessoa navegue no catálogo, mas exibir os preços e permitir compras somente para compradores do grupo de clientes _Atacado_. No exemplo a seguir, somente os usuários conectados têm acesso à categoria &quot;Coleções&quot;. Para convidados, a opção &quot;Coleções&quot; não aparece no menu principal.

![Usuários conectados veem a categoria &quot;Coleções&quot;](./assets/storefront-category-permissions-logged-in.png){width="600" zoomable="yes"}

Quando habilitada, uma nova seção _[!UICONTROL Category Permissions]_&#x200B;é exibida na página Categoria, permitindo que você aplique o acesso necessário para cada categoria. Você pode adicionar várias regras de permissão a cada categoria para sites e grupos de clientes diferentes.

## Etapa 1: configurar permissões de categoria

>[!IMPORTANT]
>
>Todas as [configurações de permissão de grupo](../configuration-reference/catalog/catalog.md#category-permissions) existentes são ignoradas por **_todas_** categorias no catálogo quando o recurso **_[!UICONTROL Shared Catalog]_** está habilitado. [!UICONTROL Shared Catalog] controla totalmente todas as permissões de categoria no catálogo quando ele é habilitado.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Category Permissions]**.

   ![Permissões de Categoria](../configuration-reference/catalog/assets/catalog-category-permissions.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada dessas opções, consulte [Permissões de Categoria](../configuration-reference/catalog/catalog.md#category-permissions) na _Referência de Configuração_.

1. Defina **[!UICONTROL Enable]** como `Yes`.

1. Complete as outras opções de acordo com o que deseja permitir ou restringir na loja (consulte as seções a seguir).

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Quando solicitado a atualizar o cache, clique no link **[!UICONTROL Cache Management]** na mensagem do sistema e siga as instruções para atualizar o cache.

### [!UICONTROL Allow Browsing Category]

Esta opção se aplica a todas as categorias no [site](../getting-started/websites-stores-views.md).

Para permitir que membros de um **_grupo de clientes específico_** naveguem pelos produtos da categoria, faça o seguinte:

1. Defina **[!UICONTROL Allow Browsing Category]** como `Specified Customer Groups`.

1. Na caixa **[!UICONTROL Customer Groups]**, selecione cada grupo que tem permissão para navegar pelos produtos da categoria.

   Para selecionar vários grupos, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) enquanto clica em cada grupo.

   ![Permitir Navegação por Grupo de Clientes Atacados](./assets/category-permissions-allow-browsing-customer-groups.png){width="600" zoomable="yes"}

Para **_restringir o acesso e redirecionar para uma página de aterrissagem_**, faça o seguinte:

1. Defina **[!UICONTROL Allow Browsing Category]** como `No, Redirect to Landing Page`.

1. Escolha a **[!UICONTROL Landing Page]** para onde os visitantes são redirecionados.

   ![Redirecionar para a Página Inicial](./assets/category-permissions-browse-category-landing-page.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Embora a configuração _[!UICONTROL Allow Browsing Category]_&#x200B;se aplique a todas as categorias do site, você pode configurar uma página de aterrissagem diferente para cada exibição de loja.

### [!UICONTROL Display Product Prices]

Esta opção se aplica a todas as categorias no [site](../getting-started/websites-stores-views.md).

Para permitir que somente membros de **_grupos de clientes específicos_** vejam o preço dos produtos na categoria, faça o seguinte:

1. Defina **[!UICONTROL Display Product Prices]** como `Yes, for Specified Customer Groups`.

1. Na caixa **[!UICONTROL Customer Groups]**, selecione cada grupo que tem permissão para ver o preço dos produtos na categoria.

   Para selecionar vários grupos, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) enquanto clica em cada grupo.

   ![Somente o grupo de clientes de atacado pode visualizar os preços](./assets/category-permissions-price-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Allow Adding to Cart]

Esta opção se aplica a todas as categorias no [site](../getting-started/websites-stores-views.md).

Para permitir que apenas membros de **_grupos de clientes específicos_** coloquem produtos de categoria no carrinho de compras, faça o seguinte:

1. Defina **[!UICONTROL Allow Adding to Cart]** como `Yes, for Specified Customer Groups`.

1. Na caixa **[!UICONTROL Customer Groups]**, selecione cada grupo que tem permissão para adicionar produtos da categoria ao carrinho.

   Para selecionar vários grupos, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) enquanto clica em cada grupo.

   ![Somente o grupo de clientes de atacado pode colocar o produto no carrinho](./assets/category-permissions-cart-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Disallow Catalog Search]

Defina esta opção para impedir que os membros de um grupo de clientes específico usem a Pesquisa no catálogo. Aplica-se a todas as categorias no [site](../getting-started/websites-stores-views.md).

- Para permitir que apenas **_clientes conectados_** usem a Pesquisa no Catálogo, selecione `NOT LOGGED IN`.

- Para permitir que **_apenas grupos de clientes específicos_** usem a Pesquisa no Catálogo, selecione cada grupo a ser excluído de usar a Pesquisa na Categoria.

  Para selecionar vários grupos, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) enquanto clica em cada grupo.

  ![Pesquisa de catálogo não permitida para o grupo geral de clientes](./assets/category-permissions-disallow-category-search.png){width="600" zoomable="yes"}

## Etapa 2: Aplicar permissões de categoria

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Na árvore de categorias, selecione a categoria de destino.

1. Expanda o ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Category Permissions]** na página e faça o seguinte:

   - Para criar uma regra de permissões, clique em **[!UICONTROL New Permission]**.

     ![Seção de Permissões de Categoria](./assets/category-permissions-section-admin.png){width="600" zoomable="yes"}

   - Escolha os **[!UICONTROL Website]** e **[!UICONTROL Customer Group]** aplicáveis.

   - Defina as permissões individuais conforme necessário.

   >[!NOTE]
   >
   >Quando a permissão `Browsing Category` = `Deny` é definida para qualquer categoria pai, ela não é exibida na [Trilha da Navegação Estrutural](navigation-breadcrumb-trail.md) na página de categoria filho.

1. Quando terminar, clique em **[!UICONTROL Save]**.

>[!NOTE]
>
>Se qualquer permissão **_Permitir_** estiver definida para `Root Category`, essas permissões serão automaticamente aplicadas a todas as subcategorias e todos os produtos dentro de `Catalog`. Se algum produto for atribuído a várias categorias e tiver qualquer permissão **_Permitir_** para pelo menos uma categoria, ele terá automaticamente as mesmas permissões **_Permitir_** para todas as categorias atribuídas.
