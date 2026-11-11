---
title: Catálogos de Preços
description: Saiba como os catálogos de preços são mapeados a partir dos dados de catálogo e preço em [!DNL Adobe Commerce].
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="Somente SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplicável a instâncias do Adobe Commerce as a Cloud Service provisionadas apenas com CCDM (infraestrutura SaaS gerenciada pela Adobe)."
TQID: 'https://experienceleague.adobe.com/8gpl-l6oQebTnrt-00-n1FEdKnzqhTQi3hRz4lrGQoE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 3033d2ab-c1d2-5b52-b865-72d9e5ad2c37
    internal-label: Currency
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 1041abe0e7d7c1212a717d5fd03180ce7fd32958
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%
---
# Catálogos de preços

Os catálogos de preços definem os preços do produto para uma origem de catálogo em níveis e mercados do cliente. Elas suportam uma hierarquia de catálogos de preços pai e filho.

![Hierarquia do Catálogo de Preços](../assets/price-book-hier.png)

## Principais conceitos

| Termo | Descrição |
| ------ | ------------- |
| **Catálogo de Preços** | Agrupamento lógico que define preços para uma origem de catálogo; por exemplo, região específica ou nível de cliente e é usado para gerenciar preços de produtos. |
| **Catálogo de Preços de Fallback** | O catálogo de preços mais alto em uma hierarquia. Ele não tem pai e é o catálogo de preços *only* que define a moeda para ele mesmo e para todos os seus catálogos de preços descendentes.<br/><br/>Se nenhum pai for definido durante a criação do catálogo de preços (por meio da API), um novo catálogo de preços de fallback será criado. |
| **Catálogo de Preços Pai** | Um catálogo de preços de nível superior do qual um catálogo de preços filho pode herdar preços se eles não estiverem explicitamente definidos no filho. |
| **Profundidade da Hierarquia** | Máximo de três níveis (Fallback -> Filho -> Netinho)<br/><br/>não aplicados no momento da assimilação. |
| **Moeda** | Definido somente para o catálogo de preços de fallback. Herdado por todos os catálogos de preços filhos.<br/><br/>Se a moeda não for especificada durante a criação do catálogo de preços de fallback (por meio da API), a moeda assumirá USD como padrão. |
| **Preço do produto** | O preço específico atribuído a um produto (SKU) em um catálogo de preços específico. |
| **Descontos** | Os descontos são definidos no preço do produto. Não herdado. |

## Implementação do catálogo de preços

Ao usar o Adobe Commerce as a Cloud Service com o modelo de dados de catálogo combinável (CCDM), as tabelas de preços são mapeadas a partir dos dados de catálogo e de preços. Eles não são criados manualmente.

Em um nível superior, o mapeamento é:

- **Exibição de loja → Origem do catálogo** — Os dados de produto de exibição de loja, incluindo atributos localizados, são mapeados para uma origem de catálogo.
- **Site → Catálogo de preços ou catálogos de preços**—O preço do site mapeia para o(s) catálogo(s) de preços aplicável(is).
- **Preços do grupo de clientes → Entradas do catálogo de preços**—Os preços do grupo de clientes mapeiam as entradas de preços relevantes.

Mantenha o catálogo de origem, o site e a configuração de precificação na configuração do Adobe Commerce e, em seguida, atribua os catálogos de preços mapeados na exibição de catálogo relevante configurando os catálogos de preços disponíveis. Se nenhum catálogo de preços for atribuído, a exibição do catálogo usará o catálogo de preços padrão.

Uma exibição de catálogo usa a configuração de catálogos de preços disponíveis com seus dados e políticas de catálogo para determinar a experiência de merchandising, incluindo os preços retornados para os produtos.

>[!NOTE]
>
>Para o Commerce B2B, o sistema cria e atribui um único catálogo de preços a cada visualização de catálogo com base na configuração do catálogo compartilhado. Não é necessário configurar a disponibilidade do catálogo de preços para essas exibições.

## Preços de check-out

As tabelas de preços suportam a experiência de catálogo de merchandising e vitrine. O Commerce Core continua a lidar com carrinho e check-out. Um preço disponível somente no CCDM não se torna automaticamente o preço usado pelo check-out.

Mantenha os preços consistentes com a configuração principal do Commerce e teste os preços exibidos, o carrinho, as promoções e o check-out como parte da validação da implementação.

## Exibir catálogos de preços

Depois que a sincronização de dados do catálogo for concluída, exiba os catálogos de preços disponíveis e suas IDs no espaço de trabalho **[!UICONTROL Catalog views]**.

1. Vá para _Configuração da loja_ e clique em **[!UICONTROL Catalog views]**.

1. Clique em **[!UICONTROL Create catalog view]**.

1. Revise os catálogos de preços disponíveis na seção **[!UICONTROL Price Books]** da configuração de exibição do catálogo.

   ![Nomes e IDs do Catálogo de Preços](../assets/price-book-name-ids.png)

## Configurar disponibilidade do catálogo de preços

Associe catálogos de preços mapeados a exibições de catálogo configurando catálogos de preços disponíveis no espaço de trabalho Exibições de Catálogo no Administrador do Commerce.

>[!NOTE]
>
>Uma exibição de catálogo privado (uma com [!UICONTROL Catalog Protection] habilitada) pode fazer referência a apenas um catálogo de preços.

1. No espaço de trabalho **[!UICONTROL Catalog views]**, selecione a exibição de catálogo que deseja configurar.

1. Na seção **[!UICONTROL Price Books]**, selecione os catálogos de preços disponíveis para lojas com suporte na exibição de catálogo.
