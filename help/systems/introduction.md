---
title: Introdução aos sistemas de administração
description: Saiba mais sobre as ferramentas e funções do sistema que o administrador da loja pode usar para gerenciar com eficiência os sites, dados, integrações e usuários administradores.
exl-id: 52792a89-8f6f-4230-9a04-e193b3943410
TQID: https://experienceleague.adobe.com/E-6P-9RyoWsRXfdnU-nT4sEMLd3Pmlkynvd1q2Dqpms
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: cc250cf1-34eb-4863-80d0-d170d45ea067
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 471
ht-degree: 0%

---

# Introdução aos sistemas de administração

O Administrador da loja é o back office seguro onde os comerciantes configuram produtos e promoções, gerenciam pedidos e executam outras tarefas administrativas. Todas as tarefas básicas de configuração e operações de gerenciamento de armazenamento são executadas pelo Administrador. Também há funções que oferecem suporte a vários recursos de loja que os administradores podem gerenciar para suas organizações.

## Variáveis e comunicação com o cliente

As variáveis são informações que podem ser criadas uma vez e usadas em vários lugares. Seu armazenamento inclui muitas variáveis predefinidas que podem ser facilmente usadas para personalizar modelos de [email](email-templates.md) e [informativo](../merchandising-promotions/newsletter-template.md) e outros tipos de [conteúdo](../content-design/introduction.md#content). Você também pode criar variáveis personalizadas para incorporar informações específicas às suas necessidades.

- [Variáveis predefinidas](variables-predefined.md)
- [Variáveis personalizadas](variables-custom.md)

Uma das tarefas a serem concluídas antes de iniciar sua loja é revisar os modelos de email usados para todas as comunicações enviadas pela loja para garantir que eles reflitam a sua marca. Isso inclui a personalização de email e [modelos de boletim informativo](../merchandising-promotions/newsletter-template.md), faturas e guias de remessa do PDF. Também inclui a personalização do conteúdo com variáveis e [marcas de marcação](markup-tags.md).

## Gerenciamento de operações

O Administrador também oferece suporte a várias tarefas para que os administradores de sistemas gerenciem os usuários Administradores em sua organização e operem a loja. Elas incluem as seguintes ferramentas:

- **Permissões e contas de usuário administrador** - Gerenciar [contas de usuário](permissions-users-all.md) do Administrador, bem como as [funções e permissões](permissions-user-roles.md) associadas que controlam seu acesso a sites e áreas funcionais no Administrador.
- **Sessões de administrador e restrições de site** - Examine as práticas recomendadas de [segurança](security.md) e saiba como gerenciar sessões de administrador e credenciais, implementar o CAPTCHA e gerenciar restrições de site.
- [!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} **Ferramentas do sistema** - Executar operações de gerenciamento de rotina [índice](index-management.md) e [cache](cache-management.md), [fazer backup](backups.md) do sistema, gerenciar [operações agendadas](data-scheduled-import-export.md) e usar uma variedade de [ferramentas de desenvolvedor](developer-tools.md).
- **Transferência de Dados** - Use as ferramentas de [transferência de dados](data-transfer.md) para importar e exportar dados, bem como gerenciar dados de produto, preço, cliente e alíquota do imposto.
- **Integrações** - Estabeleça o local das credenciais do OAuth e a URL de redirecionamento para [integrações de terceiros](integrations.md) e identifique os recursos de API disponíveis.
- **Logs de ação** - ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Acesse os registros ([logs de ação](action-log.md)) das alterações feitas pelos usuários administradores que trabalham no seu armazenamento.
- [!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} **Ferramentas de suporte** - ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) [Relatórios do Sistema](support.md#access-system-reports)) foram projetadas para identificar problemas conhecidos em seu sistema. Eles podem ser usados como um recurso durante os processos de desenvolvimento e otimização e como uma ferramenta de diagnóstico para ajudar nossa equipe de suporte a identificar e resolver problemas.
