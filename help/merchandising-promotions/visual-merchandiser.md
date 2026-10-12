---
title: Visão geral do Visual Merchandiser
description: Saiba mais sobre as ferramentas do Visual Merchandiser que permitem posicionar produtos e determinar quais produtos aparecem na lista de categorias.
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: 'https://experienceleague.adobe.com/MbeCfIBdepAr5U2B1I-lfFGNm1b5DiKGevM5365brpo'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
    internal-label: Categories
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%
---
# Visual Merchandiser

{{ee-feature}}

O _Visual Merchandiser_ é um conjunto de ferramentas avançadas que permite posicionar produtos e aplicar condições que determinam quais produtos aparecem na lista de categorias. O resultado pode ser uma seleção dinâmica de produtos que se ajusta às alterações no catálogo. Você pode trabalhar no _modo visual_, que mostra cada produto como um bloco em uma grade, ou trabalhar a partir de uma lista de produtos na categoria. As mesmas ferramentas estão disponíveis em cada modo e você pode usar os botões no canto superior direito para alternar entre cada tipo de exibição.

![Categoria de produtos na exibição de bloco](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Acessar o Visual Merchandiser

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Percorra a árvore de categorias e clique na categoria que deseja editar.

1. Role para baixo e expanda ![Seletor de expansão](../assets/icon-display-expand.png) na seção **[!UICONTROL Products in Category]**.

1. Clique no botão _Exibir como Blocos_ ( ![Exibir como blocos](../assets/icon-view-tiles.png) ) para exibir os produtos como uma grade.

1. Quando terminar, clique em **[!UICONTROL Save Category]**.

## Alterar a posição de um produto

1. Use a [ordem de classificação](../catalog/navigation-product-listings.md) para exibir o produto que deseja mover.

   - **Método 1: arrastar e soltar**

     Segure o controle _Arrastar_ (![ícone Arrastar](../assets/icon-move.png)) no canto superior direito do bloco do produto e solte o produto na posição. O número de cada produto se ajusta para refletir a nova posição.

   - **Método 2: Definir Valor de Posição**

     No controlador _Posição_ (![campo Posição](../assets/control-position.png)) no bloco do produto, digite o número onde deseja que o produto apareça. Digite `0` para colocar o produto no topo da lista.

1. Quando terminar, clique em **[!UICONTROL Save Category]**.

>[!NOTE]
>
>Em uma instalação limpa, a Adobe Commerce reserva a ID de categoria `2` para o catálogo raiz do armazenamento padrão. O Visual Merchandiser pode usar somente categorias com um número de ID de `3` ou maior.

## Controles do Workspace

| Controle | Descrição |
|--- |--- |
| ![Ícone Exibir lista](../assets/icon-view-list.png) | Exibir como lista |
| ![Ícone Exibir como mosaicos](../assets/icon-view-tiles.png) | Exibir como blocos |
| ![Corresponder por alternância de regra - não](../assets/toggle-no.png) | Corresponder por regra - não |
| ![Corresponder por alternância de regra - sim](../assets/toggle-yes.png) | Corresponder por regra - sim |
| ![Ícone Mover](../assets/icon-move.png) | Arrastar |
| ![Controlador de posição](../assets/control-position.png) | Position |
| ![Ícone Remover da categoria](../assets/icon-delete-x.png) | Remover da categoria |
| ![Itens por controle de página](../assets/control-items-per-page.png) | Visualização por página |
| ![Alterar exibição de página](../assets/control-page-display.png) | Ir para o próximo/anterior |

{style="table-layout:auto"}
