---
title: '[!UICONTROL Services] > Teclas de Acesso Restrito de ACO'
description: Revise as configurações na página [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys] do Administrador do Commerce.
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
source-git-commit: df30ce0e482be65523f346d578be481b3ff893c8
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]

Use essa configuração para controlar o período de expiração padrão que o [!DNL Adobe Commerce Optimizer Connector for B2B] aplica às chaves de acesso restritas que ele provisiona para exibições de catálogo compartilhado B2B. Para criar, atribuir e excluir essas chaves, consulte [Gerenciamento de Chaves de Acesso Restrito](../../systems/restricted-access-keys.md).

>[!NOTE]
>
>Esta página se aplica ao conector. As instâncias provisionadas com o Composable Catalog Data Model (CCDM) sincronizam dados nativamente e não usam o conector. Consulte [Serviços de merchandising com CCDM](/help/optimizer/overview.md).

{{config}}

## [!UICONTROL Provisioning]

![Provisionamento](./assets/optimizer-restricted-access-key-config.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| --- | --- | --- |
| [!UICONTROL Default key expiry (days)] | Global | Período de validade para chaves de acesso restrito recém-provisionadas. [!DNL Adobe Commerce Optimizer] requer uma data de expiração de pelo menos um minuto em cada chave e exclui chaves expiradas das leituras de gateway, portanto, um valor de pelo menos um dia é sempre aplicado. Valor padrão: `36500` |

{style="table-layout:auto"}

>[!NOTE]
>
>A expiração padrão está definida como um período de expiração longo porque a rotação de chaves automática ainda não está disponível. Consulte [Seleção e rotação de chaves](../../systems/restricted-access-keys.md#key-selection-and-rotation).

>[!MORELIKETHIS]
>
> - [Exibição do Catálogo ACO](./aco-catalog-view.md) — Configure os tokens de acesso de vitrine para exibições de catálogo
> - [Gerenciamento de Chaves de Acesso Restrito](../../systems/restricted-access-keys.md) — Criar, atribuir e excluir chaves de acesso restrito
> - [Monitoramento do Status de Sincronização da Exibição de Catálogo](../../systems/catalog-view-sync-status.md) — Monitorar chaves perto da expiração
