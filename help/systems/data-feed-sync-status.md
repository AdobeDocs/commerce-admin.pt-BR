---
title: Monitoramento do status do feed de dados
description: Monitore a sincronização da exportação de dados e identifique problemas ou atrasos no processamento do feed para  [!DNL Catalog Service], [!DNL Live Search] e [!DNL Product Recommendations].
feature: Products, Customers, Data Import/Export
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 433d3fd4dc10a81b685262c1e3c06a0da5778841
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 0%

---


# Monitoramento do status do feed de dados

Os administradores do Adobe Commerce podem monitorar o status de sincronização dos dados exportados do Adobe Commerce para os serviços conectados do Commerce usando a página Status de sincronização do feed de dados no administrador do Commerce.

![Página de detalhes Status da Sincronização do Feed de Dados com relatórios de status do item de feed](assets/data-feed-sync-status.png)

Esta página fornece insights em tempo real sobre a integridade e o desempenho dos feeds de exportação de dados que transferem dados de produto e categoria da Commerce para serviços externos, como [!DNL Product Recommendations], [!DNL Live Search] e [!DNL Catalog Service].

A página de status da sincronização mostra apenas o status da exportação. Um status bem-sucedido indica que os dados foram exportados com êxito para o banco de dados SaaS para publicação. Use o [Painel de gerenciamento de dados](data-dashboard.md) para rastrear dados transferidos do banco de dados do Commerce para serviços conectados.

O monitoramento do status do feed ajuda a garantir a consistência dos dados e permite a resolução imediata de quaisquer problemas que surjam durante o processo de exportação. Os administradores podem:

* **Exibir o status de sincronização** para todos os feeds de dados
* **Identificar e solucionar erros** no processamento do feed
* **Acessar informações detalhadas de status** de itens de feed individuais

O status é rastreado para os seguintes feeds:

* Feed de produtos
* Feed de atributos do produto
* Feed de categorias
* Feed de substituições do produto
* Feed de preços do produto
* Feed de variantes de produto

