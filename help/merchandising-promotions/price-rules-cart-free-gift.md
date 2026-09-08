---
title: Promoções de presentes gratuitos
description: Saiba como configurar uma promoção de presente gratuito com regras de preço de carrinho para oferecer um presente gratuito quando um conjunto de condições for atendido.
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
TQID: https://experienceleague.adobe.com/FR-q4Qj-ZDDzmfEKSvSj-BlwsM7ro-BqAE1yCppTaXE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-git-commit: 3cddc90c619a27b1404e0be7bb4b2c9a3b77e443
workflow-type: tm+mt
source-wordcount: 349
ht-degree: 0%

---


# Promoção do presente gratuito

A promoção *Presente Gratuito* permite definir uma [regra de preço do carrinho](price-rules-cart.md) que adiciona um item gratuito ao carrinho sob condições específicas.

>[!NOTE]
>
>Esse recurso não é compatível com vitrines Luma. Ele pode ser acessado por meio do [GraphQL](https://developer.adobe.com/commerce/webapi/graphql/schema/cart/mutations/select-free-gift/) e está disponível nas vitrines do Edge Delivery Services (EDS).

## Criar uma promoção de presente gratuito

Esta seção descreve como criar uma promoção de presente gratuito usando o seguinte formato:

**Compre um produto X, ganhe um produto Y grátis**

1. [Crie uma regra de preço de carrinho](price-rules-cart.md#step-1-add-a-rule) com uma promoção de presente gratuito.

1. [Descreva as condições](price-rules-cart.md#step-2-describe-the-conditions) das instruções do carrinho para definir as condições da regra de preço. Essa é a primeira de várias condições que podem ser adicionadas à regra e determina quando a regra é acionada. Ela pode ser baseada em uma combinação dos seguintes:

   - Atributos do produto
   - Produtos
   - Atributos do carrinho
   - Segmentos de clientes do Adobe Commerce

   Se deixado em branco, a regra será acionada para cada carrinho.

   ![Regra de preço do carrinho - condições](./assets/conditions.png){width="600" zoomable="yes"}

1. Defina as ações para a regra de preço do carrinho:

   1. Expanda  (../assets/icon-display-expand.png) a seção **[!UICONTROL Actions]** e insira as seguintes informações:

   - Defina **[!UICONTROL Apply]** como `Free Gift`.
   - Em **[!UICONTROL Gift SKU(s)]**, selecione uma ou mais SKUs que o cliente pode escolher como presente gratuito.
   - Defina **[!UICONTROL Free Gift Discount Type]** como **[!UICONTROL Price Based]** ou **[!UICONTROL Discount Based]**.
   - Em **[!UICONTROL Gift Qty]**, insira a quantidade do presente gratuito que o cliente recebe. Por exemplo, digite `2` se quiser que o cliente receba dois itens gratuitos.
   - Para evitar a aplicação de outros descontos, defina **[!UICONTROL Discard subsequent rules]** como `Yes`.

   1. Clique em **[!UICONTROL Save and Continue Edit]** e conclua o restante da regra conforme necessário.

1. [Conclua o rótulo](price-rules-cart.md) das instruções de regra de preço do carrinho para inserir o rótulo que aparece durante o check-out.

![Regra de preço do carrinho - Etiqueta de presente gratuito](./assets/free-gift-promotion-label.png){width="600" zoomable="yes"}

{{new-price-rule}}

1. Quando a regra estiver concluída, clique em **[!UICONTROL Save Rule]**.

## Variações

Você pode personalizar as regras de preço do carrinho de várias maneiras diferentes. O recurso Presente gratuito pode ser configurado com dois tipos de desconto diferentes:

- **Baseado em preço**: um item de linha de presente é adicionado ao preço de `0`.
- **Baseado em Desconto** : um desconto total é aplicado ao item de linha de presente.
