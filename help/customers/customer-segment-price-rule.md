---
title: Segmentos do cliente em regras de preço
description: Saiba mais sobre como associar segmentos de clientes a uma regra de preço de carrinho para poder definir promoções direcionadas para sua loja.
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
TQID: https://experienceleague.adobe.com/MSMNikJwG2lQuLlQxnK82zjCOeF-u8JEjmabKFJgpZU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# Segmentos do cliente em regras de preço

{{ee-feature}}

Um segmento de cliente pode ser usado para promoções segmentadas, associando-o a uma [regra de preço do carrinho](../merchandising-promotions/price-rules-cart.md).

![Regra de preço do carrinho - segmento de cliente direcionado](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_&#x200B;**Para associar um segmento a uma regra de preço de carrinho:**&#x200B;_

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _Promoções_ > **[!UICONTROL Cart Price Rules]**.

1. Abrir uma regra nova ou existente:

   * Para usar uma nova regra, clique em **[!UICONTROL Add New Rule]** no canto superior direito.
   * Para usar uma regra existente, clique na regra na lista para abri-la no modo de edição.

1. Role para baixo e expanda a seção **[!UICONTROL Conditions]**.

1. Adicione a condição.

   * Clique no ícone _Adicionar_ (![Ícone de Lista](../assets/icon-add-green-circle.png)), que exibe a lista de condições. Em seguida, escolha **[!UICONTROL Customer Segment]**.

   ![Regra de preço do carrinho - adicionar condição de segmento de cliente](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   Por padrão, a condição é definida para encontrar uma condição correspondente. Se necessário, clique no link **[!UICONTROL matches]** e altere o operador para um dos seguintes:

   * `does not match`
   * `is one of`
   * `is not one of`

   ![Operador de condição](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. Para direcionar um segmento específico, clique no link Mais **...** para exibir opções adicionais. Em seguida, clique no ícone _Seletor_ (![Ícone de Lista](../assets/icon-list-chooser.png)) para exibir a lista de segmentos de clientes.

1. Na lista, marque a caixa de seleção de cada segmento que você deseja direcionar com a condição.

   ![Regra de preço do carrinho - lista do seletor de condições](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Select]** para colocar os segmentos de clientes selecionados na condição.

1. Complete o restante da regra de preço, conforme necessário.

1. Quando terminar, clique em **[!UICONTROL Save]**.
