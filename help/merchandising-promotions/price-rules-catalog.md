---
title: Regras de preço de catálogo
description: Saiba mais sobre as regras de preço de catálogo que podem ser usadas para oferecer produtos a compradores por um preço com desconto com base em um conjunto de condições definidas.
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
TQID: https://experienceleague.adobe.com/JZE2DF0tp-XOsKjxo-WaQiwA3Y-FrM4TI5qq-Nze-qo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
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
source-wordcount: 468
ht-degree: 0%

---

# Regras de preço de catálogo

As regras de preço de catálogo podem ser usadas para oferecer produtos aos compradores por um preço com desconto, com base em um conjunto de condições definidas. As regras de preço de catálogo não usam [códigos de cupom](price-rules-cart-coupon.md), pois são acionadas antes de um produto ser colocado no carrinho de compras.

Por exemplo, você pode definir e definir as condições para uma regra de preço que, quando atendida, exibe automaticamente os produtos com um preço especial ou promocional. As propriedades de regras definidas podem incluir grupos de clientes, categorias de produtos, um valor ou porcentagem de desconto, cor do produto, tamanho do produto ou quase qualquer atributo de produto definido em sua loja. É possível definir datas inicial e final para uma regra de preço que inicie e interrompa automaticamente uma promoção nas datas definidas na regra. As propriedades de uma regra salva podem ser atualizadas ou modificadas, conforme necessário.

- ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Também é possível vincular uma regra definida a um [bloco dinâmico](../content-design/dynamic-blocks.md) para ajudar a promover o evento ou produto em sua loja.

- ![Magento Open Source](../assets/open-source.svg) (somente Magento Open Source) Para promoções recorrentes, você pode definir manualmente uma regra salva para o status _Ativo_ ou _Inativo_ sempre que desejar executar a promoção.

## Acessar regras de preço de catálogo

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

   ![Regras de preço de catálogo](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. Atualizar propriedades de uma regra:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Clique em **[!UICONTROL Edit]** para exibir a página _Informações da Regra_.

   - ![Magento Open Source](../assets/open-source.svg) (somente Magento Open Source) Clique na regra na lista para exibir a página Informações da Regra.

   Você pode alterar as configurações da regra (semelhante a [criando uma regra](price-rules-catalog-create.md)).

## Opções de filtro

| Campo | Descrição |
|--- |--- |
| [!UICONTROL ID] | Insira um texto para filtrar a lista de um número de ID de regra específico. |
| [!UICONTROL Rule] | Digite texto para filtrar a lista com base no nome da regra definido quando a regra foi criada. |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Digite texto neste campo para filtrar a lista com base na prioridade definida para uma regra. |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Use essa opção para filtrar a lista com base nos sites definidos para uma regra. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Clique em **[!UICONTROL Edit]** para exibir as Informações da Regra e atualizar as configurações da regra (semelhante à criação de uma regra). |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (somente Magento Open Source) Use os campos de calendário dinâmico (Para: e De:) para filtrar a lista com base na data de início da regra, conforme definido quando a regra foi criada. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (somente Magento Open Source) Use os campos de calendário dinâmico (Para: e De:) para filtrar a lista com base na data de término da regra, conforme definido quando a regra foi criada. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (somente Magento Open Source) Use esta opção para filtrar a lista com base no status da regra (`Active` ou `Inactive`). |

{style="table-layout:auto"}
