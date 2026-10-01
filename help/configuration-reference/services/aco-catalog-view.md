---
title: '[!UICONTROL Services] > Exibição do catálogo de ACO'
description: Revise e atualize as definições de configuração do Adobe Commerce Optimizer na página [!UICONTROL Services] > [!UICONTROL ACO Catalog View] do Administrador do Commerce.
feature: Configuration, Security
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: b32c28afffe75b3f684f0fef81bd61e9cdcb485a
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View]

Use essas configurações para controlar os tokens de acesso emitidos pelo [!DNL Adobe Commerce Optimizer Connector for B2B]. As vitrines usam esses tokens para autenticar em exibições de catálogo privado do Commerce Optimizer preenchidas com dados sincronizados de catálogos compartilhados personalizados configurados no Administrador.

{{config}}

![Administrador do Adobe Commerce mostrando as configurações de token de acesso da Exibição de Catálogo do ACO, com uma emissão de token e TTL de 3.600 segundos habilitada.](./assets/aco-catalog-view-access-token-config.png)<!-- zoom -->

## [!UICONTROL Access Token Configuration]

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| --- | --- | --- |
| [!UICONTROL Token TTL (seconds)] | Global | O número de segundos que um token de acesso permanece válido após ser gerado. Esta configuração é somente leitura no escopo padrão. Os valores configurados no escopo do site ou da visualização de loja são ignorados. O padrão é: 3600 segundos. |
| [!UICONTROL Issue Access Tokens] | Exibição da loja | Controla se a loja pode obter um token de acesso para uma exibição de catálogo. Quando definido como `No`, `Company.catalogViewContext` retorna a ID de exibição do catálogo, mas nenhum token de acesso, portanto, as vitrines não podem ser autenticadas para ler de [!DNL Adobe Commerce Optimizer] exibições do catálogo privado sincronizadas do Adobe Commerce. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [Sincronização de Exibição de Catálogo ACO](./aco-catalog-view-sync.md) — Configure como as exibições de catálogo são sincronizadas em [!DNL Adobe Commerce Optimizer]
> - [Monitoramento do Status de Sincronização da Exibição de Catálogo](../../systems/catalog-view-sync-status.md) — Monitorar a integridade da sincronização e reconciliar descompasso
