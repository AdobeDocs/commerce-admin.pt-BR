---
title: Guia de sistemas do administrador
description: Saiba mais sobre as práticas recomendadas de segurança para proteger suas permissões de armazenamento e gerenciamento do Commerce e como importar e exportar dados, gerenciar integrações e extensões e cuidar da manutenção de rotina.
exl-id: 9d22571e-9e09-4d1a-ba55-a889f094158d
TQID: https://experienceleague.adobe.com/TMdBCvfpmoU6cWCqaC8W4JJpIiyt4tXY7Lun7-p-rHA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: cc250cf1-34eb-4863-80d0-d170d45ea067
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 430
ht-degree: 6%

---

# Guia de sistemas de administração do Adobe Commerce

Este guia destina-se aos administradores de sistema e integradores que trabalham no Adobe Commerce e no Magento Open Source Admin. Ele fornece informações detalhadas sobre segurança do administrador, operações de manutenção e recursos em todo o sistema que oferecem suporte a atividades em várias funções organizacionais para seus negócios de comércio eletrônico. Ele pressupõe uma compreensão básica da configuração e funcionalidade principais do Commerce.

Este guia abrange:

| Assunto | Descrição |
| ------- | ----------- |
| [Introdução](introduction.md) | Visão geral dos sistemas e da função de integração em uma instância do Commerce. |
| [Menu do sistema](system-menu.md) | Use o menu [!UICONTROL System] para acessar ferramentas de importação e exportação de dados, gerenciamento de índice e cache do sistema, gerenciamento de permissões e conta de usuário, backups, notificações do sistema e variáveis personalizadas. |
| [Contas e permissões de administrador](permissions.md) | Gerencie as contas de usuário Admin e as funções usadas para conceder acesso às funções de armazenamento. |
| [Variáveis](variables-predefined.md) | As variáveis facilitam a personalização de modelos de email e de boletins informativos, além de outros tipos de conteúdo que oferecem suporte ao seu site e à experiência do cliente. |
| [Modelos de email](email-templates.md) | Os templates de email definem o layout, o conteúdo e a formatação das mensagens automatizadas enviadas pela loja. Eles são chamados de emails transacionais porque cada um está associado a um tipo específico de transação ou evento. |
| [Transferência de dados](data-transfer.md) | <ul><li>As ferramentas de importação e exportação permitem gerenciar vários registros em uma única operação. Você não pode apenas importar novos itens, mas também atualizar, substituir e excluir conjuntos existentes de produtos.</li><li>Exibir o status de sincronização de dados das entidades transferidas para os serviços conectados da Commerce a partir de [[!UICONTROL Data Management Dashboard]](data-dashboard.md).</li><li>Monitore o status de sincronização da exportação de feed de dados para os serviços SaaS da Commerce na página [[!UICONTROL Data Export Feed Sync Status]](data-feed-sync-status.md).</li></ul> |
| [Logs de ação](action-log.md) | Para o Adobe Commerce, os logs de ação capturam todas as alterações feitas por um usuário administrador que trabalha na sua loja. Isso permite rastrear todas as alterações feitas em sua loja. |
| Ferramentas | [!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} administradores do sistema têm uma coleção de ferramentas disponíveis: as [ferramentas de suporte](support.md) foram projetadas para identificar problemas conhecidos em seu sistema. As ferramentas do sistema fornecem suporte operacional para executar o gerenciamento de rotina do [índice](index-management.md) e do [cache](cache-management.md), [fazer backup do sistema](backups.md), gerenciar [operações agendadas](data-scheduled-import-export.md) e usar uma variedade de [ferramentas de desenvolvedor](developer-tools.md). |
| [Integrações](integrations.md) | Estabeleça a localização das credenciais do OAuth e forneça os URLs de redirecionamento para integrações de terceiros. |
| [Segurança](security.md) | Saiba mais sobre as ferramentas disponíveis para proteger seu armazenamento e seus dados, e as diretrizes para um plano de ação de segurança se você detectar um comprometimento. |

{style="table-layout:auto"}

## Documentação disponível

{{docs-links}}
