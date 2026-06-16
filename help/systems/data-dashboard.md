---
title: Painel de gerenciamento de dados
description: Saiba como acessar insights sobre fluxos de dados para  [!DNL Catalog Service], [!DNL Live Search] e [!DNL Product Recommendation]s.
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
TQID: https://experienceleague.adobe.com/5WxRmKbBDfWM4JHypuXKCmrUTn5VjQeAUdLRJUWQXtc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 802
ht-degree: 0%

---

# Painel de gerenciamento de dados

O Painel de gerenciamento de dados oferece uma visão geral do status de sincronização para dados de produtos transferidos do banco de dados do Commerce para os serviços SaaS da Commerce. Os usuários podem monitorar convenientemente os status de sincronização de produtos e iniciar a ressincronização de dados a partir de um painel unificado. Esse recurso fornece informações valiosas sobre a disponibilidade de dados de produtos para sua loja, garantindo que eles possam ser exibidos imediatamente para seus compradores.

>[!NOTE]
>
>Se você instalou o [Conector do Adobe Commerce Optimizer](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/overview) para exportar dados de catálogo para o Adobe Commerce Optimizer, use a [página Sincronização de Dados](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync) no Commerce Optimizer Studio para verificar se a sincronização de dados foi bem-sucedida, em vez do Painel de Gerenciamento de Dados.

## Público-alvo

O Painel de Gerenciamento de Dados está disponível sem custo adicional para todos os comerciantes do Commerce que usam o [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview), [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce/live-search/guide-overview) ou [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview) com uma licença ativa.

O Painel de Gerenciamento de Dados está localizado em *Sistema* > Transferência de Dados > *Painel de Gerenciamento de Dados*.

![Painel de gerenciamento de dados](assets/data-management-dashboard.png)

O painel contém os seguintes campos:

| Campo | Descrição |
|--- |--- |
| Escopo | Site específico para os dados sincronizados. |
| [!DNL Product Recommendations] | Exibe o status da sincronização, o número de produtos sincronizados e uma tabela dos [exibíveis](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) produtos sincronizados para [!DNL Product Recommendations]. |
| [!DNL Live Search] | Exibe o status da sincronização, o número de produtos sincronizados e uma tabela dos [exibíveis](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) produtos sincronizados para [!DNL Live Search]. |
| [!DNL Catalog Service] | Exibe o status da sincronização, o número de produtos sincronizados e uma tabela dos produtos sincronizados para [!DNL Catalog Service]. |
| Configurações | Abre uma caixa de diálogo onde você pode [ressincronizar manualmente os dados do catálogo](#resync-catalog-data). |
| Status de sincronização | Exibe o número de produtos que foram transferidos do banco de dados do Commerce para qualquer um dos serviços SaaS nas últimas três horas. Se você fizer atualizações pouco frequentes no catálogo, esse valor será frequentemente zero. Se uma sincronização estiver em andamento, clique em **[!UICONTROL Refresh]** para obter uma contagem atualizada. |
| Contagem de produtos | Reflete o número total de produtos de catálogo disponíveis para o serviço. Os painéis [!DNL Product Recommendations] e [!DNL Live Search] exibem o número total de produtos _exibíveis_. O [!DNL Catalog Service] não filtra produtos por exibível, portanto, se você tiver o [!DNL Catalog Service] e o [!DNL Live Search] ou o [!DNL Product Recommendations] instalados, é possível que os dois painéis mostrem dois valores diferentes para a contagem de produtos. |
| Produtos sincronizados | Fornece detalhes sobre os produtos no índice Commerce principal. Por padrão, essa tabela é classificada por &quot;Última atualização&quot;. Para localizar um produto específico, use o campo **[!UICONTROL Search by SKU]**. Para controlar quais colunas são exibidas, clique em **[!UICONTROL Customize Table]** à direita da tabela. |

## Uso do painel de Gerenciamento de dados

Ao atualizar produtos no banco de dados do Commerce, os dados do produto são transferidos para os serviços SaaS de acordo com a configuração do sistema. Quando o processo de sincronização é iniciado, **Contagem de produto** indica o número de produtos enviados para os serviços SaaS.

>[!IMPORTANT]
>
>O tempo necessário para concluir a sincronização varia de acordo com o tamanho do catálogo e o volume de dados atualizados.

Quando o número de produtos processados corresponde ao número de produtos atualizados, indica que a sincronização está concluída.

>[!NOTE]
>
>A Adobe também fornece uma interface de linha de comando e registros do sistema que desenvolvedores e integradores de sistemas podem usar para gerenciar e rastrear operações de sincronização e solucionar erros de serviços SaaS da Commerce. Para obter detalhes, consulte o [Guia de Exportação de Dados SaaS](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview).

### Lista de produtos sincronizados

Para ver os detalhes de um produto sincronizado, clique no produto na tabela.

![Detalhes do produto sincronizado](assets/sync-product-detail.png)

### Ressincronizar dados do catálogo

Para garantir que seus serviços SaaS da Commerce estejam sempre atualizados com as informações mais recentes do produto, você deve [implementar um agendamento](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex) para sincronizar os dados do catálogo.

Embora você possa [iniciar manualmente](#manually-resync-catalog) uma ressincronização de dados de catálogo do banco de dados do Commerce para serviços SaaS, isso não é recomendado, pois pode aumentar a carga nos recursos de hardware. No entanto, a ressincronização manual do catálogo pode ser necessária nos seguintes cenários:

- Sempre que alterações significativas forem feitas no catálogo de produtos, como adicionar novos produtos, atualizar detalhes do produto ou modificar categorias

- Se você observar discrepâncias ou problemas de desempenho na exibição dos dados do produto em suas lojas

- Após qualquer atualização ou alteração nas integrações entre o banco de dados do Commerce e os serviços SaaS

- Ao implantar personalizações ou configurações que afetam o gerenciamento de dados do produto ou os processos de sincronização

Seguindo essas diretrizes e ressincronizando proativamente os dados do catálogo conforme necessário, você pode manter a consistência, a precisão e a confiabilidade dos dados em todo o ecossistema do Adobe Commerce.

#### Ressincronizar manualmente o catálogo

Se você precisar ressincronizar os dados do catálogo, clique em **[!UICONTROL Settings]** no lado direito da página para exibir uma caixa de diálogo onde você pode iniciar uma ressincronização. A ressincronização dos dados do catálogo força o serviço a buscar novamente os dados do banco de dados do Commerce nos serviços SaaS.

![Sincronizar Produtos Manualmente](assets/resync-data.png)
