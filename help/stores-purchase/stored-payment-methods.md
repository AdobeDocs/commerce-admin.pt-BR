---
title: Métodos de pagamento armazenados
description: Saiba como os clientes podem usar métodos de pagamento armazenados em sua loja da Commerce.
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
TQID: https://experienceleague.adobe.com/dYEYXgEIp83AKhHepfDQVNR9YBUQGbJ7B2zu8UTM-I4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 0%

---

# Métodos de pagamento armazenados

Os clientes com acesso a um cofre seguro para armazenar informações de pagamento podem agilizar a finalização da compra sem inserir as informações de cartão de crédito a cada vez. Se a [Compra instantânea](checkout-instant-purchase.md) estiver habilitada, os clientes poderão ignorar o processo de finalização em duas etapas e fazer o pedido na página do produto.

É necessário um método de pagamento que ofereça suporte a um cofre seguro, como [Braintree](braintree.md). Quando um cofre seguro é ativado na configuração do método de pagamento, os clientes têm a opção, durante a finalização da compra, de salvar suas informações de cartão de crédito como um método de pagamento armazenado. Os clientes podem gerenciar métodos de pagamento armazenados no painel de contas.

![Métodos de pagamento armazenados](./assets/customer-account-stored-payment-methods.png){width="700" zoomable="yes"}

## Adicionar método de pagamento armazenado no check-out

1. Na loja, o cliente acessa a página de detalhes do produto.

1. Adiciona o produto ao carrinho.

1. Prossegue para a página de check-out.

1. Conclui a etapa _Remessa_.

1. Seleciona o método de pagamento **[!UICONTROL Braintree Credit Card]**.

1. Preenche os dados do cartão de crédito.

1. Marca a caixa de seleção **[!UICONTROL Save for later use]**.

1. Cliques **[!UICONTROL Place Order]**.

O método de pagamento salvo será exibido na guia _[!UICONTROL Stored Payment Methods]_&#x200B;do painel do cliente.

## Excluir um método de pagamento armazenado

Qualquer método de pagamento adicionado anteriormente e armazenado não pode ser editado pelo cliente, somente pode ser excluído. Essa ação não pode ser desfeita.

1. Na barra lateral da conta, o cliente seleciona **[!UICONTROL Stored Payment Methods]**.

1. Localiza a entrada do método de pagamento a ser excluída.

1. Cliques **[!UICONTROL Delete]**.

1. Para confirmar a ação, clique em **[!UICONTROL OK]**.
