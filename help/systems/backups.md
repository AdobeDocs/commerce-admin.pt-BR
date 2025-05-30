---
title: Backups do sistema
description: Saiba como criar e agendar backups de sistema, incluindo o sistema de arquivos, o banco de dados e os arquivos de mídia.
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# Backups do sistema

O Adobe Commerce e o Magento Open Source oferecem a capacidade de fazer backup de diferentes partes do sistema — como o sistema de arquivos, o banco de dados e os arquivos de mídia — e de reverter automaticamente. Um registro para cada backup aparece na grade na página _Backups_. A exclusão de um registro da lista também exclui o arquivo arquivado. Os arquivos de backup do banco de dados são compactados usando o formato GZ. Para os backups de sistema e de banco de dados e de mídia, o formato TGZ é usado. Como prática recomendada, você deve restringir o acesso às ferramentas de backup e fazer backup antes de instalar extensões e atualizações.

- **Restringir o acesso às ferramentas de backup.** O acesso à ferramenta de gerenciamento de backups e reversões pode ser restrito configurando [funções de usuário](permissions-user-roles.md) para os recursos de backup e reversão. Para restringir o acesso, deixe a caixa de seleção correspondente desmarcada. Para conceder acesso a recursos de rollback, você também deve conceder acesso a recursos de backup.

- **Faça backup antes de instalar extensões e atualizações.** Sempre faça um backup antes de instalar uma extensão ou atualização.

{{$include /help/_includes/backups-note.md}}

## Habilitar e agendar backups

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Backup Settings]**.

1. Defina **[!UICONTROL Enabled Schedule Backup]** como `Yes`.

1. Para programar os backups automáticos, defina as opções de programação:

   - Defina **[!UICONTROL Enabled Schedule Backup]** como `Yes`.
   - Defina **[!UICONTROL Scheduled Backup Type]** como o tipo de backup a ser executado no intervalo agendado.
   - Defina **[!UICONTROL Start Time]** como a hora do dia para executar a operação de backup.
   - Defina **[!UICONTROL Frequency]** como `Daily`, `Weekly` ou `Monthly`.
   - Defina **[!UICONTROL Maintenance Mode]** como `Yes`.

   ![Configuração avançada - backups](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Criar um backup

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Backups]**.

1. No canto superior direito, clique no tipo de backup que deseja criar:

   - **[!UICONTROL System Backup]** - Cria um backup completo do banco de dados e do sistema de arquivos. Durante o processo, você pode optar por incluir a pasta de mídia no backup.

   - **[!UICONTROL Database and Media Backup]** - Cria um backup do banco de dados e da pasta de mídia.

   - **[!UICONTROL Database Backup]** - Cria um backup do banco de dados.

   ![Ferramentas do sistema - backups](./assets/tools-backups.png){width="600" zoomable="yes"}

1. Para colocar o armazenamento no modo de manutenção durante o backup, marque a caixa de seleção.

   Quando o backup é concluído, o modo de manutenção é desativado automaticamente.

1. Para um backup de sistema, marque a caixa de seleção **[!UICONTROL Include Media folder to System Backup]** para incluir a pasta de mídia.

1. Quando solicitado, confirme a ação.


