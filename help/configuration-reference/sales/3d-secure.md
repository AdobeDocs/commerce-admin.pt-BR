---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: Revise as configurações na página [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] do Administrador do Commerce.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

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
