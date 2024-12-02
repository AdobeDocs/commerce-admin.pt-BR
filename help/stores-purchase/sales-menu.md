---
title: Menu [!UICONTROL Sales]
description: O Administrador do Commerce inclui o menu [!UICONTROL Sales], que fornece acesso a ferramentas para trabalhar com pedidos de acordo com onde eles estão no fluxo de trabalho.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# Menu [!UICONTROL Sales]

O menu Vendas lista as transações de acordo com onde elas estão no workflow da ordem. Você pode pensar em cada opção como um estágio diferente no tempo de vida de um pedido.

![Menu Vendas](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## Exibir o menu [!UICONTROL Sales]

Na barra lateral _Admin_, clique em **[!UICONTROL Sales]**.

## Opções de menu

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) (Disponível com Adobe Commerce B2B)

Os compradores autorizados podem [negociar o preço](../b2b/quotes.md) com o vendedor, enviando uma [solicitação](../b2b/quote-request.md) do carrinho de compras.

### [!UICONTROL Orders]

Quando um [pedido](orders.md) é feito, uma ordem de venda é criada como um registro temporário da transação. O pagamento não foi processado e o pedido ainda pode ser cancelado.

### [!UICONTROL Invoices]

Uma [fatura](invoices.md) é um registro do recebimento de pagamento de um pedido. Várias faturas podem ser criadas para um único pedido, cada uma com a quantidade de produtos comprados que você especificar. Dependendo da ação de pagamento, o pagamento poderá ser capturado automaticamente quando a NFF for gerada.

### [!UICONTROL Shipments]

Uma [remessa](shipments.md) é um registro dos produtos em um pedido que foram remetidos. Assim como com as NFFs, várias entregas podem ser associadas a um único pedido, até que todos os produtos do pedido sejam entregues.

### [!UICONTROL Credit Memos]

Um [memorando de crédito](credit-memos.md) é um documento que mostra o valor devido pelo cliente para um reembolso total ou parcial. O valor pode ser aplicado a uma compra ou reembolsado ao cliente.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce)

Uma [autorização de mercadoria devolvida](returns.md) (RMA) pode ser concedida a clientes que solicitam a devolução de um item para substituição ou reembolso. As RMAs podem ser emitidas para tipos de produtos Simples, Agrupado, Configurável e Pacote. No entanto, os RMAs não estão disponíveis para produtos virtuais e baixáveis ou cartões-presente.

### [!UICONTROL Billing Agreements]

Um [contrato de cobrança](paypal-billing-agreements.md) é semelhante a uma ordem de compra, exceto que não está limitado a uma única compra. Durante a finalização da compra, o cliente escolhe o Contrato de faturamento como método de pagamento. Um contrato de faturamento simplifica o processo de finalização porque o cliente não precisa inserir informações de pagamento para cada compra.

### [!UICONTROL Transactions]

A página [Transações](transactions.md) lista todas as atividades de pagamento que ocorreram entre sua loja e todos os sistemas de pagamento e fornece acesso a informações mais detalhadas.

### [!UICONTROL Braintree Virtual Terminal]

Na página do Terminal virtual de Braintree, um usuário administrador pode aceitar o pagamento do valor selecionado. Para disponibilizar o recurso de terminal, um comerciante deve definir as [configurações de Braintree](braintree.md) básicas. O Braintree oferece uma experiência de finalização de compra totalmente personalizável com detecção de fraudes e integração com o PayPal.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce)

(A opção de arquivamento deve estar habilitada) [Arquivar ordens](order-archive.md) e outros documentos de vendas melhora o desempenho regularmente e mantém seu espaço de trabalho livre de informações desnecessárias.
