---
title: '[!UICONTROL My Requisition Lists]'
description: Saiba mais sobre a experiência do cliente para listas de requisição, que está disponível no painel de contas.
exl-id: ed1b41aa-9c36-49f8-80f2-ad0eb151b7a5
feature: B2B, Companies
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!UICONTROL My Requisition Lists]

O principal motivo para manter uma lista de requisições é facilitar a reorganização dos produtos. Os clientes autorizados podem reordenar facilmente os itens de uma lista de requisições, adicionando-os ao carrinho de compras e movendo ou copiando os itens de uma lista para outra.

![Minhas Listas de Requisições](./assets/account-dashboard-my-requisition-lists.png){width="700" zoomable="yes"}

## Abrir uma lista de requisições

1. No painel de contas, o cliente escolhe **[!UICONTROL My Requisition Lists]**.

1. Localiza a lista de requisições que deseja abrir, clica em **[!UICONTROL View]** e realiza qualquer um dos seguintes procedimentos:

### Adicionar produtos ao carrinho

1. O cliente realiza um dos seguintes procedimentos para selecionar os produtos a serem adicionados:

   - Marca a caixa de seleção de cada item.
   - Cliques **[!UICONTROL Select All]**.

1. Insere o **[!UICONTROL Qty]** a ser adicionado ao carrinho.

1. Para alterar qualquer opção de produto, o faz o seguinte:

   - No item de linha, clique no ícone _Editar_ (![Lápis](../assets/icon-edit-pencil.png)).
   - Altera todas as opções necessárias.
   - Cliques **[!UICONTROL Update Requisition List]**.

1. Cliques **[!UICONTROL Add to Cart]**.

   ![Detalhes da Lista de Requisições](./assets/requisition-list-view.png){width="700" zoomable="yes"}

### Copiar itens para uma lista diferente

1. O cliente marca a caixa de seleção de cada item a ser movido.

1. Clica em **[!UICONTROL Copy Selected]** e executa um dos seguintes procedimentos:

   - Escolhe uma lista de requisições existente.
   - Cliques **[!UICONTROL Create New Requisition List]**.

### Exportar uma lista

1. O cliente abre a lista de requisições a serem exportadas.

1. Clica no link **[!UICONTROL Export]**.

O Adobe Commerce gera e baixa uma lista CSV com `sku` e `qty` valores.

### Mover itens para uma lista diferente

1. O cliente marca a caixa de seleção de cada item a ser movido.

1. Clique em **[!UICONTROL Move Selected]** e siga um destes procedimentos:

   - Escolhe uma lista de requisições existente.
   - Cliques **[!UICONTROL Create New Requisition List]**.

### Imprimir uma lista

1. No canto superior direito da lista, o cliente clica em **[!UICONTROL Print]**.

1. Verifique o dispositivo de saída e clique em **[!UICONTROL Print]**.

   ![Imprimir Lista de Requisições](./assets/requisition-list-print.png){width="500" zoomable="yes"}

### Editar opções de produto

Para editar as opções de produto na lista, o cliente faz o seguinte:

1. Clica no ícone de _Lápis_ (![Lápis](../assets/icon-edit-pencil.png)) para abrir a página do produto.

1. Altera todas as opções necessárias.

1. Cliques **[!UICONTROL Update Requisition List]**.

   ![Atualizar Lista de Requisições](./assets/requisition-list-update.png){width="700" zoomable="yes"}

Um produto na lista de requisições pode ser editado quando:

- O produto tem **[!UICONTROL all options set]** (quando é um [produto configurado](../catalog/product-create-configurable.md) na Lista de Requisições).

  O produto é **[!UICONTROL added to this Requisition List]**.

- O produto é [um produto simples com opções](../catalog/settings-advanced-custom-options.md)

- A edição é permitida para o tipo de produto.

### Remover itens

1. O cliente marca a caixa de seleção de cada item a ser removido.

1. Cliques **[!UICONTROL Remove Selected]**.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL Delete]**.

### Renomear uma lista

1. Após o título da lista, o cliente clica em **[!UICONTROL Rename]**.

1. Inserir um **[!UICONTROL Requisition List Name]** diferente.

1. Cliques **[!UICONTROL Save]**.

   ![Renomear Lista de Requisições](./assets/requisition-list-rename.png){width="300"}


### Remover uma lista de requisições

1. O cliente abre a lista de requisições a serem deletadas.

1. Cliques **[!UICONTROL Delete Requisition List]**.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL Delete]**.

>[!NOTE]
>
>Essa ação não pode ser desfeita.

## Ações

| Ação | Descrição |
|--- |--- |
| [!UICONTROL Rename] | Oferece a capacidade de renomear a lista de requisições e atualizar a descrição. |
| [!UICONTROL Export] | Exporta a lista de requisições em um arquivo CSV. |
| [!UICONTROL Print] | Imprime a lista de requisições atual. |
| [!UICONTROL Select] | Gerencia as seleções de itens que serão o assunto de uma ação. <br/>**[!UICONTROL Select All]**- Seleciona todos os itens na lista de requisições.<br/>**[!UICONTROL Remove Selected]** - Remove todos os itens selecionados da lista de requisições. <br/>**[!UICONTROL Copy Selected]**- Copia todos os itens selecionados para outra lista de requisições. |
| [!UICONTROL Add to Cart] | Adiciona itens selecionados ao carrinho de compras. |
| [!UICONTROL Update List] | Recalcula o subtotal para refletir uma alteração na quantidade. |
| [!UICONTROL Delete Requisition List] | Exclui a lista de requisições da conta do usuário da empresa. |

{style="table-layout:auto"}
