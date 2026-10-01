---
title: '[!UICONTROL Services] > Sincronização de Exibição de Catálogo ACO'
description: Revise as configurações na página [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync] do Administrador do Commerce.
feature: Configuration, Security
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
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
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync]

Use essas configurações para controlar como o [!DNL Adobe Commerce Optimizer Connector for B2B] sincroniza configurações de catálogo compartilhado B2B (exibição de catálogo, política, catálogo de preços e chave) no [!DNL Adobe Commerce Optimizer] e como ele resolve as diferenças de configuração entre os dois sistemas. Consulte [Monitoramento do Status de Sincronização da Exibição de Catálogo](../../systems/catalog-view-sync-status.md) para monitorar os resultados dessas configurações.

{{config}}

## [!UICONTROL Deletion]

![Exclusão](./assets/aco-catalog-view-sync-configuration.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| --- | --- | --- |
| [!UICONTROL Deletion Grace Period (days)] | Global | Período de retenção para dados de catálogo compartilhados. Especifica por quantos dias as exibições, as políticas e os metadados do catálogo compartilhado excluído são retidos antes de serem excluídos. O valor padrão é 7 dias. Defina como `0` para excluí-lo imediatamente. |

{style="table-layout:auto"}

## [!UICONTROL Creation]

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| --- | --- | --- |
| [!UICONTROL Creation Grace Period (days)] | Global | Número de dias que uma exibição de catálogo recém-registrada pode esperar que o [!DNL Adobe Commerce Optimizer Connector for B2B] conclua sua primeira sincronização das configurações de exibição de catálogo, política, catálogo de preços e chave, enquanto seu status é relatado como [!UICONTROL Pending]. Se o período de carência terminar sem uma sincronização bem-sucedida, o status será alterado para [!UICONTROL Failed]. Valor padrão: `1` |

{style="table-layout:auto"}

## [!UICONTROL Drift Reconciler]

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
| --- | --- | --- |
| [!UICONTROL Enabled] | Global | Executa o reconciliador de descompasso agendado para detectar e relatar diferenças entre a exibição de catálogo projetada de [!DNL Adobe Commerce] e a configuração de exibição de catálogo em [!DNL Adobe Commerce Optimizer]. Se `automatically repair drift` estiver habilitado, ele também tentará corrigir discrepâncias reparáveis. |
| [!UICONTROL Automatically Repair Drift] | Global | Quando definido como `Yes`, o reconciliador de descompasso agendado atualiza a configuração [!DNL Adobe Commerce Optimizer] para corresponder ao [!DNL Adobe Commerce] e sincroniza novamente a configuração. Quando definido como `No`, a execução só detecta e relata desvios. Entidades [!DNL Adobe Commerce Optimizer] órfãs são sempre relatadas, nunca removidas automaticamente. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [Exibição do Catálogo ACO](./aco-catalog-view.md) — Configurar tokens de acesso para leituras de vitrine de uma exibição do catálogo
> - [Monitoramento do Status de Sincronização da Exibição de Catálogo](../../systems/catalog-view-sync-status.md) — Monitore a integridade da sincronização e reconcilie desvios usando essas configurações
> - [Gerenciamento de Chaves de Acesso Restrito](../../systems/restricted-access-keys.md) — Gerencie as chaves de acesso atribuídas às exibições de catálogo sincronizadas
