---
title: '[!DNL New Relic] relatórios'
description: Saiba mais sobre a [!DNL New Relic] relatórios disponível para contas de Adobe Systems Comércio no infraestrutura em nuvem, que inclui o software do serviço Novo Relic APM.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: e9a7645aed0e3b48bf565b04cdb6a31ce5d39ca0
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 0%

---

# [!DNL New Relic] relatórios

[New Relic][1] O é um serviço de análise de software que ajuda a analisar e melhorar as interações do aplicativo. As contas do Adobe Commerce na infraestrutura em nuvem incluem o software para o [!DNL New Relic APM] serviço. Para obter mais informações, consulte [Serviços da New Relic][4] no _Guia do Commerce na infraestrutura em nuvem_.

## Etapa 1: Inscreva-se para um [!DNL New Relic] account

1. Acesse o [[!DNL New Relic]][1] site e cadastro para obter um conta.

   Você também pode se inscrever para um conta de teste de grátis.

1. Siga as instruções no site. Quando solicitado, escolha o produto que deseja instalar primeiro.

1. Enquanto estiver em seu conta, localize as seguintes credenciais necessárias para concluir a configuração Comércio:

   | Opção | Descrição |
   | ------ | ----------- |
   | ID da Conta | Do seu [!DNL New Relic] no painel de contas, a ID da conta é o número no URL após: `/accounts` |
   | ID do aplicativo | Do seu [!DNL New Relic] painel da conta, clique em **[!UICONTROL New Relic APM]**. No menu, escolha **[!UICONTROL Applications]**. Em seguida, escolha o aplicativo. O ID do aplicativo é o número no URL após: `/applications/` |
   | Chave da API do New Relic | Do seu [!DNL New Relic] painel da conta, clique em **[!UICONTROL Account Settings]**. No menu à esquerda, em Integrações, escolha **[!UICONTROL Data Sharing]**. Você pode criar, regenerar ou excluir sua chave de API nesta página. |
   | Chave da API do Insights | Do seu [!DNL New Relic] painel da conta, clique em **[!UICONTROL Insights]**. No menu à esquerda, em Administração, escolha **[!UICONTROL API Keys]**. Suas chaves de API do Insights aparecem nesta página. Se necessário, clique no sinal de mais (**+**) ao lado de Insert Keys (Inserir teclas) para gerar uma chave. |

   {style="table-layout:auto"}

## Etapa 2: instalar o [!DNL New Relic] agente no servidor

Para usar [!DNL New Relic APM Pro] para coletar e transmitir dados, o agente PHP deve estar instalado em seu servidor.

1. Quando solicitado a escolher um agente da Web, clique em **PHP**.

1. Para configurar o agente PHP em seu servidor, siga as instruções.

   Se precisar de ajuda, consulte [New Relic para PHP][3].

1. Verifique se o cron está em execução no servidor.

   Para saber mais, consulte [Configurar e executar o cron][5] na documentação do desenvolvedor.

## Etapa 3: configurar seu armazenamento

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel de navegação esquerdo, onde **[!UICONTROL General]** for expandido, escolha **[!UICONTROL New Relic Reporting]** e faça o seguinte:

   ![Configuração de relatórios do New Relic](./assets/new-relic-reporting-general.png){width="600"}

   * Definir **[!UICONTROL Enable New Relic Integration]** para `Yes`.

   * No **[!UICONTROL Insights API URL]**, substitua a porcentagem (`%`) com sua ID de conta da New Relic.

   * Insira seu **[!UICONTROL New Relic Account ID]**.

   * Insira seu **[!UICONTROL New Relic Application ID]**.

   * Insira seu **[!UICONTROL New Relic API Key]**.

   * Insira você **[!UICONTROL Insights API Key]**.

1. Para **[!UICONTROL New Relic Application Name]**, insira um nome para identificar a configuração para referência interna.

1. (Opcional) Para **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**, selecione `Yes` para enviar dados coletados da loja e do Administrador como aplicativos separados para a New Relic.

   Esta opção requer um nome inserido para a função **[!UICONTROL New Relic Application Name]**.

   >[!NOTE]
   >
   >Habilitar este recurso reduz o número de falsos positivos [!DNL New Relic] O alerta e permite o monitoramento configurado e alertas estritamente para o desempenho de front-end. O New Relic recebe arquivos de dados de aplicativo separados com nomes de Nome do aplicativo anexados a `Adminhtml` e front-end. Por exemplo: `MyStore_Adminhtml`

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Etapa 4: Ativar o Cron para [!DNL New Relic] relatórios

