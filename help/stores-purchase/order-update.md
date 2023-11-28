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

Ao ajudar um cliente que fez um pedido, você deve determinar o status do pedido. As opções disponíveis para um `Pending` pedidos são diferentes das opções de um `Processing` pedido. Para obter mais informações, consulte [Processar um pedido](order-processing.md).

## Pedidos pendentes

Depois que um cliente faz um pedido, mas antes de o pagamento ser recebido, o pedido está em `Pending` status. Você pode editar a ordem, colocá-la em espera ou cancelá-la totalmente. A barra de botões de um pedido pendente lista as ações disponíveis para um pedido.

![Opções de pedido pendente](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

Se você modificar partes substanciais de um pedido, o pedido original será cancelado e um novo pedido será gerado. No entanto, você pode alterar o endereço de faturamento ou de entrega sem gerar um novo pedido.

| Botão | Descrição |
|--- |--- |
| **[!UICONTROL Back]** | Retorna à página Pedidos sem salvar as alterações. |
| **[!UICONTROL Login as Customer]** | Permite que um usuário administrador auxilie os clientes em seus pedidos. |
| **[!UICONTROL Cancel]** | Cancela a ordem pendente. |
| **[!UICONTROL Send Email]** | Envia um email sobre o pedido pendente para o cliente. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Altera o status do pedido pendente para `On Hold`. Para liberar a retenção, escolha _[!UICONTROL Unhold]_. |
| **[!UICONTROL Invoice]** | Cria um [fatura](invoices.md#create-an-invoice) da ordem pendente convertendo a ordem em uma NFF e alterando o status da ordem para `processing`. |
| **[!UICONTROL Ship]** | Cria um [remessa](shipments.md#create-a-shipment) registro do pedido. |
| **[!UICONTROL Reorder]** | Cria uma nova ordem pendente que é uma duplicata da ordem pendente atual. |
| **[!UICONTROL Edit]** | Abre um pedido pendente no modo de edição. O botão Editar só está disponível para ordens pendentes ou para ordens baseadas em ordens negociadas [aspas](../b2b/quotes.md). |

{style="table-layout:auto"}

## Processamento de ordens

Um pedido insere um `Processing` quando:

* O pagamento de uma ordem é recebido/capturado e a fatura é gerada — quando a ação de pagamento é definida como `Authorize and Capture`.
* Uma transação de ordem está autorizada, mas o pagamento ainda não foi capturado—quando a ação de pagamento está definida como `Authorize`.

A variável [configuração da ação de pagamento](../configuration-reference/sales/payment-methods.md#payment-actions) determina quais ações de ordem estarão disponíveis após a criação de um pedido.

Não é possível alterar substancialmente um `Processing` pedido, mas você pode editar o endereço de cobrança e de entrega.

![Opções de Ordem de Processamento](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Quando a ação de pagamento do método de pagamento é definida como `Authorize and Capture`, uma fatura é criada automaticamente quando o cliente faz um pedido. Nessa circunstância, é possível reembolsar fundos usando uma [memorando de crédito](credit-memo-create.md), mas não pode [cancelar](#cancel-a-pending-order) ou [void](#void-a-processing-order) a ordem.

| Botão | Descrição |
|--- |--- |
| **[!UICONTROL Back]** | Retorna à página Pedidos sem salvar as alterações. |
| **[!UICONTROL Send Email]** | Envia um email sobre o pedido para o cliente. |
| **[!UICONTROL Void]** | [Nulos](#void-a-processing-order) uma transação de ordem ou uma transação de ordem parcial. |
| **[!UICONTROL Credit Memo]** | Inicia o processo para criar uma [memorando de crédito](credit-memo-create.md). |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Altera o status da ordem de venda para `On Hold`. Para liberar a retenção na ordem de venda, escolha _[!UICONTROL Unhold]_. |
| **[!UICONTROL Reorder]** | Cria uma nova ordem pendente com base na ordem atual. |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Inicia o processo para [retornar](returns.md) um ou mais itens do pedido. |

{style="table-layout:auto"}

## Anular uma ordem de processamento

Quando um pedido ainda está em uma `Processing` e a integração de pagamento estiver definida como `Authorize` (não `Authorize and Capture`), você só poderá anular uma transação ou cancelar um pedido. [Cancelar um pedido](#cancel-a-pending-order) também anula a autorização.

Quando um pedido é feito usando um método de pagamento com a ação de pagamento definida como `Authorize and Capture` você pode reembolsar os fundos por meio do aviso de crédito, mas não pode cancelá-lo porque ele foi faturado e o pagamento foi capturado.

Seu método de pagamento determina as ações de pagamento disponíveis. Consulte [Ações de pagamento](../configuration-reference/sales/payment-methods.md#payment-actions) para obter mais informações.

**_Para anular uma ordem:_**

1. No _Admin_ barra lateral, vá para **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. No **[!UICONTROL Action]** para a ordem a ser editada, clique em **[!UICONTROL View]**.

1. Clique em **[!UICONTROL Void]** para anular a ordem.

1. No prompt, clique em **[!UICONTROL OK]** para anular a ordem.

É possível emitir os reembolsos necessários usando uma [memorando de crédito](credit-memo-create.md) após a captura dos fundos. Você também pode criar um [autorização para devolução de mercadoria (RMA)](returns.md) emitido para devoluções de produtos. Para saber mais, consulte [Processar um pedido](order-processing.md).

## Editar um pedido pendente

1. No _Admin_ barra lateral, vá para **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. No **[!UICONTROL Action]** para a ordem a ser editada, clique em **[!UICONTROL View]**.

1. Clique em **[!UICONTROL Edit]**.

   ![Editar pedido](./assets/order-edit.png){width="600" zoomable="yes"}

1. No prompt, clique em **[!UICONTROL OK]** para continuar editando.

1. Atualize a ordem conforme necessário.

1. Aplique as alterações:
   * Para salvar as alterações feitas no endereço de entrega ou cobrança, clique em **[!UICONTROL Save]**.
   * Para salvar as alterações feitas nos itens de linha e reprocessar a ordem, clique em **[!UICONTROL Submit Order]**.

## Colocar uma ordem em espera

Se o método de pagamento preferido do cliente não estiver disponível ou se o item estiver temporariamente esgotado, você poderá colocar a ordem em retenção.

1. No _Pedidos_ grade, localize a `Pending` ordem que você deseja colocar em espera.

1. No _Ação_ clique em **[!UICONTROL View]**.

1. Clique em **[!UICONTROL Hold]** para colocar a ordem em retenção.

Para remover a suspensão em um pedido, edite-o novamente e clique em **[!UICONTROL Unhold]**.

## Cancelar um pedido pendente

Cancelar um pedido altera seu status de `Pending` para `Canceled`.

1. No _[!UICONTROL Orders]_grade, localize a ordem pendente a ser cancelada.

1. No _[!UICONTROL Action]_clique em **[!UICONTROL View]**.

1. Clique em **[!UICONTROL Cancel]** para cancelar a ordem.

O status do pedido agora é `Canceled`.
