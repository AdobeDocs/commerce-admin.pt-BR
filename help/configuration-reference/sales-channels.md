---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Revise as configurações na página [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] do Administrador do Commerce.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Estas configurações estão disponíveis quando o [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html?lang=pt-BR) é instalado.

![Configurações do Sales Channel](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Campo | [Escopo](../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Global | Opções:<br/><br/>**`Once Daily`**: selecione esta opção para limpar o histórico de atividades da loja uma vez por dia.<br/><br/>**`Once Weekly`**: selecione esta opção para limpar o histórico de atividades da loja uma vez por semana.<br/><br/>**`Once Monthly`**: (padrão) selecione essa opção para limpar o histórico de atividades da loja uma vez por mês. |
| [!UICONTROL Background Tasks (CRON) Source] | Global | Selecione `Magento CRON` para especificar que o [!DNL Amazon Sales Channel] use suas configurações de cron do Commerce para determinar os intervalos de comunicação e sincronização de dados com a Central de Vendas do Amazon. |
| [!UICONTROL Enable Debug Logging] | Global | Selecione `Enabled` para coletar dados de sincronização adicionais quando a solução de problemas for necessária.<br/><br/>Essa opção está desabilitada por padrão e só deve ser habilitada quando necessária para a solução de problemas, pois o logon contínuo afeta negativamente o desempenho. Se ativado para solução de problemas, deve ser desativado ao concluir. |
| [!UICONTROL Read-Only Mode] | Global | Selecione `Enabled` para bloquear todas as solicitações de API que mudam de estado de saída. As alterações potenciais são salvas, mas não enviadas, até que o modo somente leitura seja desativado. Para iniciar as transferências de dados novamente, selecione `Disabled`.<br/><br/>Quando um banco de dados é migrado para uma nova cópia da instância (detectada quando a URL de um repositório muda na configuração), o modo somente leitura é habilitado automaticamente.<br/><br/>Isso foi projetado para uso em cópias da instância de produção, como _Preparo_ ou _Controle de qualidade_, e não deve ser usado na instância de produção.<br/><br/>**_Observação _**: o cache de configuração deve ser limpo para que [!UICONTROL Read-Only Mode] seja habilitado. |

{style="table-layout:auto"}
