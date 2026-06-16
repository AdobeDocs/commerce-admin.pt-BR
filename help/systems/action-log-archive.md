---
title: Arquivo de log de ações
description: Saiba como configurar e exibir o arquivo de log de ações do administrador.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/xgyeoO5XJFZPopM9bsIn2oOtrxl4fyuEY2du5ryXeTY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 0%

---

# Arquivo de log de ações

{{ee-feature}}

O arquivo morto Admin [actions](action-log.md) lista os arquivos de log CSV armazenados no servidor. Na configuração, você pode especificar por quanto tempo as entradas de log são armazenadas e com que frequência elas são arquivadas. Por padrão, o nome de arquivo inclui a data atual no formato ISO: `yyyyMMddHH`

>[!NOTE]
>
>O arquivamento de logs requer a configuração de um [trabalho do cron](cron.md).

## Configurar o arquivo de log

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Admin Actions Log Archiving]** e defina estas opções:

   - **[!UICONTROL Log Entry Lifetime, Days]** — Digite o número de dias que você deseja manter as entradas de log no banco de dados antes de elas serem removidas.
   - **[!UICONTROL Log Archiving Frequency]** — Defina como `Daily`, `Weekly` ou `Monthly`.

   ![Configuração avançada - arquivamento do log de ações do administrador](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada das definições de configuração, consulte [Arquivamento do Log de Ações do Administrador](../configuration-reference/advanced/system.md) na _Referência de Configuração_.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Exibir o arquivo

Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![Arquivo morto do log de ações](./assets/action-log-archive.png){width="600" zoomable="yes"}
