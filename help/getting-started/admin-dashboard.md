---
title: Painel de administração
description: Saiba mais sobre o Painel de administração, que geralmente é a primeira página exibida ao fazer logon.
exl-id: 56957c0a-1618-444b-a37a-ecf0d7b27eae
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---

# Painel de administração

O painel geralmente é a primeira página exibida ao fazer logon na _Admin_ e podem fornecer uma visão geral em tempo real das vendas e da atividade do cliente. Os dados do painel fornecem um instantâneo das vendas vitalícias, da quantidade média de pedidos, dos pedidos recentes e dos termos de pesquisa. O gráfico mostra pedidos e valores concluídos para o intervalo de datas selecionado e pode ser gerado a partir de dados dinâmicos, em tempo real ou agregados históricos. As guias na parte inferior fornecem relatórios rápidos dos produtos mais vendidos, dos produtos mais visualizados, dos novos clientes e dos clientes que mais compraram.

Se você tiver uma quantidade significativa de dados para processar, o gráfico poderá ser desativado para melhorar o desempenho. O painel no exemplo a seguir é configurado para usar dados em tempo real e mostra os pedidos concluídos por hora nas últimas 24 horas. O gráfico é atualizado para cada pedido concluído.

![Painel](./assets/dashboard-full.png){zoom=&quot;yes&quot;}

[Relatórios avançados](business-intelligence.md#advanced-reporting) O exibe um painel personalizado com base no produto, pedido e dados do cliente.

![Relatórios avançados](./assets/dashboard-advanced-reporting.png){zoom=&quot;yes&quot;}

## Configurar o painel

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**e conclua qualquer uma das configurações a seguir.

1. Quando a configuração estiver concluída, clique em **[!UICONTROL Save Config]**.

1. Depois de salvar as alterações, clique em **[!UICONTROL Cache Management]** e atualizar cada cache inválido.

### Ativar gráficos

Se você tiver uma grande quantidade de dados para processar, poderá desativar a exibição do gráfico para melhorar o desempenho. Quando não estiver ativado, a mensagem &quot;Nenhum dado encontrado&quot; será exibida no lugar do gráfico, embora os totais de resumo abaixo ainda sejam gerados.

1. No painel de navegação esquerdo, em **[!UICONTROL Advanced]**, escolha **[!UICONTROL Admin]**.

1. Se necessário, expanda a variável **[!UICONTROL Dashboard]** seção.

   ![Configuração avançada - Ativar gráficos](./assets/admin-dashboard-config.png){width="600"}

1. Para alterar o valor padrão, desmarque a caixa **[!UICONTROL Use system value]** caixa de seleção

1. Definir **Ativar Gráficos** para `Yes`.

Para obter mais informações sobre as opções de configuração de Admin, consulte [Guia de referência de configuração](../configuration-reference/advanced/admin.md).

### Alterar a página de inicialização

O painel é o padrão [página de inicialização](../configuration-reference/advanced/admin.md) para o Administrador, embora seja possível configurar uma página de inicialização diferente.

1. Se você ainda não tiver as opções de Configuração de administrador abertas, escolha **[!UICONTROL Admin]** em _[!UICONTROL Advanced]_no painel de navegação esquerdo.

1. Clique para expandir o **Página de inicialização** seção.

   ![Painel do administrador - configuração da página de inicialização](./assets/admin-startup-page.png){width="600"}

1. Limpe a **[!UICONTROL Use system value]** e escolha a caixa de seleção **Página de inicialização** que você deseja que apareça ao fazer logon no Administrador.

### Escolher as datas de início

1. No painel de navegação esquerdo, em **[!UICONTROL General]**, escolha **Relatórios**.

1. Na página, expanda a variável **[!UICONTROL Dashboard]** seção.

1. Limpe a **[!UICONTROL Use system value]** para as configurações de data e faça o seguinte:

   - Definir **Início do Acumulado no Ano** para o **Month** e **Dia**.

   - Definir **Mês Atual Começa** para o **Dia**.

   ![Painel do administrador - configurações de data](./assets/reports-dashboard.png){width="600"}

Para obter mais informações sobre o [!UICONTROL Reports] opções de configuração, consulte a seção [_Guia de referência de configuração_](../configuration-reference/general/reports.md).

### Configurar a fonte de dados

O gráfico de painel pode ser gerado em tempo real ou usando dados históricos e agregados. Se o desempenho for um problema, você pode acelerar o processo usando dados agregados.

1. No painel de navegação esquerdo, clique para expandir **Vendas** e escolha **Vendas** por baixo.

1. Na página, expanda a variável **[!UICONTROL Dashboard]** seção.

   ![Painel de administração - configuração da fonte de dados](./assets/config-sales-dashboard.png){width="600"}

1. Limpe a **[!UICONTROL Use system value]** caixa de seleção e definir **[!UICONTROL Use Aggregated Data]** a um dos seguintes:

   - Para dados históricos e agregados, escolha `Yes`.
   - Para dados em tempo real, escolha `No`.

## Seções do gráfico

| Seção | Descrição |
|--- |--- |
| [!UICONTROL Orders] | Esta guia exibe um gráfico em tempo real de todos os pedidos concluídos para a visualização de armazenamento atual e o período especificado. |
| [!UICONTROL Amounts] | Esta guia exibe um gráfico em tempo real de todos os valores de pedidos concluídos para a exibição de armazenamento atual e o período especificado. |
| [!UICONTROL Time Range] | Determina os dados que são representados no gráfico e o resumo total abaixo. Opções: `Last 7 Days` / `Current Month` / `YTD` / `2YTD` |
| [!UICONTROL Summary Totals] | Os totais de receita, imposto, remessa e quantidade abaixo do gráfico são baseados nos dados do gráfico e na configuração atual do intervalo de tempo. |

{style="table-layout:auto"}

## Dados de instantâneo

| Seção | Descrição |
|--- |--- |
| [!UICONTROL Lifetime Sales] | As vendas totais agregadas durante o tempo de vida da loja. |
| [!UICONTROL Average Order] | O valor médio de pedido durante a vida útil do armazenamento. |
| [!UICONTROL Last Orders] | Um resumo dos últimos cinco pedidos feitos. |
| [!UICONTROL Last Search Terms] | Os últimos cinco termos de pesquisa. |
| [!UICONTROL Top Search Terms] | Os cinco termos de pesquisa mais usados. |

{style="table-layout:auto"}

## Guias Relatório

| Seção | Descrição |
|--- |--- |
| [!UICONTROL Bestsellers] | Os cinco produtos mais vendidos durante o período de tempo especificado. |
| [!UICONTROL Most Viewed Products] | Os cinco produtos foram os mais visualizados durante o período especificado. |
| [!UICONTROL New Customers] | Os cinco clientes mais recentes que se registraram em uma conta durante o período especificado. |
| [!UICONTROL Customers] | Os cinco últimos clientes com um pedido que concluiu o processamento durante o período especificado. |

{style="table-layout:auto"}

## Botões do painel

| Botão | Descrição |
|--- |--- |
| [!UICONTROL Reload Data] | Atualiza os dados do painel. |
| [!UICONTROL Go to Advanced Reporting] | Exibe um painel personalizado de gráficos dinâmicos e relatórios com base em seu produto, pedido e dados do cliente. Para obter análises mais abrangentes, consulte [Relatórios avançados](business-intelligence.md#advanced-reporting). |

{style="table-layout:auto"}
