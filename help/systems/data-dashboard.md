---
title: Painel de gerenciamento de dados
description: Saiba mais sobre o Painel de gerenciamento de dados
feature: Products, Customers, Data Import/Export
source-git-commit: 925af4d3841f2972dfffcd52125a41c4a4b28815
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Painel de gerenciamento de dados

O Painel de gerenciamento de dados fornece informações sobre fluxos de dados para produtos SaaS da Adobe Commerce. Usuários de [!DNL Live Search], [!DNL Product Recommendations], e [!DNL Catalog Service] O pode exibir os status de sincronização do produto e ressincronizar os dados de um único painel.

O Painel de gerenciamento de dados está localizado em *Sistema* > Transferência de dados > *Painel de gerenciamento de dados*.

![Painel de gerenciamento de dados](assets/data-management-dashboard.png)

## Configurações

O botão Settings no lado direito da página abre a variável [[!DNL Catalog Sync]](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/data-services/catalog-sync.html) caixa de diálogo de configurações.

Normalmente, a variável [!DNL Catalog Sync] O processo do é executado automaticamente, uma vez por hora.

A ressincronização dos dados do catálogo força o serviço a buscar novamente os dados do banco de dados do Commerce, garantindo que as alterações mais recentes sejam refletidas no serviço e no site. Use este botão se você tiver feito várias alterações no produto e precisar atualizá-las antes do processo de sincronização automática normal.

## Status de sincronização

A variável _[!UICONTROL Sync]_o painel de status informa o número de produtos que foram sincronizados nas últimas três horas. Se você fizer atualizações pouco frequentes no catálogo, esse valor será frequentemente zero. Clique em **[!UICONTROL Refresh]**para atualizar a contagem.

## Contagem de produtos

O painel de contagem de produtos reflete o número total de produtos de catálogo disponíveis para o serviço.

A variável [!DNL Catalog Service] o painel reflete o número total de produtos no catálogo disponível para o serviço. Geralmente, esses são todos os produtos no banco de dados do Commerce.

Os painéis Recommendations do produto e Live Search exibem o número total de [_pesquisável_](https://experienceleague.adobe.com/docs/commerce-admin/catalog/catalog/search/search.html) produtos. Se alguns produtos não estiverem configurados para serem pesquisados, isso contabilizará a diferença nos totais dos produtos entre [!DNL Product Recommendations] e [!DNL Live Search], e [!DNL Catalog Service].

## Produtos sincronizados

A tabela Produtos de Catálogo Sincronizados fornece detalhes sobre os produtos no índice. Por padrão, essa tabela é classificada por &quot;Última atualização&quot;.

Para encontrar um produto específico, use o **[!UICONTROL Search by SKU]** campo .
Para controlar quais colunas são exibidas, clique em **[!UICONTROL Customize Table]** à direita da mesa.