>[!TIP]
>
>Para saber mais sobre o processo de sincronização de dados, consulte [Sincronizar dados com a exportação de dados SaaS](https://experienceleague.adobe.com/pt-br/docs/commerce/saas-data-export/data-synchronization)no *Guia de Exportação de Dados SaaS**.

## Instalar a extensão

A página Status do feed de dados está disponível para todos os comerciantes da Commerce com licenças ativas para os seguintes serviços da Commerce:

* [[!DNL Product Recommendations v6.0.0+]](https://experienceleague.adobe.com/pt-br/docs/commerce/product-recommendations/guide-overview)
* [[!DNL Live Search v4.1.0+]](https://experienceleague.adobe.com/pt-br/docs/commerce/live-search/guide-overview)
* [[!DNL Catalog Service v1.17+]](https://experienceleague.adobe.com/pt-br/docs/commerce/catalog-service/guide-overview) com uma licença ativa.

**Requisitos**

* PHP 8.1, 8.2, 8.3 ou 8.4
* Adobe Commerce 2.4.4+
* [Extensão de Exportação de Dados do Adobe Commerce](https://experienceleague.adobe.com/pt-br/docs/commerce/saas-data-export/manage-extension), versão 103.4.15 ou posterior
* Acesso ao [repo.magento.com](https://repo.magento.com)

  Para gerar chaves e obter os direitos necessários, consulte [Obter suas chaves de autenticação](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Para instalações na nuvem, consulte o [Guia de Infraestrutura do Commerce na Nuvem](https://experienceleague.adobe.com/pt-br/docs/commerce-on-cloud/user-guide/develop/authentication-keys).

* Acesso à linha de comando do servidor de aplicativos do Adobe Commerce.

### Etapas de instalação

Adicionar o módulo `adobe-commerce/module-data-exporter-status` usando o Composer:

```shell
composer require magento/module-data-exporter-status
```

Para ver as etapas detalhadas de instalação, consulte os guias a seguir:

* [Instalar extensão no Adobe Commerce na Infraestrutura em Nuvem](https://experienceleague.adobe.com/pt-br/docs/commerce-on-cloud/user-guide/configure-store/extensions)

* [Instalar Adobe Commerce de extensão no local](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/installation-guide/tutorials/extensions)

## Acessar a página Status do feed de dados

No Administrador do Commerce, acesse a página Status do feed de dados do Administrador do Commerce em **[!DNL System]** > Transferência de dados > **[!DNL Data Feed SyncStatus]**.

![Página Status da Sincronização do Feed de Dados resumindo a atividade de exportação do feed de dados](assets/data-feed-sync-status.png)

O monitoramento do status do feed de dados fornece duas interfaces:

* A [página de resumo Status de sincronização do feed de dados](#data-feed-sync-status-summary), que lista os feeds disponíveis e o estado atual
* A [página Status de Sincronização do Feed de Dados - Detalhes](#data-feed-sync-status-details) que mostra informações detalhadas sobre um feed selecionado.

## Resumo do status de sincronização do feed de dados

A página de resumo Status de sincronização do feed fornece informações sobre a atividade de exportação do feed de dados, incluindo as seguintes informações:

| Campo | Descrição |
|-------|-------------|
| **Nome do feed** | O nome do indexador de feed responsável por sincronizar uma entidade específica ou sua parte, por exemplo, produto ou preço do produto. |
| **Registros Source** | Número de registros disponíveis para exportação no banco de dados do Commerce. Esse número pode ser maior do que o número de registros exibidos no Administrador do Commerce, pois cada item de feed pertence a um escopo específico, como o código de Exibição de loja. |
| **Registros Enviados Com Êxito** | Número de registros transmitidos com êxito ao Commerce SaaS para processamento adicional. Se ocorreram erros durante a transmissão, o número de registros transmitidos com êxito para serviços externos. |
| **Registros com Falha** | Número de registros que falharam ao exportar e exigem atenção. |
| **Ação** | Selecione **[!UICONTROL Details]** para exibir a atividade de sincronização de um feed. |

## Detalhes do status de sincronização do feed de dados

Na página de resumo Status do feed de dados, clique em um nome de feed ou use a ação [!DNL View Details] para acessar informações detalhadas sobre registros individuais em um feed.

![[!UICONTROL Data Feed Sync Status - Details] página com relatório de status de item de feed](assets/data-feed-sync-status-details.png)

A exibição detalhada fornece as seguintes informações para cada item do feed:

| Campo | Descrição |
|-------|-------------|
| **ID do Item do Feed** | Identificador interno do registro de feed |
| **ID da entidade** | A ID da entidade de origem (ID do produto, ID da categoria e assim por diante) |
| **Status da exportação** | O [status de sincronização](#export-status-types) do item de feed. Status atual da tentativa de exportação com indicadores codificados por cores |
| **Data da Última Sincronização** | Carimbo de data e hora quando o registro foi enviado pela última vez para os Serviços Commerce |
| **A entidade foi excluída?** | Indica se a entidade ou sua parte (preço do produto ou produto, por exemplo) foi excluída no Adobe Commerce. Os itens são exibidos somente se ocorrer um erro durante a sincronização. |
| **ID da Solicitação** | Um identificador exclusivo para a solicitação de sincronização. Forneça essa ID ao suporte ao solucionar problemas de atualizações de entidade específicas. |
| **Erro** | Informações detalhadas sobre o erro se o item de feed não for sincronizado. |

Você pode gerenciar a exibição usando os seguintes controles:

* [!DNL Mass Action] para agendar a ressincronização dos itens de feed selecionados
* [!DNL Filters]
* [!DNL Default View] para criar e salvar um modo de exibição filtrado e alternar entre modos de exibição
* [!DNL Columns] para mostrar e ocultar colunas na tabela.

### Indicadores de saúde do feed

Na parte superior de cada página de detalhes do feed, os indicadores críticos de integridade fornecem o status do sistema para cada feed:

#### Status do indexador

* **Válido**: os dados estão sincronizados; nenhuma reindexação é necessária.
* **Inválido**: os dados originais foram alterados; o índice deve ser atualizado.
* **Processando**: indexação em andamento.

>[!TIP]
>
>Para saber mais sobre o processamento de índice, consulte o tópico [Gerenciamento de índice](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/systems/tools/index-management).

#### Backlog de log de alterações

* **Todas as sincronizadas**: nenhuma alteração pendente para processar
* **Itens na lista de pendências**: Número de alterações pendentes aguardando para serem processadas

### Exportar tipos de status

O sistema fornece indicadores de status para ajudar você a identificar problemas rapidamente:

#### Categorias de status

| **Status** | **Descrição** | **Ação necessária** |
|--------|-----------|-------------|
| **Enviado ao serviço** | O item de feed foi exportado com sucesso para o serviço Commerce. | Nenhum |
| **Falha, tentará novamente** | Falha temporária. O sistema tentará automaticamente novamente. | Monitor para resolução |
| **Falha, requer atenção** | Falha devido a um erro de aplicativo ou de dados. | Investigue e resolva o problema na coluna [!DNL Error] |
| **Aguardando envio** | Na fila para exportação, mas ainda não processado. | Estado de processamento normal |

## Monitorar status do feed de dados

Ao atualizar entidades relacionadas ao produto e à categoria no banco de dados do Commerce, os dados são transferidos para os serviços da Commerce de acordo com a configuração do feed. Você pode monitorar esse processo em tempo real na página de resumo Status de sincronização do feed de dados.

>[!IMPORTANT]
>
>O tempo necessário para concluir a sincronização de dados varia de acordo com o tamanho do catálogo, o volume de dados atualizados e o desempenho do serviço externo.

Quando o número de registros enviados com êxito corresponde ao número de registros de origem, isso indica que a sincronização foi concluída e todos os dados foram transmitidos com êxito.

>[!NOTE]
>
>O Adobe também fornece ferramentas de interface de linha de comando e registros do sistema que desenvolvedores e integradores de sistemas podem usar para gerenciar e rastrear operações de sincronização. Para obter detalhes, consulte o [Guia de Exportação de Dados SaaS](https://experienceleague.adobe.com/pt-br/docs/commerce-merchant-services/saas-data-export/overview).

### Gerenciamento de exportações com falha

Para ver os detalhes das exportações com falha e executar a ação corretiva:

1. Na página Status de sincronização do feed, encontre o feed com registros com falha.
1. Clique em **[!DNL Details]**.

1. Revise as mensagens de erro para obter os motivos específicos da falha.

1. Use ações em massa para programar operações de ressincronização para itens com falha.

### Ressincronizar dados com falha

Você pode ressincronizar manualmente feeds de dados com falha ou problemáticos usando o menu [!DNL Actions] na página [!DNL Data Feed Sync Status - Details].

Enquanto o sistema tenta automaticamente determinados tipos de falhas, pode ser necessária uma intervenção manual nos seguintes cenários:

* Você percebe erros de autenticação ou permissão (códigos de status 401, 403).
* Após resolver problemas de formato de dados que causavam erros de carga.
* Seguindo atualizações para configurações de serviço externo ou endpoints.
* Você está implantando personalizações que afetam processos de exportação de dados.

Ao monitorar proativamente o status do feed e solucionar falhas prontamente, você pode manter a consistência e a confiabilidade dos dados em todo o ecossistema do Commerce.

#### Ressincronizar manualmente os itens do feed

Se precisar ressincronizar itens específicos do feed:

1. **Selecionar Registros**: use caixas de seleção para selecionar registros com falha que precisem de atenção.
2. **Escolher Ação**: Selecione **[!DNL Schedule Resync]** na lista suspensa de ações em massa.
3. **Confirmar**: clique em **[!DNL Submit]** e confirme a operação de ressincronização.
4. **Monitorar Resultados**: Verifique a mensagem de êxito e monitore as alterações de status.

## Práticas recomendadas

### Monitoramento regular

1. **Verificações Diárias**: examine a página de visão geral diariamente para ver se há feeds mostrando altas taxas de falha
1. **Aprofundamento Semanal**: examine o status detalhado de feeds críticos (produtos, preços)
1. **Análise Mensal**: controle tendências em taxas de sucesso e desempenho de exportação

### Solução de problemas do fluxo de trabalho

1. **Identificar problemas**: procure erros e contagens altas de falhas
1. **Verificar Integridade do Indexador**: verifique se os indexadores são válidos e se a lista de pendências é gerenciável
1. **Revisar Detalhes do Erro**: clique nos registros com falha para ver mensagens de erro específicas
1. **Ressincronizar agendamento**: usar ações em massa para repetir exportações com falha
1. **Resolução do Monitor**: verifique se os itens ressincronizados mostram o status de êxito

### Corrigir problemas comuns

#### Altas taxas de falha

**Sintomas**: grande número de registros mostrando o status &quot;Falha, requer atenção&quot;

**Causas potenciais**:

* Alterações na configuração do serviço externo
* Incompatibilidades de formato de dados
* Problemas de autenticação ou permissão

**Etapas de resolução**:

1. Verificar o status e a configuração do serviço externo
1. Revisar mensagens de erro por padrões
1. Verificar credenciais de autenticação
1. Entre em contato com o suporte do serviço externo, se necessário

#### Desempenho de exportação lento

**Sintomas**: alta lista de pendências de changelog, atualizações lentas de status

**Causas Possíveis**:

* Problemas de desempenho do indexador
* Alto volume de dados
* Limitação da taxa de serviço externa

**Etapas de Resolução**:

1. Verifique o status do indexador e execute novamente se for inválido
2. Monitorar tempos de resposta do serviço externo
3. Considere o agendamento de exportações fora do horário de pico
4. Analisar o desempenho e os recursos do sistema

#### Falhas de autenticação

**Sintomas**: códigos de status 401 ou 403

**Etapas de Resolução**:

1. Verificar credenciais e tokens da API
1. Verificar permissões de conta de serviço externo
1. Renovar tokens de autenticação expirados
1. Entre em contato com seu provedor de serviços para resolver problemas de acesso

>[!MORELIKETHIS]
>
>* [Painel de gerenciamento de dados](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/systems/data-transfer/data-dashboard)
>* [Guia De Exportação De Dados SaaS](https://experienceleague.adobe.com/pt-br/docs/commerce-merchant-services/saas-data-export/overview)
