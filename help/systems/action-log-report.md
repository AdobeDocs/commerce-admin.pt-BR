---
title: Relatório de logs de ação
description: Saiba como exibir, filtrar e exportar o relatório de Log de ações, que fornece um registro detalhado de todas as ações de administrador habilitadas para log.
exl-id: f2be5852-9185-4f14-b0bb-44d779b40819
feature: Logs, Data Import/Export
TQID: https://experienceleague.adobe.com/b6LYoDmgU-uDdTLCjtDKd1TS4f7krj4fs9Qz4ClAJr4
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 441
ht-degree: 0%

---

# Relatório de logs de ação

{{ee-feature}}

O relatório _Logs de Ação_ exibe um registro detalhado de todas as ações de Administrador habilitadas para log. Cada registro recebe um carimbo de data e hora e registra o endereço IP e o nome do usuário. Os detalhes do log incluem dados do usuário administrador e alterações relacionadas que foram feitas durante a ação.

As ações que você deseja exibir no relatório devem ser habilitadas na tela [Log de Ações do Administrador](action-log.md) nas configurações de armazenamento. Se o tipo de ação estiver marcado (ativado), esses tipos de ações de Admin serão exibidos no relatório de Logs de ação.

O relatório pode ser filtrado usando as opções em cada coluna. Você pode definir uma única opção de filtro ou definir opções de filtro para várias colunas para restringir o relatório e listar ações específicas. Você também pode exportar dados de relatório nos formatos CSV ou XML do Excel.

O Relatório de Logs de Ação inclui as seguintes informações:

- **[!UICONTROL Time]** - A data e a hora em que a ação ocorreu
- **[!UICONTROL Action Group]** - Exibe o tipo de ação, correlaciona-se com as ações habilitadas na tela _Log de Ações de Administrador_ nas configurações do repositório
- **[!UICONTROL Action]** - Exibe a ação que foi registrada
- **[!UICONTROL IP Address]** - Exibe o endereço IP do computador no qual a ação foi executada
- **[!UICONTROL Username]** - Exibe a ID de logon do usuário que executou a ação
- **[!UICONTROL Result]** - Exibe o sucesso ou falha da ação do usuário
- **[!UICONTROL Full Action Name]** - Exibe o nome da ação de back-end
- **[!UICONTROL Details]** - Exibe a categoria de ação de back-end
- **[!UICONTROL Full Details]** - Exibe todos os detalhes registrados da ação do administrador

## Exibir o relatório de Logs de Ação

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Report]**.

   ![Logs de ação](./assets/action-log-report.png){width="600" zoomable="yes"}

1. Para exibir os detalhes completos de uma ação de administrador listada, clique em **[!UICONTROL View]**.

   ![Detalhes da entrada do log de ações](./assets/action-log-report-view.png){width="600" zoomable="yes"}

## Filtrar o relatório Logs de ação

Você pode definir os campos de opções de filtro e clicar em **[!UICONTROL Search]** para restringir as ações exibidas.

Para limpar as opções de filtro e retornar ao relatório completo, clique em **[!UICONTROL Reset Filter]**.

![Filtros de relatório do log de ações](./assets/action-log-report-filters.png){width="600" zoomable="yes"}

| Campo | descrição |
|--- |--- |
| [!UICONTROL Time] | Em **[!UICONTROL From]**, clique para selecionar uma data no calendário dinâmico para definir a data de início do filtro. Em **[!UICONTROL To]**, clique em para selecionar uma data para definir a data de término do filtro. |
| [!UICONTROL Action Group] | Escolha um grupo de ação. |
| [!UICONTROL Action] | Escolha uma ação. |
| [!UICONTROL IP Address] | Insira o endereço IP da máquina usada para uma ação. |
| [!UICONTROL Username] | Escolha um nome de usuário. O padrão é `All Users`. |
| [!UICONTROL Result] | Escolha Sucesso ou Falha. |
| [!UICONTROL Full Action Name] | Digite o texto para que a pesquisa corresponda no campo. |
| [!UICONTROL Details] | Digite o texto para que a pesquisa corresponda no campo. |

{style="table-layout:auto"}

## Exportar o relatório de Logs de Ação

1. Para **[!UICONTROL Export to]**, escolha um formato de exportação:

   - `CSV` - Um arquivo de valores separados por vírgula contendo dados de texto sem formatação
   - `Excel XML` - Um formato de dados de planilha baseado em XML

1. Clique em **[!UICONTROL Export]**.

   O arquivo gerado é salvo automaticamente na pasta designada para downloads.

   ![Exportação do relatório de logs de ação](./assets/action-log-report-export.png){width="200"}
