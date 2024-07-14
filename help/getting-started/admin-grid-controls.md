---
title: Controles de grade de administração
description: Saiba como trabalhar em páginas de administrador que gerenciam dados que exibem uma coleção de registros em uma grade.
exl-id: a4a9531d-eb2f-41d6-bb36-dc6d8811ee95
source-git-commit: a3fb702d0b6e08c3aaaa0d6b5e07aa825026ef76
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Controles de grade de administração

As páginas de administração que gerenciam dados exibem uma coleção de registros em uma grade. Os controles na parte superior de cada coluna podem ser usados para classificar os dados. A ordem de classificação atual é indicada por uma seta crescente ou decrescente no cabeçalho da coluna. Você pode especificar quais colunas aparecem na grade e arrastá-las para posições diferentes. Também é possível salvar diferentes arranjos de colunas como visualizações que podem ser usadas posteriormente. A coluna **[!UICONTROL Action]** lista operações que podem ser aplicadas a um registro individual. Além disso, a data do modo de exibição atual da maioria das grades pode ser exportada para um arquivo [CSV](../systems/data-csv.md) ou XML.

![Página Pedidos - exibição de grade](./assets/admin-workspace-grid.png){width="700" zoomable="yes"}

## Classificar a lista

1. Clique em qualquer cabeçalho de coluna.

   A seta indica a ordem atual como crescente ou decrescente.

1. Use os controles de paginação para exibir páginas adicionais na coleção.

   ![Exibição em grade - controles de página](./assets/pagination-controls.png){width="300"}

## Paginar a lista

1. Defina o controle **[!UICONTROL Pagination]** como o número de registros que deseja exibir por página.

1. Clique em **[!UICONTROL Next]** e **[!UICONTROL Previous]** para percorrer a lista ou insira um **[!UICONTROL Page Number]** específico.

## Filtrar a lista

1. Clique em **[!UICONTROL Filters]**.

1. Complete quantos filtros forem necessários para descrever o registro que deseja localizar.

1. Clique em **[!UICONTROL Apply Filters]**.

   ![Lista de pedidos - controles de filtro](./assets/admin-workspace-filters.png){width="700" zoomable="yes"}

## Exportar dados

1. Selecione os registros que deseja exportar.

   >[!NOTE]
   >
   >Os dados do produto não podem ser exportados da grade. Para saber mais, consulte [Exportar](../systems/data-export.md).

1. No menu _Exportar_ (![Seletor de menu](../assets/icon-export.png)), no canto superior direito, escolha um dos seguintes formatos de arquivo:

   - `CSV`
   - `Excel XML`

   ![Lista de pedidos - opções de exportação](./assets/customers-grid-export.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Export]**.

1. Procure o arquivo baixado de dados exportados no local usado para downloads pelo seu navegador.

## Layout de grade

A seleção de colunas e sua ordem na grade podem ser alteradas de acordo com sua preferência e salvas como uma _exibição_. Você pode controlar quais atributos são exibidos na grade na configuração de atributo individual. A exibição de muitos atributos na grade de produtos pode afetar o tempo de carregamento e o desempenho do administrador.

![Ordenar Colunas da Grade](./assets/admin-grid-columns.png){width="700" zoomable="yes"}

### Alterar a seleção de colunas

1. No canto superior direito, clique no controle _Colunas_ (![Controle de colunas](../assets/icon-columns.png)).

1. Alterar as seleções de coluna:

   - Marque a caixa de seleção de qualquer coluna que deseja adicionar à grade.
   - Desmarque a caixa de seleção de qualquer coluna que você deseja remover da grade.
   - Para retornar à exibição de grade padrão, clique em **[!UICONTROL Reset]**.

Role a tela para baixo para ver todas as colunas disponíveis.

### Mover uma coluna

1. Clique no cabeçalho da coluna e mantenha pressionado.

1. Arraste a coluna para a nova posição e solte-a.

### Salvar uma exibição de grade

1. Clique no controle _Exibir_ (![Exibir controle](../assets/icon-view-eye.png)).

1. Clique em **[!UICONTROL Save Current View]**.

1. Insira um **[!UICONTROL name]** para a exibição.

1. Para salvar todas as alterações, clique na _Seta_ (![Salvar todas as alterações](../assets/icon-arrow-save.png)).

   O nome da exibição agora aparece como a exibição atual.

### Alterar a exibição de grade

1. Clique no controle _Exibir_ (![ícone Exibir](../assets/icon-view-eye.png)).

1. Siga um destes procedimentos:

   - Para usar uma exibição diferente, clique no nome da exibição.
   - Para alterar o nome de um modo de exibição, clique no ícone _Editar_ (![Editar ícone](../assets/icon-edit-pencil.png)) e atualize o nome.
   - Para excluir um modo de exibição, clique no ícone _Editar_ (![Editar ícone](../assets/icon-edit-pencil.png)) e no ícone _Excluir_ (![Excluir ícone](../assets/icon-delete-trashcan-solid.png)).
