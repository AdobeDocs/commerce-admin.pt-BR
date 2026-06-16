---
title: Transações
description: Saiba mais sobre a página Transações e como usá-la para rastrear a atividade entre sua loja e um sistema de pagamento.
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
TQID: https://experienceleague.adobe.com/WyZwtVw-F-pGxxfcHMU-UTz8GVROVyM-YYaLzivMLBM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 318
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
