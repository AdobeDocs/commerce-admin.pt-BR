---
title: Categoria raiz e hierarquia
description: Saiba mais sobre a hierarquia de categorias e a categoria raiz, que atua como um container para o menu principal na árvore de categorias.
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
TQID: https://experienceleague.adobe.com/nkUEOu8IqMM21waPwmkp76YckH6cToL6MiaSK--klho
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 437
ht-degree: 0%

---

# Categoria raiz e hierarquia

Os produtos no menu principal são determinados pela categoria raiz atribuída à [loja](../stores-purchase/stores.md#add-stores). A categoria raiz é basicamente um container para o menu principal na árvore de categorias. É possível criar uma categoria raiz com um conjunto de produtos totalmente novo ou copiar produtos de uma categoria raiz existente. A categoria raiz pode ser atribuída ao armazenamento atual ou a qualquer outro armazenamento no mesmo site.

![Diagrama de hierarquia de catálogo](./assets/catalog-hierarchy-scope.svg){width="550"}

No Admin, a estrutura da categoria é como uma árvore de cabeça para baixo, com a raiz na parte superior. A raiz tem um nome, mas nenhuma chave de URL, e não aparece na [navegação superior](navigation-top.md) do armazenamento. Todas as outras categorias no menu são aninhadas abaixo da raiz. Como a categoria raiz é o nível mais alto do catálogo, seu armazenamento pode ter somente uma categoria raiz ativa por vez. No entanto, você pode criar categorias raiz adicionais para estruturas de catálogo alternativas e lojas diferentes.

O exemplo a seguir mostra como criar uma categoria raiz e atribuí-la a um armazenamento diferente.

## Etapa 1: criar uma categoria raiz

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. À esquerda, clique em **[!UICONTROL Add Root Category]**.

   ![Nova categoria raiz](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. Insira um **[!UICONTROL Category Name]**.

   O nome escolhido é inicialmente atribuído a todas as exibições de loja.

1. Se quiser adicionar produtos ao catálogo a partir do catálogo atual, faça o seguinte:

   - Expanda o ![Seletor de expansão](../assets/icon-display-expand.png) a seção _Produtos na Categoria_.

   - Use os [filtros de pesquisa](../getting-started/admin-grid-controls.md) para localizar os produtos desejados e marque a caixa de seleção de cada produto que deseja copiar para o novo catálogo.

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Etapa 2: criar o menu principal

1. À esquerda, selecione a nova categoria raiz que você criou na etapa anterior.

1. Para criar a [estrutura de categoria](category-create.md) para o menu principal, clique em **[!UICONTROL Add Subcategory]** e siga as instruções.

## Etapa 3: atribuir a categoria raiz ao armazenamento

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Na coluna _Lojas_ da grade, clique no armazenamento ao qual deseja atribuir o novo catálogo.

1. Defina **[!UICONTROL Root Category]** para a nova categoria raiz que você criou.

1. Verifique se o armazenamento tem um **[!UICONTROL Default Store View]** atribuído.

   O armazenamento deve ter pelo menos uma [exibição de armazenamento](../stores-purchase/store-views.md).

1. Quando terminar, clique em **[!UICONTROL Save Store]**.

1. Para verificar se o armazenamento tem um novo catálogo, faça o seguinte:

   - Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

     Todos os produtos que foram copiados para o novo catálogo aparecem na grade.

   - Para verificar se o novo catálogo e o menu principal estão funcionando corretamente, visite a loja.
