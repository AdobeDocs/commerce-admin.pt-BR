---
title: Ferramentas de suporte
description: Saiba mais sobre as ferramentas de suporte fornecidas que você pode usar para identificar problemas em seu sistema.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
source-git-commit: 97eeb733836f0336401664c5cfb3df2b9f2f2ccf
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Ferramentas de suporte

{{ee-feature}}

As ferramentas de suporte foram criadas para identificar problemas conhecidos no sistema. Eles podem ser usados como um recurso durante os processos de desenvolvimento e otimização e como uma ferramenta de diagnóstico para ajudar nossa equipe de suporte a identificar e resolver problemas.

## Coletor de dados

O coletor de dados coleta as informações sobre seu sistema necessárias para que nossa equipe de suporte solucione problemas na instalação do Adobe Commerce. O backup criado leva vários minutos para ser concluído e inclui um dump de código e de banco de dados. Os dados podem ser exportados para um arquivo XML CSV ou do Excel.

![Sistema - Coletor de dados](./assets/data-collector.png){width="600" zoomable="yes"}

### Executar o coletor de dados

1. No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. No canto superior direito, clique em **[!UICONTROL New Backup]**.

   O backup leva alguns minutos para ser gerado. É possível monitorar os resultados do processamento clicando em **[!UICONTROL Refresh Status]**. Quando concluído, o backup é exibido no _[!UICONTROL Data Collector]_grade.

1. Para exibir um log com os detalhes do backup, faça o seguinte:

   - No _[!UICONTROL Action]_coluna, selecione **[!UICONTROL Show Log]**.

   - Clique em **[!UICONTROL Back]** para retornar à grade.

   ![log do coletor de dados](./assets/data-collector-log.png){width="600" zoomable="yes"}

### Exportar dados de backup

1. Na primeira coluna, marque a caixa de seleção do backup a ser exportado.

1. Use o **[!UICONTROL Export]** para escolher o formato dos dados de exportação.

   ![Formato de exportação](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Acesse o arquivo do local de download do navegador da Web e **[!UICONTROL Save]** o mesmo.

### Baixar dados de backup

Depois que o backup é gerado, é possível baixar a cópia dos dados do Code e do DB.

1. Localize a entidade de backup necessária na grade.

1. Verifique se ele tem um `Complete` status.

1. Clique no nome da entidade em _[!UICONTROL Code Dump]_ou_[!UICONTROL DB Dump]_ colunas.

O processo de download deve iniciar automaticamente.

## Excluir dados de backup

1. No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Localize e selecione os dados de backup a serem excluídos.

1. No _[!UICONTROL Action]_clique em **[!UICONTROL Delete]**.

1. Para confirmar a ação, clique em **[!UICONTROL OK]**.

## Relatórios do sistema

A ferramenta de relatório do sistema oferece a capacidade de tirar instantâneos periódicos completos ou parciais do sistema e salvá-los para referência futura. Você pode comparar as configurações de desempenho antes e depois dos ciclos de desenvolvimento de código ou as alterações nas configurações do servidor. A ferramenta de relatório do sistema pode reduzir drasticamente o tempo gasto na preparação e envio das informações exigidas pelo suporte para iniciar uma investigação.

Na grade Relatórios do sistema, é possível visualizar e baixar relatórios existentes, excluir relatórios e criar relatórios.

### Acessar relatórios do sistema

No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Administrador - Relatórios do sistema](./assets/reports.png){width="600" zoomable="yes"}

### Gerar um relatório

1. Clique em **[!UICONTROL New Report]**.

1. No **[!UICONTROL Groups]** selecione cada conjunto de informações que deseja incluir no relatório. Por padrão, todos os grupos são selecionados.

   ![Relatório do sistema - selecionar grupos](./assets/report-create.png){width="600" zoomable="yes"}

1. No canto superior direito, clique em **[!UICONTROL Create]**.

   O relatório pode levar alguns minutos para ser gerado, dependendo do número de tipos de relatório selecionados. Quando o relatório estiver pronto, ele será exibido na parte superior da grade com a data e a hora geradas.

### Exibir informações do módulo

Você pode encontrar informações úteis sobre módulos instalados.

**_Para exibir informações de relatório para cada módulo instalado:_**

