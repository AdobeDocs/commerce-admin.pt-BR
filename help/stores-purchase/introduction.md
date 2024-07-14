---
title: Introdução a lojas e experiência de compra
description: Saiba mais sobre os recursos usados para criar e gerenciar suas lojas online e a experiência de compra para seus clientes.
exl-id: 7ced9cbc-49b4-48f7-aae2-fcb48fdb888f
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Introdução a lojas e experiência de compra

A Adobe Commerce e o Magento Open Source fornecem um conjunto abrangente de recursos para construir e gerenciar suas lojas online e a experiência de compra para seus clientes. Na instância do Commerce, é possível gerenciar a hierarquia de lojas de sites, lojas e visualizações. Você também pode configurar os impostos e as taxas de moeda necessários para executar lojas para vários locais, incluindo classes de imposto para produtos e grupos de clientes.

## Estrutura da loja

Uma única instância do Adobe Commerce ou do Magento Open Source pode oferecer suporte a vários sites, lojas ou visualizações de loja que usam diferentes atributos e conteúdo. Um cenário típico é configurar lojas com diferentes opções em domínios diferentes. Por exemplo, você pode querer um conjunto de categorias e produtos em um domínio e outro conjunto de categorias e produtos em um domínio diferente em outro idioma. Os comerciantes podem configurar os sites, lojas e visualizações de loja no Administrador.

Quando a [hierarquia](stores.md) for definida, você poderá aplicar as definições de configuração de acordo com o [escopo](../getting-started/websites-stores-views.md#scope-settings) de modo que cada exibição de site, loja e loja forneça o catálogo de produtos e a experiência da loja desejada.

## Ponto de compra

O Adobe Commerce e o Magento Open Source reduzem os erros de pedido verificando automaticamente o SKU e a disponibilidade de todos os itens antes do envio de um pedido. Você pode configurar as [opções de carrinho](cart.md) e [de check-out](checkout-process.md) para fornecer uma experiência de compra ideal, desde a transação até a entrega. Os clientes que estão conectados às suas contas podem concluir o check-out rapidamente, pois grande parte das informações já está em suas contas. A página _Check-out_ guia o cliente em cada etapa do processo para concluir a transação do pedido. Se você ativar a [Compra instantânea](checkout-instant-purchase.md), os clientes poderão agilizar o processo de finalização usando as informações salvas em suas contas.

>[!TIP]
>
>![Adobe Commerce B2B](../assets/b2b.svg) Com a instalação e a habilitação do Adobe Commerce B2B, você pode configurar o _Pedido rápido_ para clientes associados a uma conta de empresa. Essa função reduz o processo de pedido a vários cliques quando o cliente souber o nome ou a SKU dos produtos que deseja solicitar. Você também pode configurar o suporte para Cotações Negociáveis para suas contas da empresa. Para obter mais informações sobre os recursos B2B, consulte o [Guia do Usuário B2B do Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## Assistência para compras

Às vezes, os clientes precisam de assistência para concluir uma compra. Alguns clientes gostam de fazer compras online, mas preferem fazer pedidos por telefone. Você pode oferecer assistência imediata aos hóspedes e clientes que se registraram em uma conta na sua loja.

- [Gerenciar o carrinho de compras](shopping-assisted-cart-manage.md)
- [Criar pedidos](customer-account-create-order.md) para clientes registrados
- [Atualizar ordens](order-update.md)

![Carrinho de compras](./assets/storefront-cart-price-group-discount.png){width="700" zoomable="yes"}

Saiba mais sobre compras assistidas por vendedores assistindo a este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/343662/?quality=12)

## Gerenciamento de pedidos e operações

No Admin, os comerciantes podem acessar informações em cada estágio do workflow da ordem e processar ordens:

- A página [Pedidos](orders.md) fornece aos comerciantes uma lista de fácil acesso de todos os pedidos atuais, inclui ferramentas para editar e processar pedidos existentes e criar pedidos em nome dos clientes.

- A página [Faturas](invoices.md) lista Uma fatura é baseada em uma ordem de venda temporária e fornece um registro permanente da ordem.

- A página [Remessas](shipments.md) lista o registro de remessa de cada fatura pronta para ser remetida.

- A página [Avisos de Crédito](credit-memos.md) permite que os comerciantes processem e gerenciem um aviso de crédito, que é um documento que mostra o valor devido ao cliente. O valor pode ser aplicado a uma compra ou reembolsado ao cliente.

- ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) A página [Devoluções](returns.md) lista as solicitações de merchandise (RMAs) retornadas no momento e é usada para inserir novas solicitações de devolução.

- A página [Transações](transactions.md) lista todas as atividades de pagamento que ocorreram entre sua loja e um sistema de pagamento e fornece acesso a informações mais detalhadas.

## Envio e entrega

Estudos mostram que as lojas que oferecem aos clientes uma opção de vários [métodos de entrega](delivery.md) têm taxas de conversão mais altas do que as lojas que usam um único método. O Administrador fornece várias ferramentas que os comerciantes podem usar para configurar vários métodos de entrega e [transportadoras](carriers.md), e para imprimir [etiquetas de remessa](shipping-labels.md).
