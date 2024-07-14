---
title: 'Guia do Inventory management [!DNL Inventory Management] Guia'
description: Informações abrangentes sobre [!DNL Inventory Management] administradores do Adobe Commerce e do Magento Open Source, incluindo migração e configuração.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Visão geral do Guia do [!DNL Inventory Management]

Este guia destina-se aos administradores do Adobe Commerce e do Magento Open Source. Ela fornece informações detalhadas sobre a habilitação desse módulo, incluindo a configuração e o gerenciamento de seus recursos. Ele pressupõe uma compreensão básica da configuração e funcionalidade do núcleo [!DNL Commerce].

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

- [Inconsistências de reserva de grande número](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [Problemas de inconsistência de inventário](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [O inventário de amostras não tachadas atinge &quot;0&quot;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- [Status do estoque incorreto após a instalação do Inventário](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [Tíquetes de suporte](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket)—Envie um tíquete para receber ajuda adicional.
