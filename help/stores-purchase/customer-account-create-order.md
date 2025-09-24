---
title: Criar um pedido
description: Saiba como criar um pedido para um cliente no Administrador do Commerce.
exl-id: 8a766a5b-55d6-4d78-859e-38937e0183d3
feature: Orders, Customer Service
source-git-commit: 0e2d79f6b716f5d59aa9cd60b096608a6b2dbb98
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Criar um pedido

Para clientes registrados que precisam de assistência, você pode criar um pedido inteiro diretamente do administrador. O formulário _[!UICONTROL Create New Order]_&#x200B;inclui todas as informações necessárias para o processo normal de check-out, com resumos de atividades do painel de conta do cliente.

![Criar um pedido para um cliente](./assets/create-new-order.png){width="700" zoomable="yes"}

## Etapa 1: criar um pedido

1. Na barra lateral _Admin_, clique em **[!UICONTROL Customers]**.

1. Encontre o cliente na grade.

1. Na coluna _Ação_, clique em **[!UICONTROL Edit]**.

1. No cabeçalho do espaço de trabalho, clique em **[!UICONTROL Create Order]**.

   ![cabeçalho do Workspace](./assets/order-create-buttons.png){width="700" zoomable="yes"}

   Você também pode criar um pedido no [espaço de trabalho de Pedidos](orders.md#orders-workspace) clicando em **[!UICONTROL Create New Order]**.

## Etapa 2: adicionar produtos

Se a loja tiver várias exibições, escolha a exibição da loja onde o pedido será feito.

### Adicionar produtos da barra lateral [!UICONTROL Customer's Activities]

Você pode transferir itens para o carrinho da lista de desejos de um cliente ou de qualquer item exibido, comparado ou solicitado recentemente.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) uma das seguintes seções:

   - **[!UICONTROL Wish List]**
   - **[!UICONTROL Last Ordered Items]**
   - **[!UICONTROL Products in Comparison List]**
   - **[!UICONTROL Recently Compared Products]**
   - **[!UICONTROL Recently Viewed Products]**

1. Marque a caixa de seleção de cada produto no painel esquerdo.

1. Role para baixo e clique em **[!UICONTROL Update Changes]**.

   O item aparece no formulário de pedido.

   ![Adicionar ao carrinho](./assets/create-order-add-wishlist.png){width="600" zoomable="yes"}

### Adicionar produtos do catálogo

1. Clique em **[!UICONTROL Add Products]**.

   ![Adicionar produtos](./assets/account-add-wishlist-product.png){width="600" zoomable="yes"}

1. Na grade, marque a caixa de seleção de cada produto a ser adicionado ao carrinho e insira o **[!UICONTROL Qty]** a ser comprado.

   ![Selecionar produtos](./assets/create-order-from-catalog.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >A grade de seleção de produtos sempre mostra preços base regulares para produtos, sem descontos e quaisquer regras de preço de carrinho ou grupo aplicadas. O preço do produto final é calculado somente quando o produto é adicionado a um pedido/carrinho.

1. Configure as opções de produto disponíveis:

   - Clique em **[!UICONTROL Configure]**.

   - Preencha as opções conforme necessário.

   - Clique em **[!UICONTROL OK]**.

   - Clique em **[!UICONTROL Add Selected Product(s) to Order]** para atualizar o carrinho.

1. Se um produto estiver configurado para [opções de presente](../catalog/product-gift-options.md), defina as opções conforme necessário.

1. Sobrepor o preço de um item, se necessário:

   - Marque a caixa de seleção **[!UICONTROL Custom Price]** e insira o novo preço na caixa abaixo.

   - Para atualizar os totais do carrinho, clique em **[!UICONTROL Update Items and Quantities]**.

   ![Preço Personalizado](./assets/create-order-custom-price.png){width="600" zoomable="yes"}

1. Preencha as seguintes seções conforme necessário para o pedido:

   - [!UICONTROL Order Currency]
   - [!UICONTROL Apply Coupon Codes / Gift Card Code]
   - [!UICONTROL Payment Method]
   - [!UICONTROL Shipping Method]
   - [!UICONTROL Order Comments]
   - [[!UICONTROL [Atributos da ordem personalizada]]](../stores-purchase/order-processing.md#custom-order-attributes)

>[!NOTE]
>
>Consulte o [Guia dos Serviços de Pagamento](https://experienceleague.adobe.com/pt-br/docs/commerce/payment-services/guide-overview) para obter mais informações sobre métodos de pagamento para dar suporte a esta funcionalidade quando a extensão dos Serviços de Pagamento for instalada e configurada.

## Etapa 3: enviar o pedido

Clique em **[!UICONTROL Submit Order]**.

Uma confirmação será enviada ao cliente, que poderá ver os detalhes do pedido em sua conta.
