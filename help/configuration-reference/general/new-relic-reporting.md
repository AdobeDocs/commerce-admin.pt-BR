---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: Revise as configurações na página [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] do Administrador do Commerce.
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

>[!NOTE]
>Essas opções de configuração não se aplicam ao Adobe Commerce na infraestrutura em nuvem.
>
>Se você estiver no plano Pro, o New Relic já está [pré-configurado e habilitado por padrão](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Se você estiver no plano Inicial, conclua as [etapas de configuração do New Relic](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) que fazem parte do processo de instalação.

## [!UICONTROL General]

![Geral](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/en/docs/commerce-admin/start/reporting/new-relic-reporting) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | Exibição da loja | Determina se seu armazenamento pode ser usado com Relatórios do [!DNL New Relic]. Opções: `Yes` / `No` |
| [!UICONTROL New Relic API URL] | Exibição da loja | O URL no qual as APIs do New Relic são implantadas. Por exemplo: `https://api.newrelic.com/deployments.xml` |
| URL da API do Insights | Exibição da loja | O URL onde as APIs do Insights são implantadas. Use o símbolo de porcentagem (%) para representar a ID da conta. Por exemplo: `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | Exibição da loja | A ID de conta atribuída à sua conta [!DNL New Relic]. |
| [!UICONTROL New Relic Application ID] | Exibição da loja | A ID do aplicativo atribuída à sua conta do [!DNL New Relic] para integração com o Commerce. |
| [!UICONTROL New Relic API Key] | Exibição da loja | A chave atribuída a você para obter acesso à API [!DNL New Relic]. |
| [!UICONTROL Insights API Key] | Exibição da loja | A chave atribuída a você para obter acesso aos Insights. |
| [!UICONTROL New Relic Application Name] | Exibição da loja | O nome que você atribuiu à integração do [!DNL New Relic]. |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | Exibição da loja | Uma opção para enviar dados de relatório coletados para a loja e o Administrador como aplicativos separados para a New Relic. Esta opção requer um nome inserido para o [!UICONTROL New Relic Application Name]. O recurso anexa o nome do aplicativo com um sublinhado aos dados do aplicativo coletados. Por exemplo: `MyStore_Adminhtml`, `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/cron) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | Exibição da loja | Determina se os relatórios do [!DNL New Relic] podem ser executados de acordo com o cronograma com [Cron](../../systems/cron.md). Opções: `Yes` / `No` |

{style="table-layout:auto"}
