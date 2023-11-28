---
title: Compra instantânea
description: Saiba mais sobre o Instant Purchase e saiba como ele pode fornecer um check-out rápido para contas de clientes registradas.
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Compra instantânea

_Compra instantânea_ O permite que os clientes acelerem o processo de finalização usando informações salvas em suas contas do. Quando ativado, a variável _Compra instantânea_ é exibido abaixo do _Adicionar ao carrinho_ na página do produto para clientes que atendem aos requisitos.

![Página do produto com a opção Compra instantânea exibida](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## Requisitos do cliente

- O cliente está [conectado](../customers/customer-sign-in.md) para a conta deles.

- A conta do cliente tem uma [endereço de entrega e cobrança padrão](../customers/account-dashboard-address-book.md).

- Pelo menos um [método de envio](delivery.md) está disponível para o país especificado no endereço de entrega padrão.

- A conta do cliente tem uma [pagamento armazenado](../stores-purchase/stored-payment-methods.md) com o Vault ativado.

  Os métodos de pagamento a seguir podem ser usados para fornecer acesso seguro às informações salvas do cartão de crédito:

   - [Cartões de crédito Braintree](braintree.md) (A Compra instantânea não pode ser usada com Cartões de crédito Braintree se o 3D Secure estiver habilitado.)
   - [Braintree com PayPal habilitado](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## Compra instantânea na loja

1. Na loja, o cliente vai para a página do produto do item a ser comprado.

1. Seleciona as opções e cliques necessários **[!UICONTROL Instant Purchase]**.

   ![Caixa de diálogo de confirmação para confirmar a compra instantânea](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. Analisa a **[!UICONTROL Instant Purchase Confirmation]** informações e cliques **[!UICONTROL OK]** para concluir a transação.

   Uma mensagem de confirmação e o número do pedido são exibidos na parte superior da página do produto.

## Configurar Compra Instantânea

### Etapa 1: abrir a página de configuração

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

### Etapa 2: configurar o cofre do método de pagamento

Você pode usar a Compra instantânea com o Braintree ou com os Serviços de pagamento para Adobe Commerce e Magento Open Source. A compartimentalização deve ser ativada antes que um comprador possa usar a função de Compra instantânea.

Saiba como configurar o método de pagamento e habilitar a compartimentalização para Braintree ou Serviços de pagamento:

- [Braintree](braintree.md)
- [Documentação dos serviços de pagamento](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)

### Etapa 3: Habilitar Compra Instantânea

1. No painel esquerdo, abaixo de _[!UICONTROL Sales]_escolha **[!UICONTROL Sales]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Instant Purchase]** seção.

1. Se essa alteração for para uma exibição de loja específica, [escolher a exibição de loja](../configuration-reference/scope-change.md#set-the-scope) onde a configuração se aplica.

   Quando solicitado, clique em **[!UICONTROL OK]** para continuar.

1. Definir **[!UICONTROL Enabled]** para `Yes`.

1. Insira o **[!UICONTROL Button Text]** que você deseja exibir no botão.

   O texto do botão pode ser alterado para cada exibição de armazenamento ou idioma. Por padrão, o texto do botão é `Instant Purchase`.

   ![Configuração - opções de compra instantânea](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   Para obter uma descrição detalhada de cada uma dessas configurações, consulte [Compra instantânea](../configuration-reference/sales/sales.md#instant-purchase) no _Guia de referência de configuração_.

1. Clique em **[!UICONTROL Save Config]**.

1. Quando solicitado a atualizar o cache, clique em **[!UICONTROL Cache Management]** na mensagem do sistema e siga as instruções para liberar o cache.
