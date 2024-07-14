---
title: Transações
description: Saiba mais sobre a página Transações e como usá-la para rastrear a atividade entre sua loja e um sistema de pagamento.
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Transações

A página _Transações_ lista todas as atividades de pagamento que ocorreram entre sua loja e um sistema de pagamento e fornece acesso a informações mais detalhadas.

## Exibir transações

Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Transactions]**.

![Grade de transações](./assets/transactions.png){width="600" zoomable="yes"}

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL ID] | Um identificador numérico exclusivo atribuído a cada transação. |
| [!UICONTROL Order ID] | Um identificador exclusivo atribuído quando um cliente faz um pedido. |
| [!UICONTROL Transaction ID] | Um identificador numérico exclusivo que é atribuído quando uma transação ocorre depois que um cliente faz um pedido. |
| [!UICONTROL Parent Transaction ID] | O número de ID da transação pai. |
| [!UICONTROL Payment Method] | O método de pagamento associado a uma transação. |
| [!UICONTROL Transaction Type] | Tipo de transação, que pode ser Ordem, Autorização, Captura, Anulação ou Reembolso. |
| [!UICONTROL Closed] | Se uma transação está fechada ou não. |
| [!UICONTROL Created] | Hora e data em que a transação foi criada. |

{style="table-layout:auto"}

## Exibir detalhes da transação

Clique na entrada que deseja exibir.

Na página de detalhes da transação, você pode ver a grade de detalhes da transação e transações-filho.

### Dados da transação

Esta seção inclui informações sobre a transação e fornece um link para a página de pedido na coluna **ID do Pedido**.

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL Transaction ID] | O número de ID da transação. |
| [!UICONTROL Parent Transaction ID] | Um número de ID correspondente da transação pai, se aplicável. |
| [!UICONTROL Transaction Type] | Tipo de transação, que pode ser Ordem, Autorização, Captura, Anulação ou Reembolso. |
| [!UICONTROL Is Closed] | Se uma transação está fechada ou não. |
| [!UICONTROL Created At] | Hora e data em que a transação foi criada. |

{style="table-layout:auto"}

### Transações secundárias

As transações filho são exibidas na grade após a criação de faturas para [pedidos](orders.md). Esse formato permite rastrear o histórico de transações seguindo uma hierarquia de transações.

### [!UICONTROL Transaction Details]

Esta seção inclui as informações adicionais para uma determinada transação. As informações são exibidas na forma de chaves e valores. As chaves disponíveis são:

- authAmount
- authCode
- aVSResponse
- billTo
- cardCodeResponse
- cliente
- customerIP
- lineItems
- marketType
- pedido
- pagamento
- produto
- recurringBilling
- responseCode
- responseReasonCode
- responseReasonDescription
- settAmount
- solução
- submitTimeLocal
- submitTimeUTC
- taxExempt
- transactionStatus

>[!NOTE]
>
>Se os detalhes da transação não estiverem disponíveis ou estiverem desatualizados, clique em **[!UICONTROL Fetch]** na barra de botões para atualizá-los.
