---
title: Introdução a lojas e experiência de compra
description: Saiba mais sobre os recursos usados para criar e gerenciar suas lojas online e a experiência de compra para seus clientes.
exl-id: 7ced9cbc-49b4-48f7-aae2-fcb48fdb888f
TQID: https://experienceleague.adobe.com/wP31dNMG9kiajirB5WTj-lEhTtHqKnl4FfqPsa3tFxs
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
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
source-wordcount: 680
ht-degree: 0%

---

# Introdução a lojas e experiência de compra

A Adobe Commerce e a Magento Open Source fornecem um conjunto abrangente de recursos para criar e gerenciar suas lojas online e a experiência de compra para seus clientes. Na instância do Commerce, é possível gerenciar a hierarquia de lojas de sites, lojas e visualizações. Você também pode configurar os impostos e as taxas de moeda necessários para executar lojas para vários locais, incluindo classes de imposto para produtos e grupos de clientes.

## Estrutura da loja

Uma única instância do Adobe Commerce ou do Magento Open Source pode oferecer suporte a vários sites, lojas ou visualizações de loja que usam atributos e conteúdo diferentes. Um cenário típico é configurar lojas com diferentes opções em domínios diferentes. Por exemplo, você pode querer um conjunto de categorias e produtos em um domínio e outro conjunto de categorias e produtos em um domínio diferente em outro idioma. Os comerciantes podem configurar os sites, lojas e visualizações de loja no Administrador.

Quando a [hierarquia](stores.md) for definida, você poderá aplicar as definições de configuração de acordo com o [escopo](../getting-started/websites-stores-views.md#scope-settings) de modo que cada exibição de site, loja e loja forneça o catálogo de produtos e a experiência da loja desejada.

## Ponto de compra

A Adobe Commerce e a Magento Open Source reduzem os erros de pedido verificando automaticamente o SKU e a disponibilidade de todos os itens antes do envio de um pedido. Você pode configurar as [opções de carrinho](cart.md) e [de check-out](checkout-process.md) para fornecer uma experiência de compra ideal, desde a transação até a entrega. Os clientes que estão conectados às suas contas podem concluir o check-out rapidamente, pois grande parte das informações já está em suas contas. A página _Check-out_ guia o cliente em cada etapa do processo para concluir a transação do pedido. Se você ativar a [Compra instantânea](checkout-instant-purchase.md), os clientes poderão agilizar o processo de finalização usando as informações salvas em suas contas.

>[!TIP]
>
>![Adobe Commerce B2B](../assets/b2b.svg) Com a instalação e a habilitação do Adobe Commerce B2B, você pode configurar o _Pedido rápido_ para clientes associados a uma conta de empresa. Essa função reduz o processo de pedido a vários cliques quando o cliente souber o nome ou a SKU dos produtos que deseja solicitar. Você também pode configurar o suporte para Cotações Negociáveis para suas contas da empresa. Para obter mais informações sobre os recursos B2B, consulte o [Guia do Usuário B2B do Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=pt-BR).

## Assistência para compras

Às vezes, os clientes precisam de assistência para concluir uma compra. Alguns clientes gostam de fazer compras online, mas preferem fazer pedidos por telefone. Você pode oferecer assistência imediata aos hóspedes e clientes que se registraram em uma conta na sua loja.

- [Gerenciar o carrinho de compras](shopping-assisted-cart-manage.md)
- [Criar pedidos](customer-account-create-order.md) para clientes registrados
- [Atualizar ordens](order-update.md)

![Carrinho de compras](./assets/storefront-cart-price-group-discount.png){width="700" zoomable="yes"}

Saiba mais sobre compras assistidas por vendedores assistindo a este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3411979/?captions=por_br&quality=12&learn=on)

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
