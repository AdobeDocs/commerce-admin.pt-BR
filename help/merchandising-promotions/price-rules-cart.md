---
title: Regras de preço do carrinho
description: Saiba mais sobre as regras de preço do carrinho que aplicam descontos aos itens do carrinho com base em um conjunto de condições.
exl-id: f3038f2a-9d34-4696-a39e-f87fbb1294a2
feature: Merchandising, Price Rules, Shopping Cart
TQID: https://experienceleague.adobe.com/i3G3iGuomU0cjy3aX9eynyzAtpCgQxeEFAyRUdUUu44
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
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
source-wordcount: 451
ht-degree: 0%

---

# Regras de preço do carrinho

As regras de preço do carrinho aplicam descontos aos itens do carrinho de compras, com base em um conjunto de condições. O desconto pode ser aplicado automaticamente quando as condições forem atendidas ou quando o cliente inserir um código de cupom válido. Quando aplicado, o desconto é exibido no carrinho abaixo do subtotal. Uma regra de preço do carrinho pode ser usada conforme necessário para uma temporada ou promoção, alterando seu status e intervalo de datas.

>[!NOTE]
>
>Se a regra do carrinho de cupom tiver condições que especificam opções de finalização de compra, como determinados métodos de envio ou de pagamento, as condições serão atendidas somente na finalização de compra após a seleção dos métodos específicos de envio/pagamento. Nesse caso, o cupom pode ser aplicado no check-out na última etapa.

![Exemplo de vitrine - cupom de aplicação do carrinho](./assets/storefront-cart-apply-coupon.png){width="600" zoomable="yes"}

## Acessar regras de preço do carrinho

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

   ![Regra de preço do carrinho](./assets/price-rule-cart.png){width="700" zoomable="yes"}

1. Se você tiver muitas regras, use as opções de filtro na parte superior de cada coluna para simplificar a lista e clique em **[!UICONTROL Search]** para aplicar os filtros.

1. Para limpar todas as opções de filtro e exibir a lista completa, clique em **[!UICONTROL Reset Filter]**.

1. Atualizar propriedades de uma regra:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Clique em **[!UICONTROL Edit]** para exibir a página Informações da Regra.

   - ![Magento Open Source](../assets/open-source.svg) (somente Magento Open Source) Clique na regra na lista para exibir a página Informações da Regra.

   Lá, é possível alterar as configurações da regra (semelhante à criação de uma regra).

## Opções de filtro por coluna

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL ID] | Insira um texto para filtrar a lista de um número de ID de regra específico. |
| [!UICONTROL Rule] | Digite texto para filtrar a lista com base no nome da regra definido quando a regra foi criada. |
| [!UICONTROL Coupon Code] | Insira um texto para filtrar a lista com base no nome do código definido quando a regra foi criada. |
| [!UICONTROL Priority] | Campo de texto livre que filtra a lista com base na prioridade definida para uma regra. |
| [!UICONTROL Status] | Use esta opção para filtrar a lista com base no status da regra (`Active` ou `Inactive`). |
| [!UICONTROL Web Site] | Use essa opção para filtrar a lista com base nos sites definidos para uma regra. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Clique em **[!UICONTROL Edit]** para exibir a página _[!UICONTROL Rule Information]_&#x200B;e atualizar as configurações de regra (semelhante à criação de uma regra). |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (somente Magento Open Source) Use os campos de calendário dinâmico (_[!UICONTROL To:]_&#x200B;e_[!UICONTROL From:]_) para filtrar a lista com base na data de início da regra, conforme definido quando a regra foi criada. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (somente Magento Open Source) Use os campos de calendário dinâmico (_[!UICONTROL To:]_&#x200B;e_[!UICONTROL From:]_) para filtrar a lista com base na data de término da regra, conforme definido quando a regra foi criada. |

{style="table-layout:auto"}

## Use os públicos da Real-Time CDP para informar as regras de preço do carrinho

Saiba como [ativar](../customers/audience-activation.md) públicos-alvo da Real-Time CDP na sua instância do Adobe Commerce para informar as regras de preço do carrinho.
