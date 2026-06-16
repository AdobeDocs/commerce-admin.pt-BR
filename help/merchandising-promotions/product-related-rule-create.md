---
title: Criar uma regra de produto relacionada
description: Saiba como criar uma regra de produto relacionada que pode ser acionada para exibir produtos relacionados, vendas adicionais e vendas cruzadas.
exl-id: fbc059ec-d3e6-46ca-810a-a979a0631dd8
feature: Merchandising, Products, Storefront
TQID: https://experienceleague.adobe.com/jfs0iFZxLKfvJpRGLA6Hi1dADcGEvm4PJIolOf2nfI4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 648
ht-degree: 0%

---

# Criar uma regra de produto relacionada

{{ee-feature}}

O processo de criação de uma regra de produto relacionada é semelhante à configuração de uma regra de preço. Primeiro, defina as condições a serem atendidas e escolha os produtos que deseja exibir. Em um determinado momento, pode haver várias regras ativas que podem ser acionadas para exibir produtos relacionados, vendas adicionais e vendas cruzadas. A prioridade de cada regra determina a ordem na qual o bloco de produtos aparece na página.

>[!NOTE]
>
>Para que um atributo seja usado em uma regra de destino, a propriedade [_[!UICONTROL Use for Promo Rule Conditions]_](../catalog/product-attributes.md) deve ser definida como `Yes`.

>[!NOTE]
>
>O valor do escopo `All Store Views` é sempre usado para as condições [!UICONTROL Products to Match] e [!UICONTROL Products to Display] para todos os atributos de produto. Isso também se aplica quando os atributos do produto têm valores diferentes para diferentes exibições e sites da loja.

## Criar uma regra de produto relacionada

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. No canto superior direito, clique em **[!UICONTROL Add Rule]**.

   ![Regra de produtos relacionados - informações](./assets/catalog-related-products-rule-information.png){width="600" zoomable="yes"}

1. Conclua o **[!UICONTROL Rule Information]** da seguinte maneira:

   - Insira um **[!UICONTROL Rule Name]** para identificar a regra ao trabalhar no Administrador.

   - Para **[!UICONTROL Priority]**, insira um número que determine a ordem em que os resultados aparecem na página quando os resultados de outras regras são direcionados para o mesmo local. O número `1` é a prioridade máxima.

   - Para habilitar a regra, defina **[!UICONTROL Status]** como `Active`.

   - Defina **[!UICONTROL Apply To]** como um dos seguintes:

      - `Related Products`
      - `Up-sells`
      - `Cross-sells`

   - Se a regra for ficar ativa por um período específico, insira as datas **[!UICONTROL From]** e **[!UICONTROL To]**.

   - Para **[!UICONTROL Result Limit]**, insira o número de registros a serem exibidos na lista de resultados. O número máximo é 20.

   - Se a regra se aplicar a um [segmento de cliente](../customers/customer-segments.md) específico, defina **[!UICONTROL Customer Segments]** como `Specified` e escolha o segmento de cliente na lista.

   - Se a regra se aplicar a um [público-alvo do Real-Time CDP](../customers/audience-activation.md) específico, defina **[!UICONTROL Real-Time CDP Audience]** como `Specified` e escolha o público-alvo do Real-Time CDP na lista.

     ![Regra de produtos relacionados - Público-alvo da Real-Time CDP](./assets/rtcdp-related-products.png){width="500"}

1. No painel esquerdo, escolha **[!UICONTROL Products to Match]** e crie as condições como você faria para uma [regra de preço de catálogo](price-rules-catalog.md).

   ![Regra de produtos relacionados - produtos a serem correspondidos](./assets/catalog-related-products-match.png){width="500"}

1. No painel esquerdo, escolha **[!UICONTROL Products to Display]** e crie as condições de resultados como você faria para uma [regra de preço de catálogo](price-rules-catalog.md).

   ![Regra de produtos relacionados - produtos a serem exibidos](./assets/catalog-related-products-to-display.png){width="500"}

   Complete a condição para descrever os produtos que deseja incluir nos resultados exibidos.

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Excluir uma regra de produto relacionada

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. Localize a regra de produto relacionada que deseja excluir.

1. Clique na regra para abrir a página de detalhes.

1. No canto superior direito, clique em **[!UICONTROL Delete]**.

1. Para confirmar a ação, clique em **[!UICONTROL OK]**.

## Demonstração de regra de produto relacionada

Assista a este vídeo para saber mais sobre como criar regras de produto relacionadas:

>[!VIDEO](https://video.tv.adobe.com/v/343837?quality=12&learn=on)

## Descrições dos campos

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Rule Name] | Um nome que identifica a regra para uso interno. |
| [!UICONTROL Priority] | Determina a sequência em que os resultados da regra aparecem quando exibidos com outros conjuntos de resultados que têm como alvo o mesmo local na página. O valor pode ser definido como qualquer número inteiro, com a prioridade mais alta de 1. Por exemplo, se houver várias regras de venda adicional aplicáveis, a de maior prioridade será exibida antes das outras. A ordem de classificação dos produtos em cada conjunto de resultados é aleatória. Qualquer venda adicional, venda cruzada e produto relacionado que foi configurado manualmente sempre aparecem na página antes de qualquer promoção de produto baseada em regras. |
| [!UICONTROL Status] | Controla o status ativo da regra. Opções: `Active` / `Inactive` |
| [!UICONTROL Apply To] | Identifica o tipo de relacionamento de produto associado à regra. Opções: `Related Products` / `Up-sells` / `Cross-sells` |
| [!UICONTROL From Date] | Se a regra estiver ativa por um intervalo de tempo, essa configuração determinará a primeira data em que a regra estará ativa. |
| [!UICONTROL To Date] | Se a regra estiver ativa por um intervalo de tempo, essa configuração determinará a última data em que a regra ficará ativa. |
| [!UICONTROL Result Limit] | Determina o número de produtos que aparecem nos resultados de uma vez. O número máximo é 20. Se mais resultados correspondentes forem encontrados, os produtos girarão pelo bloco sempre que a página for atualizada. |
| [!UICONTROL Customer Segments] | Identifica os segmentos de clientes aos quais a regra se aplica. Opções: `All` / `Specified` |

{style="table-layout:auto"}
