---
title: Gerenciamento de pedidos de vitrine eletrônica
description: Saiba como os clientes podem visualizar e gerenciar seu histórico de pedidos na loja da Commerce.
exl-id: 85d953e6-f5a1-4a5e-a6ef-36b9cf6988bb
feature: Orders, Storefront
source-git-commit: c13a4b730ed70ed4829cc20b13c2723137dcbb3a
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Gerenciamento de pedidos de vitrine eletrônica

Os clientes têm acesso a todos os seus pedidos por meio de sua conta. Os pedidos podem ser visualizados, filtrados, rastreados e reenviados como novos pedidos. Dependendo do status da ordem, os clientes podem imprimir suas ordens, NFFs, entregas e registros de restituição.

## Filtrar ordens

{{b2b-feature}}

Os resultados iniciais de _[!UICONTROL My Orders]_também contêm pedidos correspondentes de usuários subordinados de todos os sites na instância de comércio. Um cliente associado a uma conta de empresa pode filtrar a lista de pedidos para localizar registros rapidamente nos resultados. Para mostrar as opções de filtro, o cliente clica em **[!UICONTROL Filter]**e em **[!UICONTROL Close]**para ocultar os filtros.

![Meus Pedidos](./assets/account-dashboard-my-orders-b2b.png){width="700" zoomable="yes"}

| Filtro | Descrição |
| ------ | ----------- |
| [!UICONTROL SKU or Product Name] | Insira um SKU ou um nome de produto. |
| [!UICONTROL Order Number] | Pode ser um número de pedido completo ou parcial. |
| [!UICONTROL Order Status] | Escolhe um valor na lista suspensa para filtrar por status. |
| [!UICONTROL Invoice Number] | Insere um número de fatura total ou parcial. |
| [!UICONTROL Order Date] | Define um ou ambos os campos de data para filtrar por data do pedido. |
| [!UICONTROL Created by] | Filtra os pedidos da empresa pelo criador do pedido. |
| [!UICONTROL Order Total] | Define os valores mín., máx. ou ambos para filtrar pelo total do pedido. |

## Exibir um pedido

Um cliente encontra o pedido na lista e clica em **[!UICONTROL View Order]**. Na ordem aberta, eles podem executar qualquer um dos seguintes procedimentos:

![Exibir Pedido](./assets/customer-account-order-items-ordered.png){width="700" zoomable="yes"}

### Exibir produtos encomendados recentemente

O bloco **[!UICONTROL Recent Orders]** é exibido na barra lateral e na página **[!UICONTROL My Account]** para clientes que estão conectados após fazerem um pedido. Ele exibe cinco produtos da última compra.

O cliente pode ler os produtos no carrinho selecionando os produtos e clicando em **[!UICONTROL Add to Cart]**. Eles também podem exibir a última ordem clicando em **[!UICONTROL View all]**, que redireciona para a página _[!UICONTROL My Account]_e o bloco **[!UICONTROL Recent Orders]**.

### Imprimir ordem

1. O cliente clica em **[!UICONTROL Print Order]**.

1. Siga as instruções na caixa de diálogo Imprimir para concluir a impressão.

### Imprimir faturas

1. Na guia **[!UICONTROL Invoices]**, o cliente clica em uma das opções a seguir:

   - **[!UICONTROL Print All Invoices]**

   - **[!UICONTROL Print Invoice]**

   ![Faturas](./assets/customer-account-order-invoices.png){width="700" zoomable="yes"}

1. Usa a caixa de diálogo Imprimir para concluir a impressão.

### Imprimir remessas

1. Na guia **[!UICONTROL Order Shipments]**, o cliente clica em uma das opções a seguir:

   - **[!UICONTROL Print All Shipments]**

   - **[!UICONTROL Print Shipment]**

   ![Imprimir Todas as Remessas](./assets/customer-account-order-shipments.png){width="700" zoomable="yes"}

1. Usa a caixa de diálogo Imprimir para concluir a impressão.

### Rastrear uma remessa

1. Na guia **[!UICONTROL Order Shipments]**, clique em **[!UICONTROL Track this Shipment]**.

   Todas as informações de rastreamento disponíveis são exibidas em uma janela pop-up.

1. Quando estiver pronto, o cliente clica em **[!UICONTROL Close Window]**.

### Imprimir reembolsos

