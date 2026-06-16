---
title: '[!UICONTROL Sales Channels] > [!UICONTROL Global Settings]'
description: Revise as configurações na página [!UICONTROL Sales Channels] > [!UICONTROL Global Settings] do Administrador do Commerce.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
TQID: https://experienceleague.adobe.com/jnjAspEdJbx3unjmoqgH12JEiLz4ThbgFGeFOArOonU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 225
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Estas configurações estão disponíveis quando o [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html?lang=pt-BR) é instalado.

![Configurações do Sales Channel](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Campo | [Escopo](../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Global | Opções:<br/><br/>**`Once Daily`**: selecione esta opção para limpar o histórico de atividades da loja uma vez por dia.<br/><br/>**`Once Weekly`**: selecione esta opção para limpar o histórico de atividades da loja uma vez por semana.<br/><br/>**`Once Monthly`**: (Padrão) selecione esta opção para limpar o histórico de atividades da loja uma vez por mês. |
| [!UICONTROL Background Tasks (CRON) Source] | Global | Selecione `Magento CRON` para especificar que o [!DNL Amazon Sales Channel] use suas configurações de cron do Commerce para determinar os intervalos de comunicação e sincronização de dados com a Central de Vendas do Amazon. |
| [!UICONTROL Enable Debug Logging] | Global | Selecione `Enabled` para coletar dados de sincronização adicionais quando a solução de problemas for necessária.<br/><br/>Essa opção está desabilitada por padrão e só deve ser habilitada quando necessária para a solução de problemas, pois o logon contínuo afeta negativamente o desempenho. Se ativado para solução de problemas, deve ser desativado ao concluir. |
| [!UICONTROL Read-Only Mode] | Global | Selecione `Enabled` para bloquear todas as solicitações de API que mudam de estado de saída. As alterações potenciais são salvas, mas não enviadas, até que o modo somente leitura seja desativado. Para iniciar as transferências de dados novamente, selecione `Disabled`.<br/><br/>Quando um banco de dados é migrado para uma nova cópia da instância (detectado quando a URL de um armazenamento muda na configuração), o modo somente leitura é habilitado automaticamente.<br/><br/>Isso foi projetado para uso em cópias da instância de produção, como _Preparo_ ou _QA_, e não deve ser usado na instância de produção.<br/><br/>**_Observação _**: o cache de configuração deve ser limpo para que o [!UICONTROL Read-Only Mode] seja habilitado. |

{style="table-layout:auto"}
