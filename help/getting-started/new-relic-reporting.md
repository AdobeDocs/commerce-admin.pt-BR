---
title: '[!DNL New Relic] relatórios'
description: Saiba mais sobre os [!DNL New Relic] relatórios disponíveis para contas do Adobe Commerce na infraestrutura em nuvem, que inclui o software para o serviço de APM da New Relic.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: 0651a2489a396ab142b60a8678d6c7590fd5f9ee
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 0%

---

# [!DNL New Relic] relatórios

O [New Relic][1] é um serviço de análise de software que ajuda a analisar e melhorar as interações entre aplicativos. As contas do Adobe Commerce na infraestrutura em nuvem incluem o software para o serviço [!DNL New Relic APM]. Para obter mais informações, consulte [serviços da New Relic][4] no _Guia de Infraestrutura do Commerce na Nuvem_.

## Etapa 1: Inscrever-se para uma conta do [!DNL New Relic]

1. Vá para o site do [[!DNL New Relic]][1] e cadastre-se para obter uma conta.

   Você também pode se inscrever para obter uma conta de avaliação gratuita.

1. Siga as instruções no site. Quando solicitado, escolha o produto que deseja instalar primeiro.

1. Enquanto estiver em seu conta, localize as seguintes credenciais necessárias para concluir a configuração Comércio:

   | Opção | Descrição |
   | ------ | ----------- |
   | ID da Conta | No painel de conta do [!DNL New Relic], a ID da conta é o número na URL após: `/accounts` |
   | ID do aplicativo | No painel de conta do [!DNL New Relic], clique em **[!UICONTROL New Relic APM]**. No menu, escolha **[!UICONTROL Applications]**. Em seguida, escolha o aplicativo. A ID do aplicativo é o número no URL depois: `/applications/` |
   | Novo chave de API de relíquia | No painel de conta do [!DNL New Relic], clique em **[!UICONTROL Account Settings]**. No menu à esquerda, em Integrações, escolha **[!UICONTROL Data Sharing]**. Você pode criar, regenerar ou excluir sua chave de API nesta página. |
   | Chave da API do Insights | No painel de conta do [!DNL New Relic], clique em **[!UICONTROL Insights]**. No menu à esquerda, em Administração, escolha **[!UICONTROL API Keys]**. Suas chaves de API do Insights aparecem nesta página. Se necessário, clique no sinal de mais (**+**) ao lado de Inserir chaves para gerar uma chave. |

   {style="table-layout:auto"}

## Etapa 2: instalar o agente do [!DNL New Relic] no servidor

Para usar o [!DNL New Relic APM Pro] para coletar e transmitir dados, o agente PHP deve estar instalado no servidor.

1. Quando solicitado a escolher um agente web, clique em **PHP**.

1. Para configurar o agente PHP em seu servidor, siga as instruções.

   Se precisar de ajuda, consulte [New Relic para PHP][3].

1. Verifique se o cron está em execução no servidor.

   Para saber mais, consulte [Configurar e executar o cron][5] na documentação do desenvolvedor.

## Etapa 3: configurar seu armazenamento

>[!NOTE]
>Essas opções de configuração não se aplicam ao Adobe Commerce na infraestrutura em nuvem.
>
>Se você estiver no plano Pro, o New Relic já está [pré-configurado e habilitado por padrão](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Se você estiver no plano Inicial, conclua as [etapas de configuração do New Relic](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) que fazem parte do processo de instalação.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel de navegação esquerdo, onde **[!UICONTROL General]** é expandido, escolha **[!UICONTROL New Relic Reporting]** e faça o seguinte:

   ![Configuração de relatórios do New Relic](./assets/new-relic-reporting-general.png){width="600"}

   * Defina **[!UICONTROL Enable New Relic Integration]** como `Yes`.

   * No **[!UICONTROL Insights API URL]**, substitua o símbolo de porcentagem (`%`) pela ID de conta da New Relic.

   * Insira seu **[!UICONTROL New Relic Account ID]**.

   * Insira seu **[!UICONTROL New Relic Application ID]**.

   * Insira seu **[!UICONTROL New Relic API Key]**.

   * Insira você **[!UICONTROL Insights API Key]**.

1. Para **[!UICONTROL New Relic Application Name]**, insira um nome para identificar a configuração para referência interna.

1. (Opcional) Para **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**, selecione `Yes` para enviar dados coletados para a vitrine e o Administrador como aplicativos separados para a New Relic.

   Esta opção requer um nome inserido para o **[!UICONTROL New Relic Application Name]**.

   >[!NOTE]
   >
   >Habilitar esse recurso reduz o número de alertas [!DNL New Relic] de falso positivo e permite o monitoramento configurado e alertas estritamente para o desempenho de front-end. O New Relic recebe arquivos de dados de aplicativo separados com nomes de Nome de Aplicativo anexados a `Adminhtml` e front-end. Por exemplo: `MyStore_Adminhtml`

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Etapa 4: Habilitar o Cron para relatórios de [!DNL New Relic]

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Cron]**.

   ![Configuração do New Relic Cron](./assets/new-relic-reporting-cron.png){width="600"}

