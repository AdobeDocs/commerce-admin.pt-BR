---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: Revise as configurações no [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] página do Administrador do Commerce.
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 4%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

## [!UICONTROL General]

![Geral](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | Exibição da loja | Determina se o armazenamento pode ser usado com [!DNL New Relic] Relatórios. Opções: `Yes` / `No` |
| [!UICONTROL New Relic API URL] | Exibição da loja | O URL no qual as APIs do New Relic são implantadas. Por exemplo: `https://api.newrelic.com/deployments.xml` |
| URL da API do Insights | Exibição da loja | O URL onde as APIs do Insights são implantadas. Use o símbolo de porcentagem (%) para representar a ID da conta. Por exemplo: `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | Exibição da loja | A ID da conta atribuída ao seu [!DNL New Relic] conta. |
| [!UICONTROL New Relic Application ID] | Exibição da loja | A ID do aplicativo atribuída ao seu [!DNL New Relic] conta para a integração do Commerce. |
| [!UICONTROL New Relic API Key] | Exibição da loja | A chave atribuída a você para obter acesso ao [!DNL New Relic] API. |
| [!UICONTROL Insights API Key] | Exibição da loja | A chave atribuída a você para obter acesso aos Insights. |
| [!UICONTROL New Relic Application Name] | Exibição da loja | O nome que você atribuiu ao seu [!DNL New Relic] integração. |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | Exibição da loja | Uma opção para enviar dados de relatório coletados para a loja e o Administrador como aplicativos separados para a New Relic. Esta opção requer um nome inserido para o [!UICONTROL New Relic Application Name]. O recurso anexa o nome do aplicativo com um sublinhado aos dados do aplicativo coletados. Por exemplo: `MyStore_Adminhtml`, `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | Exibição da loja | Determina se [!DNL New Relic] os relatórios podem ser executados de acordo com a programação com [Cron](../../systems/cron.md). Opções: `Yes` / `No` |

{style="table-layout:auto"}
