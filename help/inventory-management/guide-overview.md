---
title: Guia do [!DNL Inventory Management]
description: Guia de administração e CLI para  [!DNL Inventory Management] estoques, fontes, quantidades, configuração, pedidos e remessas na Adobe Commerce e na Magento Open Source.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
TQID: https://experienceleague.adobe.com/AFaKjUXrfZOMSYWjcW-dyD9OBMlQj6PkILIQiuT8YJU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a3817847081e56272e3677dede02d992e760a2d4
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 1%

---

# Visão geral das [!DNL Inventory Management]

Este guia é para administradores que gerenciam estoque em vários locais na Adobe Commerce e no Magento Open Source. Ele fornece procedimentos de configuração e gerenciamento para o módulo [!DNL Inventory Management] e presume uma compreensão básica da funcionalidade principal [!DNL Commerce].

Use o **Administrador** para tarefas de configuração, relatórios e inventário do dia a dia. Use a **interface de linha de comando** para instalação, atualizações e configuração de back-end.

Este guia abrange:

| Assunto | Descrição |
| ------- | ----------- |
| [Introdução](introduction.md) | Recursos, terminologia e como o [!DNL Inventory Management] se encaixa em sua loja. |
| [Notas de versão](release-notes.md) | Histórico de versões do módulo e problemas conhecidos. |
| [Noções básicas sobre inventário](sources-stocks.md) | Conceitos de [estoques e origens](sources-stocks.md), [seleção e reservas de origem](selection-reservations.md), [status de pedido e reserva](order-status.md) e [tipos de produto](product-types.md). |
| Introdução | [atualizações do Commerce](migrate.md), [instalação e atualizações](install-update.md), [tipos de fornecedores de comerciantes](merchant-sourcing.md) e [reestruturação de estoque](expand-restructure.md). |
| [Configuração](configuration.md) | Configurações globais, de produto e de algoritmo para exibição e remessa de vitrines. |
| [Gerenciar fontes](sources-manage.md) | Criar e manter locais de preenchimento. |
| [Gerenciar estoques](stocks-manage.md) | Mapear fontes para canais de vendas. |
| [Gerenciar quantidades](quantities-manage.md) | Atribuir e atualizar quantidades de produtos por origem. |
| [Gerenciar pedidos e remessas](shipments.md) | Atenda ordens e gerencie entregas do inventário. |
| [Referência de CLI](cli.md) | Inventário de linha de comando e tarefas de configuração. |

{style="table-layout:auto"}

## Informações do desenvolvedor

Acesse recursos avançados para APIs, personalização e arquitetura de módulos. Consulte [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) na documentação do desenvolvedor da REST API para obter detalhes técnicos sobre APIs e personalização de algoritmo.

## Documentação do Commerce

Encontre guias do comerciante, da nuvem e do desenvolvedor para ajudar em todas as partes do Adobe Commerce. Use esses recursos para qualquer necessidade de configuração ou gerenciamento.

{{docs-links}}

## Solução de problemas e suporte

Use artigos de suporte e sistemas de tíquetes para resolver problemas de inventário rapidamente. Obtenha ajuda extra para o status do estoque ou gerenciamento de produtos.

Se você precisar de informações ou tiver dúvidas que não são abordadas neste guia, use os seguintes recursos:

- [Status do estoque incorreto após a instalação do inventário](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-29910)
- [Tíquetes de suporte](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-help-center-user-guide#support-case)—Envie um tíquete para receber ajuda adicional.
