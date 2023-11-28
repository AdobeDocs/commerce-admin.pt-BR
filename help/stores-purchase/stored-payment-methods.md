---
title: Métodos de pagamento armazenados
description: Saiba como os clientes podem usar métodos de pagamento armazenados em sua loja do Commerce.
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Métodos de pagamento armazenados

Os clientes com acesso a um cofre seguro para armazenar informações de pagamento podem agilizar a finalização da compra sem inserir as informações de cartão de crédito a cada vez. Se [Compra instantânea](checkout-instant-purchase.md) estiver ativado, os clientes poderão ignorar o processo de finalização de duas etapas e fazer o pedido na página do produto.

Um método de pagamento compatível com um cofre seguro, como [Braintree](braintree.md), é obrigatório. Quando um cofre seguro é ativado na configuração do método de pagamento, os clientes têm a opção, durante a finalização da compra, de salvar suas informações de cartão de crédito como um método de pagamento armazenado. Os clientes podem gerenciar métodos de pagamento armazenados no painel de contas.

![Métodos de pagamento armazenados](./assets/customer-account-stored-payment-methods.png){width="700" zoomable="yes"}

## Adicionar método de pagamento armazenado no check-out

1. Na loja, o cliente acessa a página de detalhes do produto.

1. Adiciona o produto ao carrinho.

1. Prossegue para a página de check-out.

1. Conclui o _Envio_ etapa.

1. Seleciona o **[!UICONTROL Braintree Credit Card]** método de pagamento.

1. Preenche os dados do cartão de crédito.

1. Seleciona o **[!UICONTROL Save for later use]** caixa de seleção

1. Cliques **[!UICONTROL Place Order]**.

O método de pagamento salvo será exibido no campo _[!UICONTROL Stored Payment Methods]_do painel do cliente.

## Excluir um método de pagamento armazenado

Qualquer método de pagamento adicionado anteriormente e armazenado não pode ser editado pelo cliente, somente pode ser excluído. Essa ação não pode ser desfeita.

1. Na barra lateral da conta, o cliente seleciona **[!UICONTROL Stored Payment Methods]**.

1. Localiza a entrada do método de pagamento a ser excluída.

1. Cliques **[!UICONTROL Delete]**.

1. Para confirmar a ação, clique em **[!UICONTROL OK]**.
