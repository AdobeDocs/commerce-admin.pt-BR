---
title: Crédito da loja
description: O crédito da loja é um valor restaurado para uma conta de cliente e que pode ser usado para pagar compras ou reembolsos em dinheiro.
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/kG-y-O2Yh-h1ct-oCwqylZFvS2FOCXFPD6qVIkKrpbg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 291
ht-degree: 0%

---

# Crédito da loja

{{ee-feature}}

O crédito da loja é um valor restaurado para uma conta de cliente. Os clientes podem usar o crédito da loja para pagar compras e os administradores podem usar o crédito da loja para reembolsos em dinheiro. Os saldos de cartão-presente podem ser creditados na conta do cliente, em vez de usar o código do cartão-presente para compras futuras.

Depois que um pedido é pago e faturado, o pedido, ou uma parte dele, pode ser reembolsado pela [emissão de um memorando de crédito](../stores-purchase/credit-memo-create.md). Um aviso de crédito é diferente de um reembolso porque o valor do crédito é restaurado na conta do cliente, onde pode ser usado para compras futuras. Às vezes, um reembolso pode ser concedido ao mesmo tempo em que um aviso de crédito é emitido e aplicado ao saldo do crédito de armazenamento do cliente. O valor de crédito de armazenamento disponível na conta do cliente é especificado na configuração.

>[!NOTE]
>
>O método de pagamento [_Check-out de Subtotal Zero_](../stores-purchase/zero-subtotal-checkout.md) deve ser habilitado caso o crédito de armazenamento cubra o total do pedido.

## Fluxo de trabalho de crédito da loja

1. **Logon do cliente** - O cliente entra na conta antes de iniciar o processo de finalização.

1. **Usar Loja** - Crédito Durante a etapa [!UICONTROL _Avaliação e Pagamentos_] do processo de finalização, o cliente seleciona [!UICONTROL _Usar Crédito da Loja_] como uma opção de pagamento. O saldo disponível é exibido entre parênteses. Se o saldo disponível for maior que o total geral, os outros métodos de pagamento não serão mais exibidos.

1. **Crédito aplicado ao pedido** - O valor do crédito de armazenamento aplicado ao pedido aparece com os totais do pedido e é subtraído do total geral.

1. **Saldo do cliente ajustado** - O saldo disponível do cliente é ajustado quando o pedido é feito.