1. Defina **[!UICONTROL Enable Cron]** como `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## [!DNL New Relic] consultas

Os dados de [!DNL New Relic Insights] baseiam-se em instruções gravadas em [!DNL New Relic Query Language] (NRQL) e em quaisquer parâmetros personalizados que você possa incluir. Os dados podem ser retornados de consultas adhoc ou por consultas salvas no painel. Para saber mais, consulte a [NRQL Reference][6] na documentação [!DNL New Relic].

### Eventos de administração

#### Usuários administradores ativos

Retorna o número de usuários Administradores ativos.

    SELECIONAR uniqueCount(AdminId)
    DA Transação
    ONDE appName=&#39;&lt;nome_do_seu_aplicativo>&#39; HÁ 15 minutos

#### Usuários administradores ativos no momento

Retorna os nomes dos usuários administradores ativos.

    SELECIONAR únicos(AdminName)
    DA Transação
    ONDE appName=&#39;&lt;nome_do_aplicativo>&#39; DESDE 15 minutos atrás

#### Atividade Recente do Administrador

Retorna o número de ações recentes de Administrador.

    SELECIONE count(AdminId)
    FROM Transaction
    WHERE appName =&#39;&lt;nome_do_seu_aplicativo>&#39; FACET AdminName DESDE 1 dia atrás

#### Atividade mais recente de administrador

Retorna informações detalhadas sobre ações de administrador recentes, incluindo o nome de usuário do administrador, a duração e o nome aplicativo.

    SELECIONE AdminName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; AND AdminName IS NOT NULL
    AND AdminName !&lt;/your_app_name>= LIMITE &#39;N/A&#39; 50

### Eventos cron

#### contagem de Categoria

Retorna o número de eventos de aplicativo categoria durante a período especificada.

    SELECT average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; SÉRIE HORÁRIA 2 minutos

#### Contagem de catálogo atual

Retorna o número médio de eventos de aplicação no catálogo por categoria durante o período especificado.

    SELECT average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND CatalogCategoryCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutos atrás LIMIT 1
&lt;/your_app_name>
#### Produtos ativos

Retorna o número de eventos de aplicativo por produto durante o período especificado.

    SELECT average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    AND appName = &#39;&lt;nome_do_seu_aplicativo>&#39; TIMESERIES 2 minutos

#### Contagem de produtos ativos

Retorna o número médio de eventos de aplicativos ativos por produto durante o período especificado.

    SELECT average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; DESDE 2 minutos atrás LIMITE 1

#### Produtos configuráveis

Retorna o número médio de eventos de aplicativos para produtos configuráveis durante o período especificado.

    SELECT average(CatalogProductConfigurableCount)
    FROM Cron
    WHERE CatalogProductConfigurableCount IS NOT NULL
    AND appName = &#39;&lt;nome_do_aplicativo>&#39; SÉRIE_TEMPORAL 2 minutos

#### Contagem de produtos configurável

Retorna o número médio de eventos de aplicativos por produto configurável durante o período especificado.

    SELECT average(CatalogProductConfigurableCount)
    FROM Cron
    WHERE CatalogProductConfigurableCount IS NOT NULL
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; DESDE 2 minutos atrás LIMIT 1

#### Contagem de produtos (todos)

Retorna o número total de eventos de aplicativo para todos os produtos.

    SELECT average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
    AND appName = &#39;&lt;nome_do_seu_aplicativo>&#39; SÉRIE HORÁRIA 2 minutos

#### Contagem de produtos atual (todos)

Retorna o número médio de eventos de aplicativos para todos os produtos durante o período especificado.

    SELECT average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
    AND CatalogProductCount > 0
    AND appName = &#39;&lt;nome_do_aplicativo>&#39; DESDE 2 minutos atrás LIMIT 1

#### Contagem de clientes

Retorna o número médio de eventos de aplicativo por cliente.

    SELECT average(CustomerCount)
    FROM Cron
    WHERE CustomerCount NÃO É NULO
    AND CustomerCount > 0&lt;
    AND appName = &#39;&lt;nome_do_seu_aplicativo>&#39; TIMESERIES 2 minutos

#### Contagem atual de clientes

Retorna o número médio de clientes durante o período especificado.

    SELECT average(CustomerCount)
    FROM Cron
    WHERE CustomerCount IS NOT NULL
    AND CustomerCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; DESDE 2 minutos atrás LIMITE 1

#### Status do módulo

Retorna o número médio de vezes que os módulos de aplicativos são ativados, desativados ou instalados durante o período especificado.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    FROM Cron&lt;
    WHERE appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutos

#### Status atual do módulo

Retorna o número médio de vezes que os módulos foram habilitados, desabilitados ou instalados durante o período especificado.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; DESDE 2 minutos atrás LIMITE 1

#### Contagens de sites e lojas

Retorna o número médio de eventos de aplicativo por site e armazenamento durante o período especificado.

    SELECT average(StoreViewCount), average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&amp;lt;your_app_name&amp;gt;&#39; TIMESERIES 2 minutos

#### Contagem atual de sites e lojas

Retorna o número médio de eventos de aplicativo atuais durante o período especificado.

    SELECT average(StoreViewCount), average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; DESDE 2 minutos atrás LIMITE 1

#### Cron - todos os dados do evento

Retorna todos os dados do evento de aplicativo.

    SELECIONAR *
    DE Cron
    ONDE appName = &#39;&lt;nome_do_aplicativo>&#39;

### Clientes

#### Contagem de clientes ativos

Retorna o número de clientes ativos durante o período especificado.

    SELECIONE uniqueCount(CustomerId)
    FROM Transação
    ONDE appName = &#39;&lt;nome_do_aplicativo>&#39; HÁ 15 minutos

#### Clientes ativos

Retorna os nomes dos clientes ativos durante o período especificado.

    SELECIONAR únicos(NomeCliente)
    DA Transação
    ONDE appName=&#39;&lt;nome_do_seu_aplicativo>&#39; DESDE 15 minutos atrás

#### Principais clientes

Retorna os principais clientes durante o período de tempo especificado.

    SELECIONE count(CustomerId)
    FROM Transaction
    WHERE appName = &#39;&lt;your_app_name>&#39; FACET CustomerName DESDE 1 dia atrás

#### Atividade Recente do Administrador

Retorna um número definido de registros de atividade recente, que incluem o nome do cliente e a duração da visita.

    SELECIONE CustomerName, duration, name
    FROM Transaction
    WHERE appName=&lt;your_app_name>&#39;&#39;
    AND CustomerName IS NOT NULL
    AND CustomerName !&lt;/your_app_name>= LIMITE &#39;N/A&#39; 50

### Ordens

#### Número de pedidos feitos

Retorna o número de pedidos feitos durante a período especificada.

    SELECIONAR a contagem (pedido)
    da transação desde 1 dia atrás

#### Valor total do pedido

Retorna o número total de itens de linha solicitados durante o período especificado.

    SELECIONAR sum(orderValue)
    DE transação DESDE 1 dia atrás

#### Total de itens de linha ordenados

Retorna o número total de itens de linha solicitados durante a período especificada.

    SELECIONAR sum(lineItemCount)
    DE Transação DESDE 1 dia atrás


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
