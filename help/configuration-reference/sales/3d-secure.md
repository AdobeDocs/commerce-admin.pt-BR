---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: Revise as configurações no [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] página do Administrador do Commerce.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] foi desenvolvido por [!DNL Visa] para promover transações on-line seguras. Exemplos de [!DNL 3-D Secure] As soluções criadas por redes de cartão são verificadas por [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey], e [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] é líder global em autenticação de transações digitais e subsidiária integral da [!DNL Visa].

[!DNL 3-D Secure] A versão 2.0 oferece suporte a várias melhorias, incluindo métodos de autenticação avançados e fluxo de autenticação, além de compartilhamento de dados aprimorado entre o comerciante e o emissor.

>[!NOTE]
>
>A variável [Braintree](../../stores-purchase/braintree.md) o gateway de pagamento também suporta [!DNL 3-D Secure] verificação.

{{config}}

## [!UICONTROL CardinalCommerce]

![CardealCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Environment] | Site | Indica o modo operacional do [!DNL CardinalCommerce] conta. Se você estiver executando em um ambiente de teste, escolha &quot;Sandbox&quot;. Opções: Sandbox/Produção (Padrão) |
| [!UICONTROL Org Unit ID] | Site | A ID da unidade organizacional do [!DNL CardinalCommerce] conta de comerciante. |
| [!UICONTROL API Key] | Site | A chave de API do seu [!DNL CardinalCommerce] conta de comerciante. |
| [!UICONTROL API Identifier] | Site | O identificador de API do seu [!DNL CardinalCommerce] conta de comerciante. |
| [!UICONTROL Debug] | Site | Opções: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