1. Expanda ![a expansão seletor](../assets/icon-display-expand.png) **[!UICONTROL Cron]** seção.

   ![Configuração do New Relic Cron](./assets/new-relic-reporting-cron.png){width="600"}

1. Definir **[!UICONTROL Enable Cron]** para `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## [!DNL New Relic] queries

[!DNL New Relic Insights] Os dados do são baseados em declarações escritas em [!DNL New Relic Query Language] (NRQL) e quaisquer parâmetros personalizados que você possa incluir. Os dados podem ser retornados de consultas adhoc ou por consultas salvas no painel. Para saber mais, consulte a [Referência NRQL][6] no [!DNL New Relic] documentação.

### Eventos de administração

#### Usuários administradores ativos

Retorna o número de usuários Administradores ativos.

    SELECT uniqueCount(AdminId)
    Transação DE
    ONDE appName=&#39;&lt;your_app_name>&#39; DESDE 15 minutos atrás

#### Usuários administradores ativos no momento

Retorna os nomes dos usuários administradores ativos.

    SELECIONe uniques(AdminName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15 minutos atrás
&lt;/your_app_name>
#### Atividade Recente do Administrador

Retorna o número de ações recentes de Administrador.

    Contagem de SELECT (AdminId)
    Transação DE
    ONDE appName =&#39;&lt;your_app_name>&#39; FACET AdminName DESDE 1 dia atrás

#### Atividade mais recente de administrador

Retorna informações detalhadas sobre ações de administrador recentes, incluindo o nome de usuário do administrador, a duração e o nome aplicativo.

    SELECIONE AdminName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; AND AdminName IS NOT NULL
    AND AdminName !&lt;/your_app_name>= LIMITE &#39;N/A&#39; 50

### Eventos cron

#### contagem de Categoria

Retorna o número de eventos de aplicação por categoria durante o período especificado.

    Média de SELECT(CatalogCategoryCount)
    DO Cron
    ONDE CatalogCategoryCount NÃO É NULO
    E appName = &#39;&lt;your_app_name>&#39; SÉRIE TEMPORAL 2 minutos

#### Contagem de catálogo atual

Retorna o número médio de eventos de aplicação no catálogo por categoria durante o período especificado.

    Média de SELECT(CatalogCategoryCount)
    DO Cron
    ONDE CatalogCategoryCount NÃO É NULO
    E CatalogCategoryCount > 0
    E appName = &#39;&lt;your_app_name>&#39; DESDE 2 minutos atrás LIMITE 1

#### Produtos ativos

Retorna o número de eventos de aplicativo por produto durante o período especificado.

    Média de SELECT(CatalogProductActiveCount)
    DO Cron
    ONDE CatalogProductActiveCount NÃO É NULO
    E appName = &#39;&lt;your_app_name>&#39; SÉRIE TEMPORAL 2 minutos

#### Contagem de produtos ativos

Retorna o número médio de eventos de aplicativos ativos por produto durante o período especificado.

    Média de SELECT(CatalogProductActiveCount)
    DO Cron
    ONDE CatalogProductActiveCount NÃO É NULO
    E CatalogProductActiveCount > 0
    E appName = &#39;&lt;your_app_name>&#39; DESDE 2 minutos atrás LIMITE 1

#### Produtos configuráveis

Retorna o número médio de eventos de aplicativos para produtos configuráveis durante o período especificado.

    Média de SELECT(CatalogProductConfigurableCount)
    DO Cron
    ONDE CatalogProductConfigurableCount NÃO É NULO
    E appName = &#39;&lt;your_app_name>&#39; SÉRIE TEMPORAL 2 minutos

#### Contagem de produtos configurável

Retorna o número médio de eventos de aplicativos por produto configurável durante o período especificado.

    Média de SELECT(CatalogProductConfigurableCount)
    DO Cron
    ONDE CatalogProductConfigurableCount NÃO É NULO
    E CatalogProductConfigurableCount > 0
    E appName = &#39;&lt;your_app_name>&#39; DESDE 2 minutos atrás LIMITE 1

#### Contagem de produtos (todos)

Retorna o número total de eventos de aplicativo para todos os produtos.

    Média de SELECT(CatalogProductCount)
    DO Cron
    ONDE CatalogProductCount NÃO É NULO
    E appName = &#39;&lt;your_app_name>&#39; SÉRIE TEMPORAL 2 minutos

#### Contagem de produtos atual (todos)

Retorna o número médio de eventos de aplicativos para todos os produtos durante o período especificado.

    Média de SELECT(CatalogProductCount)
    DO Cron
    ONDE CatalogProductCount NÃO É NULO
    E CatalogProductCount > 0
    E appName = &#39;&lt;your_app_name>&#39; DESDE 2 minutos atrás LIMITE 1

#### Contagem de clientes

Retorna o número médio de eventos de aplicativo por cliente.

    Média de SELECT (CustomerCount)
    DO Cron
    ONDE CustomerCount NÃO É NULO
    E CustomerCount > 0&lt;
    E appName = &#39;&lt;your_app_name>&#39; SÉRIE TEMPORAL 2 minutos

#### Contagem atual de clientes

Retorna o número médio de clientes durante o período especificado.

    Média de SELECT (CustomerCount)
    DO Cron
    ONDE CustomerCount NÃO É NULO
    E CustomerCount > 0
    E appName = &#39;&lt;your_app_name>&#39; DESDE 2 minutos atrás LIMITE 1

#### Status do módulo

Retorna o número médio de vezes que os módulos de aplicativos são ativados, desativados ou instalados durante o período especificado.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (Módulos instalados)
    DO Cron&lt;
    ONDE appName = &#39;&lt;your_app_name>&#39; SÉRIE TEMPORAL 2 minutos

#### Status atual do módulo

Retorna o número médio de vezes que os módulos foram habilitados, desabilitados ou instalados durante o período especificado.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (Módulos instalados)
    DO Cron
    ONDE appName = &#39;&lt;your_app_name>&#39; DESDE 2 minutos atrás LIMITE 1

#### Contagens de sites e lojas

Retorna o número médio de eventos de aplicativo por site e armazenamento durante o período especificado.

    SELECT average(StoreViewCount), average(WebsiteCount)
    DO Cron
    ONDE appName = &#39;&amp;lt;your_app_name&amp;gt;&#39; SÉRIE HORÁRIA 2 minutos

#### Contagem atual de sites e lojas

Retorna o número médio de eventos de aplicativo atuais durante o período especificado.

    SELECT average(StoreViewCount), average(WebsiteCount)
    DO Cron
    ONDE appName = &#39;&lt;your_app_name>&#39; DESDE 2 minutos atrás LIMITE 1

#### Cron - todos os dados do evento

Retorna todos os dados do evento de aplicativo.

    SELECIONAR *
    DO Cron
    ONDE appName = &#39;&lt;your_app_name>&#39;

### Clientes

#### Contagem de clientes ativos

Retorna o número de clientes ativos durante o período especificado.

    SELECIONAR uniqueCount(CustomerId)
    Transação DE
    ONDE appName = &#39;&lt;your_app_name>&#39; DESDE 15 minutos atrás

#### Clientes ativos

Retorna os nomes dos clientes ativos durante a período especificada.

    SELECIONAR uniques(CustomerName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; DESDE 15 minutos atrás
&lt;/your_app_name>
#### Principais clientes

Retorna os principais clientes durante o período de tempo especificado.

    Selecionar contagem(CustomerId)
    Transação DE
    ONDE appName = &#39;&lt;your_app_name>&#39; FACET NomeCliente DESDE 1 dia atrás

#### Atividade Recente do Administrador

Retorna um número definido de registros de atividade recentes, que incluem o nome do cliente e a duração da visita.

    SELECIONE CustomerName, duration, name
    FROM Transaction
    WHERE appName=&lt;your_app_name>&#39;&#39;
    AND CustomerName IS NOT NULL
    AND CustomerName !&lt;/your_app_name>= LIMITE &#39;N/A&#39; 50

### Ordens

#### Número de pedidos feitos

Retorna o número de pedidos feitos durante a período especificada.

    SELECT count(Order)
    DA Transação DESDE 1 dia atrás

#### Valor total do pedido

Retorna o número total de itens de linha solicitados durante o período especificado.

    SELECT sum(orderValue)
    DA Transação DESDE 1 dia atrás

#### Total de itens de linha solicitados

Retorna o número total de itens de linha solicitados durante o período especificado.

    SELECT sum(lineItemCount)
    DA Transação DESDE 1 dia atrás


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
