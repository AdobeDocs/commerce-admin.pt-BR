---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Revise as configurações no [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] página do Administrador do Commerce.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Essas configurações estão disponíveis quando [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) O está instalado.

![Configurações do Sales Channel](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Campo | [Escopo](../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Global | Opções:<br/><br/>**`Once Daily`**: selecione esta opção para limpar o histórico de atividades da loja uma vez por dia.<br/><br/>**`Once Weekly`**: selecione essa opção para limpar o histórico de atividades da loja uma vez por semana.<br/><br/>**`Once Monthly`**: (padrão) selecione essa opção para limpar o histórico de atividades da loja uma vez por mês. |
| [!UICONTROL Background Tasks (CRON) Source] | Global | Selecionar `Magento CRON` para especificar que as [!DNL Amazon Sales Channel] O usa suas configurações de cron do Commerce para determinar intervalos de sincronização de dados e comunicação com a Central de Vendas da Amazon. |
| [!UICONTROL Enable Debug Logging] | Global | Selecionar `Enabled` para coletar dados adicionais de sincronização quando a solução de problemas for necessária.<br/><br/>Essa opção está desativada por padrão e só deve ser ativada quando necessário para a solução de problemas, pois o registro contínuo afeta negativamente o desempenho. Se ativado para solução de problemas, deve ser desativado ao concluir.<br/><br/>**_Nota _**: o registro de Sales Channel do Amazon é gravado no `/var/log/channel_amazon.log` arquivo e pode ser visualizado em [modo de desenvolvedor](../systems/developer-tools.md#operation-modes). |
| [!UICONTROL Read-Only Mode] | Global | Selecionar `Enabled` para bloquear todas as solicitações de API que mudam de estado de saída. As alterações potenciais são salvas, mas não enviadas, até que o modo somente leitura seja desativado. Para iniciar as transferências de dados novamente, selecione `Disabled`.<br/><br/>Quando um banco de dados é migrado para uma nova cópia da instância (detectada quando o URL de um armazenamento muda na configuração), o modo somente leitura é ativado automaticamente.<br/><br/>Ele foi projetado para uso em cópias da instância de produção, como _Estágios_ ou _QA_, e não devem ser usados na instância de produção.<br/><br/>**_Nota _**: o cache de configuração deve ser limpo para [!UICONTROL Read-Only Mode] para ativar. |

{:style=&quot;table-layout:auto&quot;}
