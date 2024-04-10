---
title: Ordens de compra para empresas
description: Saiba mais sobre os workflows de ordem de compra que permitem que as empresas rastreiem e controlem os gastos.
exl-id: 4f93ab4c-6bdf-495e-9183-3a18898b377f
feature: B2B, Purchase Orders
source-git-commit: 4b34645377102e890779059e57c61cf23f71f34c
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 0%

---

# Ordens de compra para empresas

As ordens de compra (OCs) são uma maneira comum de as empresas rastrearem e controlarem os gastos. [Ordem de compra](../stores-purchase/purchase-order.md) O é um dos métodos de pagamento off-line padrão compatíveis com o Adobe Commerce e o Magento Open Source. Quando o B2B do Adobe Commerce estiver instalado e [_Habilitar Ordens de Compra_](account-company-manage.md#advanced-settings) for ativada para uma conta da empresa, todas as ordens serão criadas automaticamente como Ordens de compra (OC). Usuários da empresa com as [permissões](account-company-roles-permissions.md) O pode criar, editar e deletar OCs que eles criam e OCs criadas por usuários subordinados.

## Fluxo da ordem de compra

Dependendo de sua função e da ordem, os usuários da empresa podem estar sujeitos a várias regras de aprovação. E dependendo de usar métodos de pagamento online ou offline, o fluxo é um pouco diferente. Os administradores da empresa podem criar pedidos automaticamente, ignorando as regras de aprovação. Como o armazenamento de detalhes de pagamento online durante o processo de aprovação é um risco de segurança, esses detalhes são adicionados após a aprovação e, em seguida, a ordem de compra é convertida em uma ordem real.

![Fluxo da ordem de compra](./assets/purchase-order-flow.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Um pedido não poderá ser feito se um ou mais produtos no pedido de compra estiverem desativados no momento ou esgotados.

O fluxo de trabalho da ordem de compra de uma empresa pode variar de algumas maneiras:

- Se nenhuma regra de aprovação for definida, as ordens de compra poderão ser feitas e a ordem concluída diretamente.

  >[!NOTE]
  >
  >Por padrão, uma variável `Purchase order has been submitted for approval` é sempre exibida para usuários da empresa, mesmo quando nenhuma regra de aprovação é definida. Quando nenhum processo de aprovação é necessário, os usuários da empresa recebem automaticamente um email informando que o pedido foi criado e aprovado.

- Se as regras de aprovação forem definidas pelo administrador da empresa, os usuários passarão pelo processo de aprovação.
- Detalhes de pagamento offline são inseridos ao criar a ordem de compra.
- Os detalhes do pagamento online são inseridos após a aprovação da ordem de compra.

>[!NOTE]
>
>Ordens de Compra criar um _instantâneo_ de preços de item, descontos e preços de entrega no momento em que o pedido foi criado. Se o preço de um item for alterado depois que a OC for criada, será usado o preço original.

### Exemplo básico de fluxo de trabalho

As empresas usam ordens de compra para controlar o que os funcionários podem comprar em nome da empresa e geralmente configuram regras de aprovação para aplicar as diretrizes da empresa. Dependendo das regras de aprovação, várias pessoas podem precisar aprovar o pedido.

1. O usuário cria uma ordem de compra de US$ 25.000 em mercadorias.
1. O gerente deles deve aprovar.
1. Como o pedido é superior a US$ 10.000, o V.P. também deve aprovar.
1. Dependendo do método de pagamento, após as aprovações, a ordem de compra é convertida automaticamente em uma ordem ou o usuário retorna para inserir detalhes de pagamento.

### Regras de aprovação

As regras de aprovação são usadas para controlar os gastos com base nas diretrizes da empresa. Exemplos de regras de aprovação:

- Qualquer pedido acima de US$ 100 precisa da aprovação do seu gerente.
- Qualquer pedido acima de US$ 1.000 precisa da aprovação do seu gerente e do administrador da empresa.
- Qualquer pedido com mais de 30 SKUs exclusivas precisa da aprovação do administrador da empresa.

Com essas regras em vigor para uma empresa, um usuário da empresa pode concluir o pedido imediatamente quando o pedido for inferior a US$ 100. Para saber mais sobre a definição da regra de aprovação, consulte [Regras de aprovação](account-dashboard-approval-rules.md)

### Tipos de usuários de loja

O workflow da ordem de compra também pode ser diferente dependendo de quem está fazendo a compra.

- Um funcionário regular pode estar sujeito a todas as regras de aprovação
- Um gerente poderia ter mais poder de compra e teria regras de aprovação diferentes
- Os administradores da empresa podem ignorar todas as regras de aprovação e ter suas ordens de compra concluídas automaticamente.

Todos esses fatores podem influenciar o processo exato de finalização.

## [!UICONTROL My Purchase Orders]

Quando as ordens de compra são ativadas para uma empresa, a variável **[!UICONTROL My Purchase Orders]** O item é exibido no painel esquerdo para clientes conectados a uma conta de usuário da empresa. Há três guias que fornecem diferentes listas e funções de ordem de compra:

- **[!UICONTROL My Purchase Orders]**: OCs criadas pelo cliente.
- **[!UICONTROL Company Purchase Orders]**: OCs feitas por usuários subordinados na empresa (depende da estrutura e das funções da empresa).
- **[!UICONTROL Requires My Approval]**: (Visível para aprovadores designados) OCs que estão aguardando a aprovação do cliente. O contador mostra quantos pedidos estão aguardando aprovação.

![Minhas Ordens de Compra](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

Para obter mais informações sobre as funções de ordem de compra aceitas disponíveis para usuários da empresa na loja, consulte [Minhas Ordens de Compra](account-dashboard-my-purchase-orders.md).

## Métodos de pagamento offline vs. online

Os workflows podem variar dependendo do método de pagamento. Para saber mais sobre os métodos de pagamento do Adobe Commerce, consulte [Métodos de pagamento](../stores-purchase/payments.md) no _Guia de experiência de vendas e compras_.

>[!IMPORTANT]
>
>As ordens de compra devem usar um _No contexto_ experiência de finalização. _Fora de contexto_ os check-outs não são suportados porque eles ignoram o fluxo de check-out normal. Em geral, _No contexto_ significa que o cliente permanece no site de comércio para concluir o processo. _Fora de contexto_ é quando o cliente é levado a outro site para concluir a compra.

### Pagamentos online

Por motivos de segurança, as lojas online normalmente não querem coletar os detalhes do cartão de crédito da loja enquanto aguardam a conclusão do processo de aprovação. Portanto, se uma opção de pagamento online for selecionada, o criador da ordem de compra retornará ao armazenamento após a aprovação, inserirá os detalhes do pagamento e concluirá a ordem. São exemplos de pagamentos em linha:

- Cartões de crédito/débito
- PayPal
- Braintree

>[!IMPORTANT]
>
>Não há suporte para o uso de cartões-presente, crédito de loja ou pontos de premiação com métodos de pagamento online para ordens de compra. A ativação desses recursos com pagamentos online pode causar algum comportamento inesperado. É recomendável desativar cartões-presente, armazenar crédito e pontos de premiação quando os pagamentos online estiverem habilitados para ordens de compra.

### Pagamentos offline

Como os métodos de pagamento offline, como uma ordem de pagamento, são tratados fora do site, eles são mais seguros. As ordens de compra com pagamentos offline podem ser processadas automaticamente, após qualquer processo de aprovação.

Exemplos de pagamentos off-line são:

- Cheque/Ordem de pagamento
- Pagamento por conta
- Dinheiro na entrega
- Transferências Bancárias
- Crédito da loja
