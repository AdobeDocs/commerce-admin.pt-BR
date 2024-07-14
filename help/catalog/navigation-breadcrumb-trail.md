---
title: Trilhas da navegação estrutural
description: Saiba mais sobre os diferentes padrões de trilha de navegação estrutural e como configurá-los para aparecer nas páginas de conteúdo e catálogo.
exl-id: 2f60d48e-960f-437c-8f8f-a3d06cc0840a
feature: Catalog Management, Categories, Site Navigation, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Trilhas da navegação estrutural

Uma _trilha de navegação estrutural_ é um conjunto de links que mostra ao cliente onde eles estão em relação a outras páginas na loja. Eles podem clicar em qualquer link na trilha de navegação estrutural para retornar à página anterior.

A trilha de navegação estrutural pode ser configurada para aparecer nas páginas de conteúdo e nas páginas do catálogo. O formato e a posição da trilha de navegação estrutural variam de acordo com o tema, mas normalmente ficam logo abaixo do cabeçalho. Por padrão, a trilha de navegação estrutural aparece nas páginas CMS.

![Trilha de navegação estrutural exibida na loja](./assets/storefront-breadcrumb-trail.png){width="700" zoomable="yes"}

## Tipos gerais de migalhas de pão

As navegações estruturais podem ser divididas em três tipos principais, que diferem em sua finalidade. A essência e os principais princípios da implementação de cada tipo de migalha de pão são descritos abaixo.

### Navegação estrutural baseada em hierarquia

Esse tipo de navegação estrutural se baseia na hierarquia de categoria configurada no site. As correntes apresentadas informam ao usuário onde estão na estrutura. Nesse caso, cada link de texto se destina a uma página que está um nível acima do anterior.

Exemplo: `Men > Tops > Hoodies & Sweatshirts`

A vantagem desse tipo é que os usuários podem ver facilmente em qual nível de categoria estão e ter fácil acesso à navegação entre páginas de catálogo.

### Navegação estrutural baseada no histórico

A navegação baseada em histórico (ou caminho) é semelhante ao botão Voltar em um navegador. Esse tipo de navegação permite que os usuários retornem rapidamente às páginas anteriores visitadas sem alterações.

A vantagem desse tipo é que ele é mais útil quando os clientes desejam retornar a uma página anterior depois de selecionar vários filtros em uma página de categoria.

Exemplo: `Home > What's New > Gear > Bags`

### Navegação estrutural baseada em atributo

Esse tipo de navegação estrutural exibe os atributos selecionados na página de categoria. A principal diferença em relação aos outros tipos é que a navegação estrutural baseada em atributos representa os filtros e as opções que o cliente selecionou na camada de navegação para determinados produtos (como preço, qualidade e cor).

Exemplo: `Home > Suits > All Suits > Refined by > Slim Fit`

## Adicionar/Remover as navegações estruturais das páginas CMS

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Web]**.

   ![Mostrar navegações estruturais para páginas CMS](../configuration-reference/general/assets/web-default-pages.png){width="600" zoomable="yes"}

1. Expanda a seção _[!UICONTROL Default Pages]_.

1. Desmarque a caixa de seleção **[!UICONTROL Use system value]**.

1. Defina **[!UICONTROL Show Breadcrumbs for CMS Pages]** como `No` ou `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

>[!NOTE]
>
>A categoria principal não é exibida na Trilha da Navegação Estrutural, na página de categoria secundária, quando tem configurações de `Browsing Category`= `Deny` [permissão de categoria](category-permissions.md).
