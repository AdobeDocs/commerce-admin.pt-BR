---
title: Arquivo de log de ações
description: Saiba como configurar e exibir o arquivo de log de ações do administrador.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Arquivo de log de ações

{{ee-feature}}

O administrador [ações](action-log.md) O arquivo lista os arquivos de log CSV armazenados no servidor. Na configuração, você pode especificar por quanto tempo as entradas de log são armazenadas e com que frequência elas são arquivadas. Por padrão, o nome do arquivo inclui a data atual no formato ISO:  `yyyyMMddHH`

>[!NOTE]
>
>O arquivamento de registros requer um [trabalho cron](cron.md) a ser configurado.

## Configurar o arquivo de log

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Admin Actions Log Archiving]** e defina estas opções:

   - **[!UICONTROL Log Entry Lifetime, Days]** — Digite o número de dias que você deseja manter as entradas de log no banco de dados antes de serem removidas.
   - **[!UICONTROL Log Archiving Frequency]** — Defina como `Daily`, `Weekly`ou `Monthly`.

   ![Configuração avançada - arquivamento do log de ações do administrador](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada das definições de configuração, consulte [Arquivamento do Log de Ações do Administrador](../configuration-reference/advanced/system.md) no _Referência de configuração_.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Exibir o arquivo

No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![Arquivo de log de ações](./assets/action-log-archive.png){width="600" zoomable="yes"}
