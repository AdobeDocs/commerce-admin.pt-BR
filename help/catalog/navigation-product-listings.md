---
title: Listagens de produtos
description: Saiba como modificar a configuração da lista de produtos, que determina quantos produtos aparecem por página e qual atributo é usado para classificar a lista.
exl-id: 3779d9db-4adb-473b-b9c9-ad066f50b549
feature: Catalog Management, Products, Page Content
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Listagens de produtos

As listas de produtos podem ser definidas para serem exibidas por padrão como uma lista ou grade. Você também pode determinar quantos produtos aparecem por página e qual atributo é usado para classificar a lista. A lista de produtos inclui um conjunto de controles que podem ser usados para classificar os produtos, alterar o formato da lista, classificar por atributo e avançar de uma página para outra.

>[!NOTE]
>
>Ao classificar uma categoria por um atributo de produto, os produtos com os mesmos valores de atributo também são classificados por seus _[!UICONTROL Product ID]_na ordem crescente.

![Produtos exibidos como uma grade](./assets/storefront-catalog-page.png){width="700" zoomable="yes"}

## Configurar listas de produtos

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** por baixo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Storefront]** seção.

   ![Opções de configuração da vitrine eletrônica](../configuration-reference/catalog/assets/catalog-storefront.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada dessas opções, consulte [Loja](../configuration-reference/catalog/catalog.md#storefront) no _Referência de configuração_.

   >[!NOTE]
   >
   >Para exibir corretamente os produtos e seus preços de acordo com _classificação de produto por preço_, verifique se as configurações para a exibição do preço no [Configuração de imposto sobre vendas](../configuration-reference/sales/tax.md) têm o mesmo valor (`Excluding Tax` **ou** `Including Tax`). Para o _[!UICONTROL Calculation Settings]_, verifique a **[!UICONTROL Catalog Prices]**valor. E para_[!UICONTROL Price Display Settings]_, verifique a **[!UICONTROL Display Product Prices in Catalog]** valor. Se eles tiverem valores diferentes, os filtros de preço na navegação em camadas podem não filtrar e classificar corretamente os produtos por preço.

1. Definir o padrão **[!UICONTROL List Mode]** a um dos seguintes:

   - `Grid Only`
   - `List Only`
   - `Grid (default) / List`
   - `List (default / Grid`

1. Para **[!UICONTROL Products per Page on Grid Allowed Values]**, insira o número de produtos que você deseja que apareça por página quando mostrado no formato de grade.

   Para inserir uma seleção de valores, separe cada número por vírgula.

1. Para **[!UICONTROL Products per Page on Grid Default Value]**, insira o número padrão de produtos a serem exibidos na grade por página.

1. Para **[!UICONTROL Products per Page on List Allowed Values]**, digite o número de produtos que você deseja que apareçam por página quando exibidos no formato de lista.

   Para inserir uma seleção de valores, separe cada número por vírgula.

1. Para **[!UICONTROL Products per page on List Default Value]**, digite o número padrão de produtos exibidos na lista, por página.

1. Definir **[!UICONTROL Product Listing Sorted by]** ao atributo padrão usado inicialmente para classificar a lista.

1. Para dar aos clientes a opção de listar todos os produtos, defina **[!UICONTROL Allow All Products on Page]** para `Yes`.

1. Se quiser reter todas as configurações de paginação enquanto os clientes navegam pelas listagens do catálogo, defina **[!UICONTROL Remember Category Pagination]** para `Yes`.

   Ativar essa configuração garante que o número de produtos exibidos em uma lista ou grade seja retido à medida que os compradores navegam de uma categoria para outra. Por padrão, esse campo está definido como `No` porque ele usa mais armazenamento em cache e pode afetar a maneira como as páginas são indexadas por mecanismos de pesquisa.

1. Se estiver usando um [catálogo plano](catalog-flat.md) (**não recomendado**), faça o seguinte:

   - Para exibir uma lista de categorias simples de produtos, defina **[!UICONTROL Use Flat Catalog Category]** para `Yes`.

   - Para exibir uma lista de produtos simples, defina **[!UICONTROL Use Flat Catalog Product]** para `Yes`.

1. Se quiser permitir referências dinâmicas para ativos de mídia em URLs de categoria e produto, defina **[!UICONTROL Allow Dynamic Media URLs in Products and Categories]** para `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Controles de página

| Controle | Descrição |
|--- |--- |
| [!UICONTROL View As] | Exibe os produtos no formato de grade ou lista. |
| [!UICONTROL Sort By] | Altera a ordem de classificação da lista. |
| [!UICONTROL Show Per Page] | Determina quantos produtos são exibidos por página. |
| Links de paginação | Links para outras páginas. |

{style="table-layout:auto"}

## Controles de paginação

As Configurações de paginação são exibidas nas partes superior e inferior da lista e controlam o formato dos links de paginação para as listagens de produtos. Você pode definir o número de links que aparecem no controle e configurar os links Next e Previous. Para que os links de paginação apareçam, deve haver mais produtos na lista do que o permitido por página na configuração da lista de produtos.

![Controles de paginação](./assets/storefront-pagination-controls.png){width="700" zoomable="yes"}

### Controles de paginação de vitrine eletrônica

| Controle | Descrição |
|--- |--- |
| ![Exibir grade](./assets/controls-pagination-list-grid.png) | [!UICONTROL View As] - Exibe a lista no formato Grade ou Lista. |
| ![Classificar por](./assets/control-pagination-sort-by.png) | [!UICONTROL Sort By] - Altera a ordem de classificação da lista. A variável _[!UICONTROL Used for Sorting in Product Listing]_a propriedade storefront determina qual [atributos do produto](../catalog/product-attributes.md) para classificar a lista. |
| ![Mostrar por página](./assets/control-pagination-show-per-page.png) | [!UICONTROL Show Per Page] - Determina quantos produtos são exibidos por página. |
| ![Links de paginação](./assets/control-pagination.png) | Links de paginação - Links de navegação para outras páginas. |

{style="table-layout:auto"}

### Configurar os controles de paginação

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Localize a exibição de loja que você deseja configurar e, na caixa **[!UICONTROL Action]** clique em **[!UICONTROL Edit]**.

1. Em **[!UICONTROL Other Settings]**, expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Pagination]** seção.

   ![Paginação](./assets/config-design-pagination.png){width="600" zoomable="yes"}

   Para obter mais informações sobre essas configurações, consulte [Configuração de design](../content-design/configuration.md).

1. Para **[!UICONTROL Pagination Frame]**, insira o número de links que devem aparecer no controle de paginação.

1. Para **[!UICONTROL Pagination Frame Skip]**, digite o número de links que deseja pular antes de exibir o próximo conjunto de links no controle de paginação.

   Por exemplo, se o quadro de paginação tiver cinco links e você quiser ir para os próximos cinco links, quantos links deseja pular adiante? Se você definir o valor como quatro (`4`), o último link do conjunto anterior é o primeiro link do próximo conjunto.

1. Para **[!UICONTROL Anchor Text for Previous]**, insira o texto que deseja exibir para o link Anterior.

   Deixe em branco para utilizar a seta padrão.

1. Para **[!UICONTROL Anchor Text for Next]**, insira o texto que deseja exibir para o link Próximo. Deixe em branco para utilizar a seta padrão.

1. Quando terminar, clique em **[!UICONTROL Save Configuration]**.
