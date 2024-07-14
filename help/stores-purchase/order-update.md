---
title: Atualizar um pedido
description: Saiba como atualizar o pedido de um cliente no Administrador.
exl-id: 15c73d27-f4bd-47d6-8d36-902074f9c3e6
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Atualizar um pedido

Ao ajudar um cliente que fez um pedido, você deve determinar o status do pedido. As opções disponíveis para uma ordem `Pending` são diferentes das opções para uma ordem `Processing`. Para obter mais informações, consulte [Processar um pedido](order-processing.md).

## Pedidos pendentes

Depois que um cliente faz um pedido, mas antes que o pagamento seja recebido, o pedido está com o status `Pending`. Você pode editar a ordem, colocá-la em espera ou cancelá-la totalmente. A barra de botões de um pedido pendente lista as ações disponíveis para um pedido.

![Opções de Pedido Pendente](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

Se você modificar partes substanciais de um pedido, o pedido original será cancelado e um novo pedido será gerado. No entanto, você pode alterar o endereço de faturamento ou de entrega sem gerar um novo pedido.

| Botão | Descrição |
|--- |--- |
| **[!UICONTROL Back]** | Retorna à página Pedidos sem salvar as alterações. |
| **[!UICONTROL Login as Customer]** | Permite que um usuário administrador auxilie os clientes em seus pedidos. |
| **[!UICONTROL Cancel]** | Cancela a ordem pendente. |
| **[!UICONTROL Send Email]** | Envia um email sobre o pedido pendente para o cliente. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Altera o status do pedido pendente para `On Hold`. Para liberar a isenção, escolha _[!UICONTROL Unhold]_. |
| **[!UICONTROL Invoice]** | Cria uma [fatura](invoices.md#create-an-invoice) do pedido pendente convertendo o pedido em uma fatura e altera o status do pedido para `processing`. |
| **[!UICONTROL Ship]** | Cria um registro de [remessa](shipments.md#create-a-shipment) para o pedido. |
| **[!UICONTROL Reorder]** | Cria uma nova ordem pendente que é uma duplicata da ordem pendente atual. |
| **[!UICONTROL Edit]** | Abre um pedido pendente no modo de edição. O botão Editar só está disponível para pedidos pendentes ou para pedidos baseados em [cotações](../b2b/quotes.md) negociadas. |

{style="table-layout:auto"}

## Processamento de ordens

Um pedido entra em um estado `Processing` quando:

* O pagamento de um pedido é recebido/capturado e a fatura é gerada — quando a ação de pagamento é definida como `Authorize and Capture`.
* Uma transação de ordem está autorizada, mas o pagamento ainda não foi capturado—quando a ação de pagamento está definida como `Authorize`.

A [configuração da ação de pagamento](../configuration-reference/sales/payment-methods.md#payment-actions) determina quais ações de ordem estarão disponíveis depois que um pedido for criado.

Você não pode alterar substancialmente um pedido de `Processing`, mas pode editar o endereço de entrega e cobrança.

![Opções de Ordem de Processamento](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Quando a ação de pagamento do método de pagamento estiver definida como `Authorize and Capture`, uma fatura será criada automaticamente quando o cliente fizer um pedido. Nesta circunstância, você pode reembolsar fundos usando um [aviso de crédito](credit-memo-create.md), mas não pode [cancelar](#cancel-a-pending-order) ou [anular](#void-a-processing-order) a ordem.

| Botão | Descrição |
|--- |--- |
| **[!UICONTROL Back]** | Retorna à página Pedidos sem salvar as alterações. |
| **[!UICONTROL Send Email]** | Envia um email sobre o pedido para o cliente. |
| **[!UICONTROL Void]** | [Anula](#void-a-processing-order) uma transação de ordem ou uma transação de ordem parcial. |
| **[!UICONTROL Credit Memo]** | Inicia o processo para criar um [memorando de crédito](credit-memo-create.md). |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Altera o status da ordem de venda para `On Hold`. Para liberar a retenção da ordem de venda, escolha _[!UICONTROL Unhold]_. |
| **[!UICONTROL Reorder]** | Cria uma nova ordem pendente com base na ordem atual. |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Inicia o processo para [retornar](returns.md) um ou mais itens do pedido. |

{style="table-layout:auto"}

## Anular uma ordem de processamento

Quando um pedido ainda está com o status `Processing` e a integração de pagamento está definida como `Authorize` (não `Authorize and Capture`), você só pode anular uma transação ou cancelar um pedido. [Cancelar uma ordem](#cancel-a-pending-order) também anula a autorização.

Quando um pedido é feito usando um método de pagamento com a ação de pagamento definida como `Authorize and Capture`, você pode reembolsar os fundos por meio do aviso de crédito, mas não pode cancelá-lo porque ele é faturado e o pagamento é capturado.

Seu método de pagamento determina as ações de pagamento disponíveis. Consulte [Ações de pagamento](../configuration-reference/sales/payment-methods.md#payment-actions) para obter mais informações.

**_Para anular um pedido:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Na coluna **[!UICONTROL Action]** para a ordem a ser editada, clique em **[!UICONTROL View]**.

1. Clique em **[!UICONTROL Void]** para anular o pedido.

1. No prompt, clique em **[!UICONTROL OK]** para anular o pedido.

Você pode emitir qualquer reembolso necessário usando um [aviso de crédito](credit-memo-create.md) após a captura dos fundos. Você também pode criar uma [autorização para devolução de mercadoria (RMA)](returns.md) emitida para devoluções de produtos. Para saber mais, consulte [Processando um pedido](order-processing.md).

## Editar um pedido pendente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Na coluna **[!UICONTROL Action]** para a ordem a ser editada, clique em **[!UICONTROL View]**.

1. Clique em **[!UICONTROL Edit]**.

   ![Editar Ordem](./assets/order-edit.png){width="600" zoomable="yes"}

1. No prompt, clique em **[!UICONTROL OK]** para continuar editando.

1. Atualize a ordem conforme necessário.

1. Aplique as alterações:
   * Para salvar as alterações feitas no endereço de entrega ou cobrança, clique em **[!UICONTROL Save]**.
   * Para salvar as alterações feitas nos itens de linha e reprocessar o pedido, clique em **[!UICONTROL Submit Order]**.

## Colocar uma ordem em espera

Se o método de pagamento preferido do cliente não estiver disponível ou se o item estiver temporariamente esgotado, você poderá colocar a ordem em retenção.

1. Na grade _Pedidos_, encontre a ordem `Pending` que você deseja colocar em espera.

1. Na coluna _Ação_, clique em **[!UICONTROL View]**.

1. Clique em **[!UICONTROL Hold]** para colocar o pedido em espera.

Para remover a suspensão em um pedido, edite o pedido novamente e clique em **[!UICONTROL Unhold]**.

## Cancelar um pedido pendente

Cancelar um pedido altera seu status de `Pending` para `Canceled`.

1. Na grade _[!UICONTROL Orders]_, localize a ordem pendente a ser cancelada.

1. Na coluna _[!UICONTROL Action]_, clique em **[!UICONTROL View]**.

1. Clique em **[!UICONTROL Cancel]** para cancelar o pedido.

O status do pedido agora é `Canceled`.