1. No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Clique em **[!UICONTROL New Report]**.
1. Selecionar `Modules` do **[!UICONTROL Groups]** lista.
1. Clique em **[!UICONTROL Create]**.
1. Depois que o relatório for gerado, clique em **[!UICONTROL Select]** e depois **[!UICONTROL View]** para ver todas as versões do módulo.
1. Clique em **[!UICONTROL Download]** para baixar o relatório.

### Gerenciar relatórios do sistema

No **[!UICONTROL Action]** da grade, selecione uma das seguintes opções:

- `View` : Use essa função para exibir os detalhes do relatório.
- `Delete` - Use essa função para excluir o relatório gerado da lista.
- `Download` : Use essa função para salvar o relatório como um arquivo HTML.

### Exibir detalhes do relatório do sistema

1. Para o relatório necessário, selecione **[!UICONTROL View]** no _[!UICONTROL Actions]_coluna.

1. No painel esquerdo, expanda ![Seletor de expansão](../assets/icon-display-expand.png) cada seção do relatório para exibir os detalhes.

   ![Informações gerais de relatório do sistema](./assets/report-information.png){width="600" zoomable="yes"}

### Relatórios de sistema disponíveis

| Grupo de relatório | Informações incluídas |
| ------------ | -------------------- |
| [!UICONTROL General] | Versão do Adobe Commerce<br>Contagem de dados<br>Status do cache<br>Status do índice |
| [!UICONTROL Environment] | Informações do ambiente<br>Status do MySQL |
| [!UICONTROL Data] | Categorias duplicadas por chave de URL<br>Duplicar produtos por chave de URL<br>Produtos duplicados por SKU<br>Pedidos Duplicados Por Id De Incremento<br>Usuários Duplicados Por Email<br>Dados de Categorias Corrompidos |
| [!UICONTROL Modules] | Lista de módulos personalizados<br>Lista de módulos desativados<br>Lista de Todos os Módulos |
| [!UICONTROL Configuration] | Configuração<br>Dados de `app/etc/env.php`<br>Métodos de envio<br>Métodos de pagamento<br>Matriz de Funcionalidade de Pagamentos |
| [!UICONTROL Logs] | Arquivos de log<br>Principais Mensagens do Sistema<br>Principais mensagens do sistema de hoje<br>Principais mensagens de depuração<br>Principais mensagens de depuração de hoje<br>Principais Mensagens de Exceção<br>Principais Mensagens de Exceção de Hoje |
| [!UICONTROL Attributes] | Atributos de EAV Definidos pelo Usuário<br>Novos atributos de EAV<br>Tipos de entidade<br>Todos os atributos de EAV<br>Atributos EAV da Categoria<br>Atributos EAV do Produto<br>Atributos de EAV do Cliente<br>Atributo EAV do Endereço do Cliente<br>Atributos EAV do Item de RMA |
| [!UICONTROL Events] | Eventos globais personalizados<br>Eventos de administração personalizados<br>Eventos de front-end personalizados<br>Eventos Doc personalizados<br>Eventos Personalizados Do Crontab<br>Eventos REST personalizados<br>Eventos SOAP personalizados<br>Eventos globais principais<br>Eventos principais de administração<br>Eventos de front-end principais<br>Eventos Doc principais<br>Eventos Crontab Principais<br>Eventos REST principais<br>Eventos SOAP principais<br>Todos os eventos globais<br>Todos os eventos de administração<br>Todos os eventos de front-end<br>Todos os eventos Doc<br>Todos os eventos REST<br>Todos os eventos SOAP<br>Todos os eventos Crontab |
| [!UICONTROL Cron] | Cronogramas Cron por código de status<br>Cronogramas Cron por código de trabalho<br>Erros na fila de cronogramas Cron<br>Lista de Cronogramas Cron<br>Trabalhos Cron Globais Personalizados<br>Tarefas Cron configuráveis personalizadas<br>Principais trabalhos Cron globais<br>Trabalhos Core Configurable Cron<br>Todos os trabalhos Cron globais<br>Todos Os Trabalhos Do Cron Configuráveis |
| [!UICONTROL Design] | Lista de temas do Adminhtml<br>Lista de temas de front-end |
| [!UICONTROL Stores] | Árvore do site<br>Lista de Sites<br>Lista de lojas<br>Lista de exibições da loja |
| Conector OMS <br>_(visível com a integração do OMS)_ | Versão do conector<br>Monitoramento do conector<br>Resultados do processamento de mensagens |

{style="table-layout:auto"}
