---
title: Reembolsos no painel de conta do cliente
description: Os clientes da loja podem exibir as informações de reembolso associadas ao pedido no painel da conta.
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/ggaeec6NA2K12-eHl7ESC10nU2u11ihbaxaPlbNAE9I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 485
ht-degree: 0%

---

# Reembolsos no painel de conta do cliente

{{ee-feature}}

Se um reembolso tiver sido emitido para um pedido, os clientes poderão exibir as informações de reembolso associadas ao pedido no painel de contas. Se você habilitou a opção [!UICONTROL _Mostrar Histórico de Crédito da Loja para Clientes_] para [Configuração de Crédito da Loja](../customers/credit-configure.md), os clientes também podem acessar seu histórico [Crédito da Loja](../customers/store-credit.md).

## Exibir um reembolso na loja

1. Na loja, o cliente faz logon em sua conta.

1. Localiza a ordem usando um dos seguintes métodos:

   * Localizando o pedido na lista de **Pedidos recentes** e clicando em **[!UICONTROL View]**.
   * No painel esquerdo, escolha **[!UICONTROL My Orders]**. Em seguida, localize a ordem na lista e clique em **[!UICONTROL View]**.

1. O cliente clica na guia **[!UICONTROL Refunds]** para exibir os detalhes do reembolso.

   ![Detalhes do reembolso na loja](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## Exibir o saldo e o histórico de crédito da loja

Método 1: **No painel de conta do cliente**

1. Na loja, o cliente faz logon na conta do.

1. Se o reembolso foi aplicado para armazenar crédito, escolha **[!UICONTROL Store Credit]** no painel esquerdo.

1. O valor reembolsado para o crédito de armazenamento aparece na lista com a data e hora da ação.

   ![Valor reembolsado para armazenar crédito](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >A página Crédito da Loja também fornece um link para o cliente resgatar um [cartão-presente](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

Método 2: **Na _página Revisão e Pagamentos_**

1. O cliente adiciona um produto ao carrinho.

2. Vai para a página _Check-out_.

3. Passa a etapa **[!UICONTROL Shipping]**.

4. Se o crédito da loja estiver disponível, o cliente clica em **[!UICONTROL Use Store Credit]**.

   ![Armazenar Crédito na página Revisão e Pagamentos](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. Se o cliente mudar de ideia sobre o uso do crédito da loja, clique em **[!UICONTROL Remove]** na seção _Resumo de Pedidos_.

## Ações de pagamento no Administrador

Você pode configurar ações de pagamento para o seu [Método de Pagamento](../configuration-reference/sales/payment-methods.md) específico. Cada método de pagamento tem um conjunto diferente de ações de pagamento.

| Ação de pagamento | Descrição |
|--- |---|
| [!UICONTROL Capture Online] | Quando a fatura é enviada, o sistema captura o pagamento do gateway de pagamento de terceiros. Um usuário administrador pode então criar um aviso de crédito e anular a fatura. |
| [!UICONTROL Capture Offline] | Quando a fatura é enviada, o sistema não captura o pagamento. Pressupõe-se que o pagamento seja capturado diretamente pelo gateway e que não possa ser capturado pelo Adobe Commerce. Um usuário administrador pode criar um aviso de crédito, mas não pode anular a fatura. (Mesmo que o pedido tenha utilizado um pagamento online, a fatura é essencialmente uma fatura offline.) |
| [!UICONTROL Not Capture] | Quando a fatura é enviada, o sistema não captura o pagamento. Presume-se que o pagamento seja capturado por meio do Adobe Commerce posteriormente. Há um botão [!UICONTROL _Capturar_] na fatura concluída. Antes de capturar, é possível cancelar a NFF. Depois de capturar, você poderá criar um aviso de crédito e anular a NFF. |

{style="table-layout:auto"}

>[!WARNING]
>
>Selecione a opção [!UICONTROL _Não Capturar_], a menos que você tenha certeza de que capturará o pagamento por meio do Adobe Commerce posteriormente. Você não pode criar um memorando de crédito até que o pagamento tenha sido capturado usando o botão [!UICONTROL _Capturar_].
