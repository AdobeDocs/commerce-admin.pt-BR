---
title: Aplicar crédito da loja
description: Os administradores de loja podem aplicar crédito de loja a uma compra.
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Aplicar crédito da loja

{{ee-feature}}

Os administradores de loja podem exibir o saldo e o histórico de crédito da conta do cliente e também aplicar crédito de loja a uma compra.

![Histórico e saldo de crédito do cliente](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## Exibir o saldo de crédito

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Encontre o cliente na grade.

1. Na coluna _Ação_, clique em **[!UICONTROL Edit]**.

1. Role a página _[!UICONTROL Customer View]_e exiba **[!UICONTROL Store Credit Balance]**na parte inferior.

![Armazenar Saldo de Crédito](assets/store-credit-balance.png){width="600" zoomable="yes"}

## Atualizar saldo de crédito da loja

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > _Operações_ > **[!UICONTROL All Customers]**.

1. Encontre o cliente na grade.

1. Na coluna _Ação_, clique em **[!UICONTROL Edit]**.

1. No painel esquerdo, escolha **[!UICONTROL Store Credit]**.

1. Escolha o site (vitrine) que deseja associar ao saldo.

1. Para **[!UICONTROL Update Balance]**, insira o novo valor.

1. Para notificar o cliente sobre a atualização do saldo, marque a caixa de seleção **[!UICONTROL Notify Customer by Email]** e escolha o modo de exibição de loja em **[!UICONTROL Send Email Notification From the Following Store View]**.

1. Digite um **[!UICONTROL Comment]** sobre a alteração.

1. Quando as atualizações estiverem concluídas, clique em **[!UICONTROL Save and Continue Edit]** ou **[!UICONTROL Save Customer]**.

O saldo atualizado deve ser exibido em **[!UICONTROL Balance History]**.

## Aplicar um saldo de crédito a uma ordem como administrador de armazenamento

Como administrador de loja, você pode fazer várias coisas em nome de um cliente, incluindo o envio de pedidos. Ao [criar um pedido](../stores-purchase/customer-account-create-order.md), você pode aplicar um saldo de Crédito da Loja que é devido ao cliente. O saldo disponível é exibido na seção _Informações de Pagamento e Envio_. Marque a caixa de seleção **[!UICONTROL Use Store Credit]** para aplicar o saldo ou uma parte do saldo se o total do pedido for menor.

![Aplicar o saldo de crédito da loja à ordem](assets/store-credit-apply.png){width="500" zoomable="yes"}

## Aplicar crédito de armazenamento durante o check-out

Se houver um saldo de crédito para o local, o cliente poderá aplicar o crédito de armazenamento ao saldo da ordem antes de colocar a ordem na loja.

1. O cliente visualiza a quantidade de crédito de loja disponível.

   Durante a etapa _Verificação e Pagamentos_, o valor disponível aparece em _[!UICONTROL Store Credit]_.

1. Para aplicar o valor ao pedido, clique em **[!UICONTROL Use Store Credit]**.

   >[!INFO]
   >
   >O total do pedido é recalculado e a quantidade de crédito de armazenamento aplicada aparece no _[!UICONTROL Order Summary]_.

   ![Saldo de crédito de armazenamento aplicado ao pedido](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. Quando estiver pronto, clica em **[!UICONTROL Place Order]**.
