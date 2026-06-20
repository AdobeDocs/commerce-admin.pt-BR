---
title: '[!UICONTROL Sales] > [!UICONTROL Shipping Settings]'
description: Revise as configurações na página [!UICONTROL Sales] > [!UICONTROL Shipping Settings] do Administrador do Commerce.
exl-id: d7d46946-f8c9-4714-96c3-2173e28f7bfa
feature: Configuration, Shipping/Delivery
TQID: https://experienceleague.adobe.com/4-Kmcd3F8pQyMgxp-NmkBFVNuEXWuYn-BOzpvxuFMhU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 204
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Shipping Settings]

{{config}}

Para obter mais informações sobre como alterar essas configurações, consulte [Configurações de remessa](../../stores-purchase/shipping-settings.md) no _Guia de Experiência de Compras e Lojas_.

## [!UICONTROL Origin]

![Origem](./assets/shipping-settings-origin.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Country] | Site | O país de ponto de origem. |
| [!UICONTROL Region/State] | Site | Região ou estado do ponto de origem. |
| [!UICONTROL ZIP/Postal Code] | Site | O CEP do ponto de origem. |
| [!UICONTROL City] | Site | A cidade do ponto de origem. |
| [!UICONTROL Street Address] | Site | O endereço do ponto de origem. |
| [!UICONTROL Street Address Line 2] | Site | Uma linha extra para o endereço do ponto de origem, se necessário. |

{style="table-layout:auto"}

## [!UICONTROL Shipping Policy Parameters]

![Parâmetros da Política de Remessa](./assets/shipping-settings-shipping-policy-parameters.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Apply Custom Shipping Policy] | Site | Determina se a política de envio aparece durante o check-out. Opções: `Yes` / `No` |
| [!UICONTROL Shipping Policy] | Exibição da loja | Contém a política de remessa como texto. |

{style="table-layout:auto"}

## [!UICONTROL Shipment Tracking URLs]

[!BADGE Somente SaaS]{type=Positive url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplicável somente a projetos do Adobe Commerce as a Cloud Service (infraestrutura SaaS gerenciada pela Adobe)."}

![Parâmetros da Política de Remessa](./assets/shipping-settings-shipment-tracking-urls.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Custom Tracking URLs] | Exibição da loja | Determina se os números de rastreamento de remessa enviados em emails do comprador são links ou texto sem formatação. O valor padrão de `No` indica que os números são texto simples. Opções: `Yes` / `No` |
| [!UICONTROL USPS Tracking URL] | Exibição da loja | O modelo de URL para remessas do Serviço Postal dos Estados Unidos. |
| [!UICONTROL UPS Tracking URL] | Exibição da loja | O modelo de URL para remessas do United Parcel Service. |
| [!UICONTROL FedEx Tracking URL] | Exibição da loja | O modelo de URL para remessas do Federal Express. |
| [!UICONTROL DHL Tracking URL] | Exibição da loja | O modelo de URL para remessas DHL Express. |

{style="table-layout:auto"}
