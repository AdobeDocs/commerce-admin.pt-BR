---
title: Adicionar produtos a um catálogo compartilhado
description: Saiba como adicionar produtos a um catálogo compartilhado, individualmente ou em grupos por categoria.
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
TQID: https://experienceleague.adobe.com/f-5xQDov-Q3tfYw8MBDQPinimUIUkGe-q2Nfzm8L9ps
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 402
ht-degree: 0%

---

# Adicionar produtos a um catálogo compartilhado

Os produtos podem ser adicionados a um catálogo compartilhado individualmente ou em grupos de vários produtos por categoria.

Os seguintes requisitos devem ser atendidos para que um produto complexo (como pacote, agrupado ou configurável) fique visível na loja em um catálogo compartilhado:

- Todos os [produtos associados](../catalog/product-configurations.md) e opções devem ser atribuídos ao mesmo catálogo compartilhado e habilitados no catálogo principal.
- Para produtos [configuráveis](../catalog/product-create-configurable.md) e [agrupados](../catalog/product-create-grouped.md), somente os produtos associados habilitados estarão visíveis.
- Para um produto [pacote](../catalog/product-create-bundle.md), todas as opções devem ser incluídas no catálogo compartilhado.

  ![Selecionar produtos para catálogo](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Método 1: adicionar um único produto

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Para o produto na grade que você deseja adicionar, vá para a coluna _[!UICONTROL Action]_&#x200B;e clique em **[!UICONTROL Edit]**.

1. Role para baixo, expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção _[!UICONTROL Product in Shared Catalogs]_&#x200B;e faça o seguinte:

   - Marque a caixa de seleção de cada catálogo compartilhado em que o produto deve aparecer. Para escolher todos os catálogos, clique em **[!UICONTROL Select all]**.

     ![Produto em Catálogos Compartilhados](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     O nome de cada catálogo selecionado aparece no campo _[!UICONTROL Shared Catalogs]_.

     ![Catálogos compartilhados atribuídos](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - Clique em **[!UICONTROL Done]** para salvar as configurações.

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Método 2: adicionar vários produtos

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Para o catálogo compartilhado na grade, vá para a coluna _[!UICONTROL Action]_&#x200B;e selecione **[!UICONTROL Set Pricing and Structure]**.

1. Na árvore de categorias, siga um destes procedimentos:

   - Para incluir todos os produtos, clique em **[!UICONTROL Select all]** ou marque a caixa de seleção da categoria principal.
   - Para incluir categorias específicas de produtos, marque a caixa de seleção de cada categoria que deseja incluir.
   - Para incluir ou excluir um produto individual, marque ou desmarque a caixa de seleção do produto.

   A notação abaixo de cada categoria na árvore mostra o número de produtos da categoria atualmente incluídos no catálogo compartilhado. A anotação abaixo da [categoria raiz](../catalog/category-root.md) mostra o número total de produtos de todas as categorias atualmente selecionadas para o catálogo compartilhado.

1. Para exibir produtos de categoria na grade, clique no nome da categoria na árvore.

   Quando uma categoria é selecionada, ocorre o seguinte:

   - O botão de alternância na primeira coluna da grade está definido como `On` para cada produto selecionado.
   - Se um produto for atribuído a várias categorias e omitido em uma delas, ele permanecerá disponível por meio das outras categorias e por meio da [pesquisa no catálogo](../catalog/search.md).
   - O sistema define automaticamente [Permissões de Categoria](../catalog/category-permissions.md) a `Allow` para os produtos selecionados.
