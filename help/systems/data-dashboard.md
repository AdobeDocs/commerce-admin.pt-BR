---
title: Painel de gerenciamento de dados
description: Saiba como acessar insights sobre fluxos de dados para Serviço de catálogo, Live Search, Recommendations de produto.
feature: Products, Customers, Data Import/Export
source-git-commit: eed80afd8755d416d979c362f8c21fe97ce2d2ba
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# Painel de gerenciamento de dados

O Painel de gerenciamento de dados fornece informações sobre fluxos de dados para produtos SaaS da Adobe Commerce. Usuários de [!DNL Live Search], [!DNL Product Recommendations], e [!DNL Catalog Service] O pode exibir os status de sincronização do produto e ressincronizar os dados de um único painel.

O Painel de gerenciamento de dados está localizado em *Sistema* > Transferência de dados > *Painel de gerenciamento de dados*.

![Painel de gerenciamento de dados](assets/data-management-dashboard.png)

## Configurações

A variável **[!UICONTROL Settings]** no lado direito da página abre a caixa de diálogo, onde é possível ressincronizar os dados do catálogo.

A ressincronização dos dados do catálogo força o serviço a buscar novamente os dados do banco de dados do Commerce. Essa ação geralmente é usada durante a primeira integração quando a sincronização do catálogo não é executada por algumas horas.

## Status de sincronização

A variável _[!UICONTROL Sync]_o painel de status informa o número de produtos que foram sincronizados nas últimas três horas. Se você fizer atualizações pouco frequentes no catálogo, esse valor será frequentemente zero. Clique em **[!UICONTROL Refresh]**para atualizar a contagem.

## Contagem de produtos

O painel de contagem de produtos reflete o número total de produtos de catálogo disponíveis para o serviço.

A variável [!DNL Product Recommendations] e [!DNL Live Search] painéis exibem o número total de _exibível_ produtos. [!DNL Catalog Service] O não filtra produtos por exibíveis, portanto, se você tiver ambos [!DNL Catalog Service] e [!DNL Live Search] ou [!DNL Product Recommendations] instalado, é possível que os dois painéis mostrem dois valores diferentes para a contagem de produtos.

## Produtos sincronizados

A tabela Produtos Sincronizados fornece detalhes sobre os produtos do índice. Por padrão, essa tabela é classificada por &quot;Última atualização&quot;.

Para encontrar um produto específico, use o **[!UICONTROL Search by SKU]** campo .
Para controlar quais colunas são exibidas, clique em **[!UICONTROL Customize Table]** à direita da mesa.
