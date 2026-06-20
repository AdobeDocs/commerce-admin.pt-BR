---
title: Guia do Inventory management [!DNL Inventory Management] Guia
description: Informações abrangentes sobre o  [!DNL Inventory Management]  para administradores do Adobe Commerce e do Magento Open Source, incluindo migração e configuração.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
TQID: https://experienceleague.adobe.com/AFaKjUXrfZOMSYWjcW-dyD9OBMlQj6PkILIQiuT8YJU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 394
ht-degree: 0%

---

# Visão geral do Guia do [!DNL Inventory Management]

Este guia destina-se aos administradores que trabalham no Adobe Commerce e no Magento Open Source Admin. Ela fornece informações detalhadas sobre a habilitação desse módulo, incluindo a configuração e o gerenciamento de seus recursos. Ele pressupõe uma compreensão básica da configuração e funcionalidade do núcleo [!DNL Commerce].

[!DNL Inventory Management] tem duas áreas para administradores:

- O Admin: use essa área para acessar a interface do usuário e os relatórios de configuração.
- A interface de linha de comando: use essa ferramenta para executar tarefas de instalação e configuração de backend.

Este guia abrange:

| Assunto | Descrição |
| ------- | ----------- |
| [Introdução](introduction.md) | Visão geral dos recursos do [!DNL Inventory Management] que você pode usar para gerenciar estoque em vários locais para que sua loja da Commerce reflita com precisão o estoque físico. |
| [Notas de versão](release-notes.md) | Revise as notas de versão para obter informações sobre todas as versões do [!DNL Inventory Management]. |
| Noções básicas de inventário | Saiba mais sobre as noções básicas de gerenciamento de estoque: [Estoques e fontes](sources-stocks.md), [seleção e reservas de origem](selection-reservations.md), [status de pedido e reserva](order-status.md) e [tipos de produto](product-types.md) |
| Introdução | Saiba mais sobre o módulo [!DNL Inventory Management] e como ele se encaixa em suas operações de instância e armazenamento da Commerce: [atualizações do Commerce](migrate.md), [instalação e atualização do módulo](install-update.md), [tipos de fornecimento de comerciantes](merchant-sourcing.md) e [alterações na estrutura de fornecimento](expand-restructure.md) |
| [Configuração](configuration.md) | Saiba mais sobre a configuração das opções do [!DNL Inventory Management] que determinam a disponibilidade de origem, os produtos da loja e a remessa do pedido. |
| [Gerenciar fontes](sources-manage.md) | Saiba mais sobre as origens e como elas definem os locais físicos onde o inventário de produtos é gerenciado e enviado para o atendimento de pedidos ou onde os serviços estão disponíveis. |
| [Gerenciar estoques](stocks-manage.md) | Saiba como o estoque é usado para representar um inventário agregado virtual de produtos para fontes de seus canais de vendas. |
| [Gerenciar quantidades](quantities-manage.md) | Saiba como atribuir origens e quantidades para novos produtos ou alterar produtos existentes. |
| [Gerenciar pedidos e remessas](shipments.md) | Saiba mais sobre os recursos e opções adicionais do [!DNL Inventory Management] para gerenciar quantidades de estoque por meio do processo de remessa. |
| [Referência de CLI](cli.md) | Saiba mais sobre os comandos fornecidos pelo módulo [!DNL Inventory Management] para gerenciar dados de inventário e definições de configuração. |

{style="table-layout:auto"}

## Informações do desenvolvedor

Consulte [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) na documentação do desenvolvedor para obter detalhes sobre a arquitetura do módulo, as APIs e a personalização de algoritmo.

## Documentação do Commerce

{{docs-links}}

## Solução de problemas e suporte

Se você precisar de informações ou tiver dúvidas que não são abordadas neste guia, use os seguintes recursos:

- [Status do estoque incorreto após a instalação do inventário](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html?lang=pt-BR)
- [Tíquetes de suporte](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=pt-BR#submit-ticket)—Envie um tíquete para receber ajuda adicional.
