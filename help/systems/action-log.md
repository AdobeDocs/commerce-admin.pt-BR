---
title: Logs de ação
description: Saiba mais sobre logs de ação e como configurar ações registradas para ajudar você a rastrear todas as alterações feitas em sua loja.
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Logs de ação

{{ee-feature}}

O recurso Logs de ação registra (registra) todas as alterações feitas por um usuário administrador que trabalha na loja. Isso permite rastrear todas as alterações feitas em sua loja. Rastrear essas alterações, juntamente com a configuração [Permissões de administrador](permissions.md) para um usuário, o pode ajudar a proteger seu armazenamento contra alterações indesejadas.

Para a maioria das ações de Administrador, as informações registradas incluem a ação, o nome do usuário, o sucesso ou falha da ação e a ID do objeto afetado pela ação. O endereço IP e a data também são registrados.

Por padrão, todas as ações do administrador são ativadas e registradas. Para configurar o Registro de ações do administrador, revise as opções e marque ou desmarque a caixa de seleção para cada tipo de ação. O Adobe Commerce registra somente os tipos marcados.

Exibir o [Relatório de Logs de Ação](action-log-report.md) para revisar ações e detalhes de administradores registrados.

![Configuração avançada - registro de ações do administrador](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

Para obter uma lista detalhada das definições de configuração, consulte [Arquivamento do Log de Ações do Administrador](../configuration-reference/advanced/system.md) no _Referência de configuração_.

## Configurar ações do administrador para fazer logon

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL Admin]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Admin Actions Logging]** e faça o seguinte para cada ação:

   - Para habilitar o log de administrador para a ação, marque a caixa de seleção.
   - Para desativar o registro de Administrador para a ação, desmarque a caixa de seleção.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Arquivar log de ações do administrador

Os logs de ação do administrador podem ser arquivados por qualquer número de dias. Os arquivos também podem ser excluídos após uma duração especificada.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expandir **[!UICONTROL Admin Action Log Archiving]** e defina as opções:

   - **[!UICONTROL Logs Entry Lifetime, Days]** - Defina o número de dias para reter o log arquivado.
   - **[!UICONTROL Log Archiving Frequency]** - Definir a frequência de criação de arquivos.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
