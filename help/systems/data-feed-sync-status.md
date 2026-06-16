---
title: Monitoramento do status de sincronização do feed de dados
description: Monitore a sincronização da exportação de dados e identifique problemas ou atrasos no processamento do feed para  [!DNL Catalog Service], [!DNL Live Search] e [!DNL Product Recommendations].
feature: Products, Customers, Data Import/Export
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
exl-id: 4e1b9da0-450c-4488-8693-1938a948e792
TQID: https://experienceleague.adobe.com/Y8vYxKS-8iX-bCLSJpAiJOItWlJk348bSMWfk1Cgpbg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1689
ht-degree: 0%

---

# Monitoramento do status de sincronização do feed de dados

Os administradores do Adobe Commerce podem monitorar o status de sincronização dos dados exportados do Adobe Commerce para os serviços conectados do Commerce usando a página Status de sincronização do feed de dados no administrador do Commerce.

![Página de detalhes Status da Sincronização do Feed de Dados com relatórios de status do item de feed](assets/data-feed-sync-status.png)

Esta página fornece insights em tempo real sobre a integridade e o desempenho dos feeds de exportação de dados que transferem dados de produto e categoria da Commerce para serviços externos, como [!DNL Product Recommendations], [!DNL Live Search] e [!DNL Catalog Service].

A página de status da sincronização mostra apenas o status da exportação. Um status bem-sucedido indica que os dados foram exportados com êxito e estarão disponíveis nos serviços conectados da Commerce.

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

## Verificar se os dados foram sincronizados com êxito com os Serviços Commerce

Use os métodos a seguir para verificar se os dados foram sincronizados com êxito com os serviços conectados da Commerce:

* Para o Adobe Commerce na nuvem ou no local, ou para implantações do Adobe Commerce as a Cloud Service, verifique o [painel de gerenciamento de dados](data-dashboard.md).
* Para implantações do Adobe Commerce na nuvem ou locais configuradas com o [Conector do Adobe Commerce Optimizer](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/overview), verifique a [página Sincronização de Dados](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync) no Commerce Optimizer Studio.

>[!TIP]
>
>Para saber mais sobre o processo de sincronização de dados, consulte [Sincronizar dados com a exportação de dados SaaS](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/data-synchronization)no *Guia de Exportação de Dados SaaS*.

## Instalar a extensão

A página Status do feed de dados está disponível para todos os comerciantes da Commerce com licenças ativas para os seguintes serviços da Commerce:

* [[!DNL Product Recommendations v6.0.0+]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)
* [[!DNL Live Search v4.1.0+]](https://experienceleague.adobe.com/en/docs/commerce/live-search/guide-overview)
* [[!DNL Catalog Service v1.17+]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview) com uma licença ativa

>[!NOTE]
>
>Não é necessário instalar a extensão Status do Feed de Dados em [[!DNL Adobe Commerce as a Cloud Service]](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/overview) instâncias.
>A extensão estará disponível por padrão se pelo menos um dos seguintes serviços estiver habilitado na implantação do Commerce: Product Recommendations v6+, Live Search v4.1+ ou Catalog Service v1.17+.

**Requisitos**

* PHP 8.1, 8.2, 8.3 ou 8.4
* Adobe Commerce 2.4.4+
* [Extensão de Exportação de Dados do Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/manage-extension), versão 103.4.15 ou posterior
* Acesso ao [repo.magento.com](https://repo.magento.com)

  Para gerar chaves e obter os direitos necessários, consulte [Obter suas chaves de autenticação](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Para instalações na nuvem, consulte o [Guia de Infraestrutura do Commerce na Nuvem](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/authentication-keys).

* Acesso à linha de comando do servidor de aplicativos do Adobe Commerce.

### Etapas de instalação

Adicionar o módulo `magento/module-data-exporter-status` usando o Composer:

```shell
composer require magento/module-data-exporter-status
```

Para ver as etapas detalhadas de instalação, consulte os guias a seguir:

* [Instalar extensão no Adobe Commerce na infraestrutura em nuvem](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure-store/extensions)

* [Instalar extensão do Adobe Commerce no local](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/tutorials/extensions)

## Acessar a página Status do feed de dados

No Administrador do Commerce, acesse a página Status do feed de dados do Administrador do Commerce em **[!DNL System]** > Transferência de dados > **[!DNL Data Feed Sync Status]**.

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
>Para saber mais sobre o processamento de índice, consulte o tópico [Gerenciamento de índice](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/index-management).

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
>O Adobe também fornece ferramentas de interface de linha de comando e registros do sistema que desenvolvedores e integradores de sistemas podem usar para gerenciar e rastrear operações de sincronização. Para obter detalhes, consulte o [Guia de Exportação de Dados SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

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
>* [Painel de gerenciamento de dados](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/data-transfer/data-sync/data-dashboard)
>* [Guia De Exportação De Dados SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview)
