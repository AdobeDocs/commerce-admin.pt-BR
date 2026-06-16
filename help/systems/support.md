---
title: Ferramentas de suporte
description: Saiba mais sobre as ferramentas de suporte fornecidas que você pode usar para identificar problemas em seu sistema.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/bS1CIJI9ZXybrYA-EgekVKjXQhywA6jdpWOM-bvw4Mc
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c1256247-af4b-46d8-9dca-0c654ecfa157id: cc250cf1-34eb-4863-80d0-d170d45ea067id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 566
ht-degree: 0%

---

# Ferramentas de suporte

{{ee-feature}}

As ferramentas de suporte foram criadas para identificar problemas conhecidos no sistema. Eles podem ser usados como um recurso durante os processos de desenvolvimento e otimização e como uma ferramenta de diagnóstico para ajudar nossa equipe de suporte a identificar e resolver problemas.

## Relatórios do sistema

A ferramenta de relatório do sistema oferece a capacidade de tirar instantâneos periódicos completos ou parciais do sistema e salvá-los para referência futura. Você pode comparar as configurações de desempenho antes e depois dos ciclos de desenvolvimento de código ou as alterações nas configurações do servidor. A ferramenta de relatório do sistema pode reduzir drasticamente o tempo gasto na preparação e envio das informações exigidas pelo suporte para iniciar uma investigação.

Na grade Relatórios do sistema, é possível visualizar e baixar relatórios existentes, excluir relatórios e criar relatórios.

### Acessar relatórios do sistema

Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Administrador - Relatórios do sistema](./assets/reports.png){width="600" zoomable="yes"}

### Gerar um relatório

1. Clique em **[!UICONTROL New Report]**.

1. Na lista **[!UICONTROL Groups]**, selecione cada conjunto de informações que deseja incluir no relatório. Por padrão, todos os grupos são selecionados.

   ![Relatório do sistema - selecionar grupos](./assets/report-create.png){width="600" zoomable="yes"}

1. No canto superior direito, clique em **[!UICONTROL Create]**.

   O relatório pode levar alguns minutos para ser gerado, dependendo do número de tipos de relatório selecionados. Quando o relatório estiver pronto, ele será exibido na parte superior da grade com a data e a hora geradas.

### Exibir informações do módulo

Você pode encontrar informações úteis sobre módulos instalados.

**_Para exibir informações de relatório para cada módulo instalado:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Clique em **[!UICONTROL New Report]**.
1. Selecione `Modules` na lista **[!UICONTROL Groups]**.
1. Clique em **[!UICONTROL Create]**.
1. Depois que o relatório for gerado, clique em **[!UICONTROL Select]** e depois em **[!UICONTROL View]** para ver todas as versões do módulo.
1. Clique em **[!UICONTROL Download]** para baixar o relatório.

### Gerenciar relatórios do sistema

Na coluna **[!UICONTROL Action]** da grade, selecione uma das seguintes opções:

- `View` - Use esta função para exibir os detalhes do relatório.
- `Delete` - Use esta função para excluir o relatório gerado da lista.
- `Download` - Use essa função para salvar o relatório como um arquivo HTML.

### Exibir detalhes do relatório do sistema

1. Para o relatório que você precisa, selecione **[!UICONTROL View]** na coluna _[!UICONTROL Actions]_.

1. No painel esquerdo, expanda ![Seletor de expansão](../assets/icon-display-expand.png) cada seção do relatório para exibir os detalhes.

   ![Informações gerais sobre o relatório do sistema](./assets/report-information.png){width="600" zoomable="yes"}

### Relatórios de sistema disponíveis

| Grupo de relatório | Informações incluídas |
| ------------ | -------------------- |
| [!UICONTROL General] | Versão do Adobe Commerce<br>Contagem de Dados<br>Status do Cache<br>Status do Índice |
| [!UICONTROL Environment] | Informações do ambiente<br>Status do MySQL |
| [!UICONTROL Data] | Categorias Duplicadas Por Chave De URL<br>Produtos Duplicados Por Chave De URL<br>Produtos Duplicados Por SKU<br>Pedidos Duplicados Por Id De Incremento<br>Usuários Duplicados Por Email<br>Dados De Categorias Corrompidas |
| [!UICONTROL Modules] | Lista de Módulos Personalizados<br>Lista de Módulos Desabilitados<br>Lista de Todos os Módulos |
| [!UICONTROL Configuration] | Configuração<br>Dados de `app/etc/env.php`<br>Métodos de Envio<br>Métodos de Pagamento<br>Matriz de Funcionalidade de Pagamentos |
| [!UICONTROL Logs] | Arquivos de Log<br>Principais Mensagens do Sistema<br>Principais Mensagens do Sistema de Hoje<br>Principais Mensagens de Depuração<br>Principais Mensagens de Hoje<br>Principais Mensagens de Exceção<br>Principais Mensagens de Hoje |
| [!UICONTROL Attributes] | Atributos EAV Definidos pelo Usuário<br>Novos Atributos EAV<br>Tipos de Entidade<br>Todos os Atributos EAV<br>Atributos EAV de Categoria<br>Atributos EAV de Produto<br>Atributos EAV de Cliente<br>Atributo EAV de Endereço de Cliente<br>Atributos EAV de Item RMA |
| [!UICONTROL Events] | Eventos Globais Personalizados<br>Eventos Personalizados De Administrador<br>Eventos Personalizados De Front-End<br>Eventos Personalizados De Documento<br>Eventos Personalizados Do Crontab<br>Eventos Personalizados De REST<br>Eventos Personalizados Do SOAP<br>Eventos Globais Principais<br>Eventos Principais De Administrador<br>Eventos Principais De Front-End<br>Eventos Principais De Documento<br>Eventos Principais Do Crontab<br>Eventos Principais Do REST<br>Eventos Principais Do SOAP<br>Todos Os Eventos Globais De Administrador<br>Todos Os Eventos De Front-End<br>Todos Os Eventos De Documento<br>Todos Os REST Eventos<br>Todos Os Eventos Da SOAP<br>Todos Os Eventos Crontab<br> |
| [!UICONTROL Cron] | Cron Agenda por código de status<br>Cron Agenda por código de trabalho<br>Erros na fila de Cron Agenda<br>Lista de Cron Agenda<br>Cron Tarefas Cron Globais Personalizadas<br>Tarefas Cron Configuráveis Personalizadas<br>Tarefas Cron Globais Principais<br>Tarefas Cron Configuráveis Principais<br>Todas as Tarefas Cron Globais<br>Todas as Tarefas Cron Configuráveis |
| [!UICONTROL Design] | Lista de Temas Adminhtml<br>Lista de Temas de Front-end |
| [!UICONTROL Stores] | Árvore do Site<br>Lista de Sites<br>Lista de Lojas<br>Lista de Exibições da Loja |
| Conector do OMS <br>_(visível com integração do OMS)_ | Versão do conector<br>Monitoramento do conector<br>Resultados do Processamento de Mensagens |

{style="table-layout:auto"}
