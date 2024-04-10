---
title: Gerenciamento de pedidos de vitrine eletrônica
description: Saiba como os clientes podem visualizar e gerenciar o histórico de pedidos na loja do Commerce.
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

Seu inicial _[!UICONTROL My Orders]_os resultados também contêm pedidos correspondentes de usuários subordinados de todos os sites na instância de comércio. Um cliente associado a uma conta de empresa pode filtrar a lista de pedidos para localizar registros rapidamente nos resultados. Para mostrar as opções de filtro, o cliente clica em **[!UICONTROL Filter]**e cliques **[!UICONTROL Close]**para ocultar os filtros.

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

Um cliente encontra a ordem na lista e clica em **[!UICONTROL View Order]**. Na ordem aberta, eles podem executar qualquer um dos seguintes procedimentos:

![Visualizar pedido](./assets/customer-account-order-items-ordered.png){width="700" zoomable="yes"}

### Exibir produtos encomendados recentemente

A variável **[!UICONTROL Recent Orders]** é exibido na barra lateral e na janela **[!UICONTROL My Account]** página para clientes que estão conectados após fazer um pedido. Ele exibe cinco produtos da última compra.

O cliente pode ler os produtos no carrinho selecionando os produtos e clicando em **[!UICONTROL Add to Cart]**. Eles também podem exibir a última ordem clicando em **[!UICONTROL View all]**, que redireciona para a _[!UICONTROL My Account]_e a **[!UICONTROL Recent Orders]**bloco.

### Imprimir ordem

1. Cliques do cliente **[!UICONTROL Print Order]**.

1. Siga as instruções na caixa de diálogo Imprimir para concluir a impressão.

### Imprimir faturas

1. No **[!UICONTROL Invoices]** , o cliente clica em uma das seguintes opções:

   - **[!UICONTROL Print All Invoices]**

   - **[!UICONTROL Print Invoice]**

   ![Faturas](./assets/customer-account-order-invoices.png){width="700" zoomable="yes"}

1. Usa a caixa de diálogo Imprimir para concluir a impressão.

### Imprimir remessas

1. No **[!UICONTROL Order Shipments]** , o cliente clica em uma das seguintes opções:

   - **[!UICONTROL Print All Shipments]**

   - **[!UICONTROL Print Shipment]**

   ![Imprimir Todas as Entregas](./assets/customer-account-order-shipments.png){width="700" zoomable="yes"}

1. Usa a caixa de diálogo Imprimir para concluir a impressão.

### Rastrear uma remessa

1. No **[!UICONTROL Order Shipments]** clique em **[!UICONTROL Track this Shipment]**.

   Todas as informações de rastreamento disponíveis são exibidas em uma janela pop-up.

1. Quando estiver pronto, o cliente clica em **[!UICONTROL Close Window]**.

### Imprimir reembolsos

1. No **Reembolsos** , o cliente clica em uma das seguintes opções:

   - **Imprimir Todos os Reembolsos**

   - **Imprimir Reembolso**

   ![Reembolsos](./assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

1. Usa a caixa de diálogo Imprimir para concluir a impressão.

Os repedidos estarão disponíveis para os clientes quando a variável [_Permitir reordenação_](reorders-allow.md) opção de configuração está habilitada.

Um cliente pode iniciar a funcionalidade de reordenação para um pedido específico a partir de duas páginas:

- Página Meus pedidos
- Página de exibição de pedidos

## Reordenações

A variável _[!UICONTROL Reorder]_é exibido na lista com pedidos próximos a_[!UICONTROL View]_ link.

![Reordenar link na página Meu pedido](./assets/account-dashboard-reorder.png){width="700" zoomable="yes"}

**Caso 1.** Todos os produtos do pedido estão disponíveis para reordenação

O cliente é redirecionado ao carrinho de compras e todos os produtos são adicionados ao carrinho.

**Caso 2.** Alguns/todos os produtos do pedido não estão disponíveis para repedido

>[!NOTE]
>
>É possível reordenar `Not Visible Individually` produtos.

A variável _[!UICONTROL Reorder]_O link do não aparece na_[!UICONTROL My Orders]_ e _[!UICONTROL View Order]_páginas.

![Página Meu pedido](./assets/account-dashboard-reorder-grid.png){width="700" zoomable="yes"}

>[!TIP]
>
>Se o carrinho não estiver vazio e o cliente clicar em **[!UICONTROL Reorder]** (do [!UICONTROL My Orders] ou [!UICONTROL Order View] ), os produtos existentes permanecerão no carrinho com os produtos de reordenação adicionados.

## Cancelar Pedidos

Cancelar está disponível para clientes quando a variável [_Permitir cancelamento_](cancel-allow.md) opção de configuração está habilitada.

Um cliente pode iniciar a funcionalidade de cancelamento para um pedido específico a partir de três páginas:

- Página Meus pedidos
- Página de exibição de pedidos
- Página Minha conta

A variável _[!UICONTROL Cancel Order]_é exibido próximo à_[!UICONTROL Reorder]_ link. Se a ordem não puder ser cancelada, o link não será exibido.

![Cancelar link na página Meu pedido](./assets/account-dashboard-cancel.png){width="700" zoomable="yes"}

Para executar o cancelamento, o cliente:

1. Cliques **[!UICONTROL Cancel Order]**

1. Fornece um motivo de cancelamento

   ![Cancelar motivos do pedido](./assets/cancel-order-reasons.png){width="700" zoomable="yes"}

   Você pode personalizar os motivos do cancelamento na [_Permitir cancelamento_](cancel-allow.md) página.

1. Cliques **[!UICONTROL Confirm]**

   ![Cancelar na página Meu pedido](./assets/cancel-order.png){width="700" zoomable="yes"}

   Após o cancelamento, as ordens que estavam em _[!UICONTROL Pending]_status, alterar para_[!UICONTROL Canceled]_ status, os pedidos que estavam em _[!UICONTROL Processing]_status, alterar para_[!UICONTROL Closed]_ status e um reembolso será processado.

   Quando o cancelamento for concluído, um email será enviado ao cliente.

   ![Cancelar email do pedido](./assets/cancel-order-email.png){width="700" zoomable="yes"}

   As informações de cancelamento são adicionadas ao histórico de pedidos do cliente. Ele aparece dentro das notas do pedido e na guia de histórico de comentários.

   ![Cancelar notas de pedido](./assets/cancel-order-notes.png){width="700" zoomable="yes"}

   ![Cancelar histórico de comentários](./assets/cancel-order-comments.png){width="700" zoomable="yes"}

   Se, por algum motivo, o pedido tiver sido alterado para um status que não pode ser cancelado e o cliente não tiver atualizado a página, o link para cancelar o pedido ainda será exibido. No entanto, quando eles tentam cancelar, uma mensagem de erro é exibida.

   ![Cancelar mensagem de erro do pedido](./assets/cancel-order-error-message.png){width="700" zoomable="yes"}

   Depois de atualizar a página, você pode ver que o pedido já estava concluído, razão pela qual o cancelamento não funcionou.

   ![Cancelar pedido após atualização](./assets/cancel-order-after-refresh.png){width="700" zoomable="yes"}