1. Na guia **Reembolsos**, o cliente clica em uma das seguintes opções:

   - **Imprimir Todos Os Reembolsos**

   - **Imprimir Reembolso**

   ![Reembolsos](./assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

1. Usa a caixa de diálogo Imprimir para concluir a impressão.

Reordenações estão disponíveis para os clientes quando a opção de configuração [_Permitir Reordenação_](reorders-allow.md) está habilitada.

Um cliente pode iniciar a funcionalidade de reordenação para um pedido específico a partir de duas páginas:

- Página Meus pedidos
- Página de exibição de pedidos

## Reordenações

O link _[!UICONTROL Reorder]_é exibido na lista com pedidos próximos ao link_[!UICONTROL View]_.

![Reordenar link na página Meu Pedido](./assets/account-dashboard-reorder.png){width="700" zoomable="yes"}

**Caso 1.** Todos os produtos do pedido estão disponíveis para reordenação

O cliente é redirecionado ao carrinho de compras e todos os produtos são adicionados ao carrinho.

**Caso 2.** Alguns/todos os produtos do pedido não estão disponíveis para reordenação

>[!NOTE]
>
>É possível reordenar `Not Visible Individually` produtos.

O link _[!UICONTROL Reorder]_não aparece nas páginas_[!UICONTROL My Orders]_ e _[!UICONTROL View Order]_.

![Página Meu Pedido](./assets/account-dashboard-reorder-grid.png){width="700" zoomable="yes"}

>[!TIP]
>
>Se o carrinho não estiver vazio e o cliente clicar em **[!UICONTROL Reorder]** (na página [!UICONTROL My Orders] ou [!UICONTROL Order View]), os produtos existentes permanecerão no carrinho com os produtos de reordenação adicionados.

## Cancelar Pedidos

Cancelar está disponível para clientes quando a opção de configuração [_Permitir Cancelamento_](cancel-allow.md) está habilitada.

Um cliente pode iniciar a funcionalidade de cancelamento para um pedido específico a partir de três páginas:

- Página Meus pedidos
- Página de exibição de pedidos
- Página Minha conta

O link _[!UICONTROL Cancel Order]_é exibido próximo ao link_[!UICONTROL Reorder]_. Se a ordem não puder ser cancelada, o link não será exibido.

![Cancelar link na página Meu Pedido](./assets/account-dashboard-cancel.png){width="700" zoomable="yes"}

Para executar o cancelamento, o cliente:

1. Cliques **[!UICONTROL Cancel Order]**

1. Fornece um motivo de cancelamento

   ![Cancelar motivos do pedido](./assets/cancel-order-reasons.png){width="700" zoomable="yes"}

   Você pode personalizar os motivos do cancelamento na página [_Permitir cancelamento_](cancel-allow.md).

1. Cliques **[!UICONTROL Confirm]**

   ![Cancelar na página Meu Pedido](./assets/cancel-order.png){width="700" zoomable="yes"}

   Após o cancelamento, os pedidos que estavam no status _[!UICONTROL Pending]_, mudam para o status_[!UICONTROL Canceled]_, os pedidos que estavam no status _[!UICONTROL Processing]_, mudam para o status_[!UICONTROL Closed]_ e um reembolso será processado.

   Quando o cancelamento for concluído, um email será enviado ao cliente.

   ![Cancelar email de pedido](./assets/cancel-order-email.png){width="700" zoomable="yes"}

   As informações de cancelamento são adicionadas ao histórico de pedidos do cliente. Ele aparece dentro das notas do pedido e na guia de histórico de comentários.

   ![Cancelar notas de pedido](./assets/cancel-order-notes.png){width="700" zoomable="yes"}

   ![Cancelar histórico de comentários](./assets/cancel-order-comments.png){width="700" zoomable="yes"}

   Se, por algum motivo, o pedido tiver sido alterado para um status que não pode ser cancelado e o cliente não tiver atualizado a página, o link para cancelar o pedido ainda será exibido. No entanto, quando eles tentam cancelar, uma mensagem de erro é exibida.

   ![Cancelar mensagem de erro da ordem](./assets/cancel-order-error-message.png){width="700" zoomable="yes"}

   Depois de atualizar a página, você pode ver que o pedido já estava concluído, razão pela qual o cancelamento não funcionou.

   ![Cancelar ordem após atualização](./assets/cancel-order-after-refresh.png){width="700" zoomable="yes"}
