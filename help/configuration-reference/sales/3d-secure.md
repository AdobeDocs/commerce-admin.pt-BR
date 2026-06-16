---
title: '[!UICONTROL Sales] > [!UICONTROL 3D Secure]'
description: Revise as configurações na página [!UICONTROL Sales] > [!UICONTROL 3D Secure] do Administrador do Commerce.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
TQID: https://experienceleague.adobe.com/WzxM9ZYbobbC1fWSIph0jv89uXLte6Wzjs5be27eMyU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] foi desenvolvido por [!DNL Visa] para promover transações online seguras. Exemplos de soluções [!DNL 3-D Secure] criadas por redes de cartão são verificadas por [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey] e [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] é líder global em autenticação de transações digitais e é uma subsidiária integral da [!DNL Visa].

A versão 2.0 do [!DNL 3-D Secure] oferece suporte a várias melhorias, incluindo métodos de autenticação avançados e fluxo de autenticação, além de compartilhamento de dados aprimorado entre o comerciante e o emissor.

>[!NOTE]
>
>O gateway de pagamento [Braintree](../../stores-purchase/braintree.md) também oferece suporte à verificação [!DNL 3-D Secure].

{{config}}

## [!UICONTROL CardinalCommerce]

![CardealCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Environment] | Site | Indica o modo operacional da conta do [!DNL CardinalCommerce]. Se você estiver executando em um ambiente de teste, escolha &quot;Sandbox&quot;. Opções: Sandbox/Produção (Padrão) |
| [!UICONTROL Org Unit ID] | Site | A ID da unidade organizacional da sua conta de comerciante [!DNL CardinalCommerce]. |
| [!UICONTROL API Key] | Site | A Chave de API da sua conta de comerciante [!DNL CardinalCommerce]. |
| [!UICONTROL API Identifier] | Site | O Identificador de API da sua conta de comerciante [!DNL CardinalCommerce]. |
| [!UICONTROL Debug] | Site | Opções: `Yes` / `No` |

{style="table-layout:auto"}
