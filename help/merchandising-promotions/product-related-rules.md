---
title: Regras de produto relacionadas
description: Saiba mais sobre as regras de produtos relacionados e como elas são usadas para apresentar dinamicamente produtos relacionados, vendas adicionais e vendas cruzadas aos clientes.
exl-id: ff566e13-cbe8-42f1-be3a-684e364b86dd
feature: Merchandising, Products, Storefront
source-git-commit: 4971fe457b7fd58d8b71951981bc889386610a99
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# Regras de produto relacionadas (regras de público alvo)

{{ee-feature}}

As regras de produtos relacionados permitem direcionar a seleção de produtos apresentados aos clientes como produtos relacionados, vendas adicionais e vendas cruzadas. Cada regra de produto pode ser associada a um [segmento de cliente](../customers/customer-segments.md) para produzir uma exibição dinâmica de merchandising direcionado.

Como várias regras ativas podem ser acionadas ao mesmo tempo, você pode definir uma prioridade para cada regra. Ele define a ordem em que as regras são aplicadas e os produtos são exibidos na página.

Para acessar as regras de produto relacionadas, acesse **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

![Lista de regras de produto relacionadas](./assets/related-products-rules.png){width="700" zoomable="yes"}

## Descrições da coluna

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL ID] | Um identificador numérico exclusivo atribuído a cada regra de produto relacionada |
| [!UICONTROL Rule] | O nome da regra de produto relacionada |
| [!UICONTROL Start] | Use os campos de calendário dinâmico (_[!UICONTROL To:]_&#x200B;e&#x200B;_[!UICONTROL From:]_) para filtrar a lista com base na data de início da regra, conforme definido quando a regra foi criada. |
| [!UICONTROL End] | Use os campos de calendário dinâmico (_[!UICONTROL To:]_&#x200B;e&#x200B;_[!UICONTROL From:]_) para filtrar a lista com base na data final da regra, conforme definido quando a regra foi criada. |
| [!UICONTROL Priority] | Insira texto neste campo para filtrar a lista com base na prioridade definida para uma regra. |
| [!UICONTROL Applies To] | Esta opção filtra a lista de regras que se aplicam a `Related Products`, `Up-sells` e `Cross-sells`. |
| [!UICONTROL Status] | Use esta opção para filtrar a lista com base no status da regra (`Active` ou `Inactive`). |

{style="table-layout:auto"}

## Prioridade da regra

Em um determinado momento, pode haver várias regras ativas que podem ser acionadas para exibir produtos relacionados, vendas adicionais e vendas cruzadas. A prioridade de cada regra determina a ordem em que os produtos aparecem na página. O valor pode ser definido como qualquer número inteiro, com `1` tendo a prioridade mais alta.

O número de IDs de produtos que podem ser incluídas em uma regra de relações de produtos é determinado pelo valor `Result Limit`, que tem um máximo de 20. O valor `Result Limit`, combinado com o `Configurable Maximum` para a promoção de produto baseada em regras específica torna-se o `Real Limit`, e determina o número real de produtos correspondentes que podem aparecer na lista.

[Limite de Resultados] + [Máximo Configurável] = [Limite Real]

Por exemplo, suponha que você tenha três regras com prioridade `1`, `2` e `3`.

- Há dois produtos correspondentes retornados para a _Regra 1_, seis produtos correspondentes para a _Regra 2_ e vinte produtos correspondentes para a _Regra 3_.
- Na configuração, o _[!UICONTROL Maximum Number of Products for Related Products List]_&#x200B;está definido como `6`.

  | Regras | Prioridade | Produtos de correspondência |
  |---|---|-----|
  | Regra 1 | `1` | `2` |
  | Regra 2 | `2` | `6` |
  | Regra 3 | `3` | `20` |

Se a primeira regra retornar mais produtos correspondentes do que o permitido pelo _limite máximo configurável_, mas menos do que o _limite real_, os produtos correspondentes das outras regras serão usados (em ordem de prioridade) até que o _limite real_ seja atingido.

Por prioridade, os produtos correspondentes retornados da _Regra 1_ podem ser usados primeiro para preencher todos os 26 slots disponíveis. Como a Regra 1 retornou apenas dois produtos correspondentes, ainda há espaço para mais 24. _A Regra 2_ tem a próxima prioridade mais alta e retorna mais seis produtos correspondentes. Agora há 18 slots disponíveis a serem preenchidos. _A regra 3_ tem o próximo nível de prioridade, com produtos correspondentes suficientes para preencher os 18 slots restantes. Quando todos os slots disponíveis estiverem preenchidos e dependendo do modo de rotação definido, os produtos poderão ser embaralhados ou ordenados por ID dentro de cada prioridade e depois reduzidos ao limite máximo configurável. Nesse caso, os seis produtos restantes aparecem na loja.

>[!NOTE]
>
>Os produtos selecionados são sempre exibidos antes dos produtos com base em regras, independentemente do modo de rotação.

## Configurar relações de produto baseadas em regras

O comportamento das regras de relacionamento do produto e a exibição de produtos correspondentes são determinados pelas definições de configuração. Essas configurações determinam quantos produtos que correspondem à regra podem ser exibidos e a ordem em que são exibidos.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel à esquerda, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo.

1. Expanda ![Expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Rules-Based Product Relations]**.

   ![Configuração de catálogo - relações de produto baseadas em regras](../configuration-reference/catalog/assets/catalog-rule-based-product-relations.png){width="600" zoomable="yes"}

1. Insira o **[!UICONTROL Maximum Number of Products in the Related Products List]**.

1. Defina **[!UICONTROL Show Related Products]** como um dos seguintes:

   - `Both Selected and Rule Based`
   - `Selected Only`
   - `Rule-Based Only`

1. Defina **[!UICONTROL Rotation Mode for Products in Related Product List]** como um dos seguintes:

   - `By Priority, Then by ID`
   - `By Priority, Then Random`
   - `Weighted Random`

1. Para concluir as configurações do produto de venda cruzada, faça o seguinte:

   - Insira o **[!UICONTROL Maximum Number of Products in the Cross-Sell Product List]**.

   - Defina **[!UICONTROL Show Cross-Sell Products]** como um dos seguintes:

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - Defina **[!UICONTROL Rotation Mode for Products in Cross-Sell Product List]** como um dos seguintes:

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. Para concluir as configurações do produto de venda adicional, faça o seguinte:

   - Insira o **[!UICONTROL Maximum Number of Products in the Upsell Product List]**.

   - Defina **[!UICONTROL Show Upsell Products]** como um dos seguintes:

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - Defina **[!UICONTROL Rotation Mode for Products in Upsell Product List]** como um dos seguintes:

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Modos de rotação

| Modo | Descrição |
|---|---|
| [!UICONTROL By Priority, Then by ID] | Os produtos são classificados por prioridade e depois reordenados por ID dentro de cada prioridade. Os produtos da regra de prioridade mais baixa aparecem somente quando não são produtos deixados da regra de prioridade mais alta para preencher os slots disponíveis. |
| [!UICONTROL By Priority, Then Random] | Os produtos são classificados por prioridade e depois aleatoriamente em cada prioridade. Os produtos da regra de prioridade mais baixa aparecem somente quando não são produtos deixados da regra de prioridade mais alta para preencher os slots disponíveis. |
| [!UICONTROL Weighted Random] | Os produtos são aleatórios para que os produtos pertencentes a uma regra com prioridade mais alta tenham maior probabilidade de serem exibidos do que aqueles pertencentes a uma regra com prioridade mais baixa. Os produtos são então reduzidos ao limite máximo configurável e reagrupados por prioridade. Esse modo dá a chance aos produtos de prioridade mais baixa aparecerem, às vezes, mesmo se os slots restantes puderem ser preenchidos com produtos de regra com prioridade mais alta |

{style="table-layout:auto"}

## Use os públicos da Real-Time CDP para informar as regras de produto relacionadas

>[!NOTE]
>
>Esse recurso está na versão beta. Se você quiser participar do programa beta, envie uma solicitação para [dataconnection@adobe.com](mailto:dataconnection@adobe.com).


Saiba como [ativar](../customers/audience-activation.md) públicos-alvo da Real-Time CDP na sua instância do Adobe Commerce para informar regras de produto relacionadas.
