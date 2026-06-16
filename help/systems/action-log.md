---
title: Logs de ação
description: Saiba mais sobre logs de ação e como configurar ações registradas para ajudar você a rastrear todas as alterações feitas em sua loja.
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/UtJhP452hJXDyEyjxrknuF4WPoLza-UcnuWxP6ILtq8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 0%

---

# Logs de ação

{{ee-feature}}

O recurso Logs de ação registra (registra) todas as alterações feitas por um usuário administrador que trabalha na loja. Isso permite rastrear todas as alterações feitas em sua loja. O controle dessas alterações, juntamente com a configuração de [Permissões de administrador](permissions.md) para um usuário, pode ajudar a proteger seu armazenamento contra alterações indesejadas.

Para a maioria das ações de Administrador, as informações registradas incluem a ação, o nome do usuário, o sucesso ou falha da ação e a ID do objeto afetado pela ação. O endereço IP e a data também são registrados.

Por padrão, todas as ações do administrador são ativadas e registradas. Para configurar o Registro de ações do administrador, revise as opções e marque ou desmarque a caixa de seleção para cada tipo de ação. O Adobe Commerce registra somente os tipos marcados.

Exiba o [Relatório de Logs de Ação](action-log-report.md) para examinar as ações e os detalhes de administrador registrados.

![Configuração avançada - registro de ações do administrador](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

Para obter uma lista detalhada das definições de configuração, consulte [Arquivamento do Log de Ações do Administrador](../configuration-reference/advanced/system.md) na _Referência de Configuração_.

## Configurar ações do administrador para fazer logon

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL Admin]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Admin Actions Logging]** e faça o seguinte para cada ação:

   - Para habilitar o log de administrador para a ação, marque a caixa de seleção.
   - Para desativar o registro de Administrador para a ação, desmarque a caixa de seleção.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Arquivar log de ações do administrador

Os logs de ação do administrador podem ser arquivados por qualquer número de dias. Os arquivos também podem ser excluídos após uma duração especificada.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expanda **[!UICONTROL Admin Action Log Archiving]** e defina as opções:

   - **[!UICONTROL Logs Entry Lifetime, Days]** - Defina o número de dias para reter o log arquivado.
   - **[!UICONTROL Log Archiving Frequency]** - Definir a frequência de criação de arquivos mortos.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
