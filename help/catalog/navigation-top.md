---
title: Navegação superior
description: Saiba como definir o menu principal de uma loja que funciona como um diretório para os diferentes departamentos.
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%

---

# Navegação superior

O menu principal da loja é como um diretório para os diferentes departamentos da loja. Cada opção representa uma categoria diferente de produtos. A posição e a apresentação da navegação superior podem variar por tema, mas a forma como ela funciona é essencialmente a mesma.

![Navegação Superior](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

A estrutura de categorias do catálogo pode influenciar o desempenho do site ser indexado por mecanismos de pesquisa. Quanto mais aninhada uma categoria, menos provável ela será indexada completamente. Geralmente, usar entre um e três níveis visíveis é o mais eficaz. A [categoria raiz](category-root.md) conta como o primeiro nível, embora não apareça no menu. O número máximo de níveis disponíveis na navegação superior é determinado pela configuração. Além disso, pode haver um limite para o número de níveis de menu compatíveis com o tema da loja. Por exemplo, o tema Luma de amostra é compatível com até cinco níveis, incluindo a raiz.

## Contagem de níveis de menu

| Item | Descrição |
|--- |--- |
| Nível 1 | O primeiro nível é a categoria raiz, que nos dados de amostra é chamada de &quot;Categoria padrão&quot;. A raiz é um container para o menu e seu nome não aparece como uma opção no menu. |
| Nível 2 | Em uma tela de desktop, a navegação superior é o menu principal que aparece na parte superior da página. Em um dispositivo móvel, o menu principal normalmente é exibido como um menu suspenso de opções. As opções de segundo nível na loja Luma são _Novidades_, _Mulheres_, _Homens_, _Engrenagens_, _Treinamento_ e _Vendas_. |
| Nível 3 | O terceiro nível aparece abaixo de cada opção do menu principal. Por exemplo, em _Mulheres_, as opções de terceiro nível são _Tops_ e _Bottom_. |
| Nível 4 | As opções de quarto nível são subcategorias que saem de uma opção de terceiro nível. Por exemplo, em _Tops_, as opções de menu do quarto nível são _Jaquetas_, _Moletons e Sweatshirts_, _Tees_ e _Bras e Tanques_. |

{style="table-layout:auto"}

## Definir a navegação superior

Para que uma categoria seja exibida na navegação superior de uma loja, conclua as seguintes etapas:

### Etapa 1: criar uma categoria

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Defina um **[!UICONTROL Store View]** para determinar onde a nova categoria deverá estar disponível.

1. Na árvore de categorias, selecione a categoria principal da nova categoria.

   Se você estiver começando do início sem nenhum dado, pode haver apenas duas categorias na lista: _Categoria padrão_, que é a raiz, e uma _Categoria de exemplo_.

1. Clique em **[!UICONTROL Add Subcategory]**.

1. Preencha as informações básicas com as seguintes configurações:

   - **[!UICONTROL Enable Category]** definido como `Yes`
   - **[!UICONTROL Include in Menu]** definido como `Yes`

1. Na Configuração de Exibição definida de **[!UICONTROL Anchor]** a `Yes`.

1. Conclua quaisquer outras [configurações de categoria](category-create.md) necessárias.

1. Quando terminar, clique em **[!UICONTROL Save]**.

Para uma instalação multistore, um menu principal diferente pode ser atribuído como a [categoria raiz](category-root.md) para cada [loja](../stores-purchase/stores.md#add-stores).

### Etapa 2: definir a profundidade da navegação superior

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Expanda a seção **[!UICONTROL Category Top Navigation]**.

   ![Navegação Superior da Categoria](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   Como a profundidade da navegação superior tem um [escopo de configuração](../getting-started/websites-stores-views.md#scope-settings) global, a configuração se aplica a todos os sites, lojas e exibições de loja na instalação do Commerce. A seção de configuração _[!UICONTROL Category Top Navigation]_está disponível somente quando_[!UICONTROL Store View]_ no canto superior esquerdo está definido como `Default Config`.

   Para obter uma lista detalhada dessas opções, consulte [Navegação Superior da Categoria](../configuration-reference/catalog/catalog.md#layered-navigation) na _Referência de Configuração_.

1. Para limitar o número de subcategorias que aparecem na navegação superior, insira o número para **[!UICONTROL Maximal Depth]**.

   O valor padrão é `0`, que não coloca um limite no número de níveis de subcategoria.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
