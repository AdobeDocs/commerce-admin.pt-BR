---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Gift Cards]'
description: Revise as configurações na página [!UICONTROL Sales] &gt; [!UICONTROL Gift Cards] do Administrador do Commerce.
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![Configurações de email de cartão-presente](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | Exibição da loja | Identifica o [contato da loja](../../getting-started/store-details.md#store-email-addresses) que aparece como remetente do email de notificação de cartão-presente. Valor padrão: `General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | Exibição da loja | Determina o [modelo](../../systems/email-templates.md) usado para o email de notificação de cartão-presente. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![Configurações Gerais do Cartão-Presente](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Redeemable] | Global | Determina se o portador do cartão-presente pode resgatar seu valor em dinheiro. Opções: `Yes` / `No`. |
| [!UICONTROL Lifetime (days)] | Global | Determina o número de dias que o cartão é válido. Se deixado em branco, o cartão não expira. <br/><br/>**_Importante:_**&#x200B;em alguns locais, é ilegal definir dados de expiração em cartões-presente. Verifique suas leis locais antes de definir uma vida útil para seus cartões-presente. |
| [!UICONTROL Allow Gift Message] | Exibição da loja | Determina se a opção para incluir uma mensagem de presente está disponível para clientes que compram um cartão-presente. Opções: `Yes` / `No`. |
| [!UICONTROL Gift Message Maximum Length] | Exibição da loja | Determina o número máximo de caracteres permitidos em uma mensagem de cartão-presente. Valor padrão: 255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | Global | Determina se uma conta de cartão-presente é gerada quando um cliente faz um pedido ou quando o pedido é faturado. Opções: `Ordered` / `Invoiced` |

{style="table-layout:auto"}

## [!UICONTROL Email Sent from Gift Card Account Management]

![Email Enviado do Gerenciamento de Conta de Cartão-presente](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | Exibição da loja | Identifica o [contato da loja](../../getting-started/store-details.md#store-email-addresses) que aparece como remetente do email do cartão-presente. Valor padrão: `General Contact` |
| [!UICONTROL Gift Card Template] | Exibição da loja | Determina o [modelo](../../systems/email-templates.md) usado para o email de cartão-presente. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![Configurações Gerais da Conta de Cartão-Presente](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Code Length] | Global | Determina o comprimento do código do cartão-presente. |
| [!UICONTROL Code Format] | Global | Determina o formato do código do cartão-presente. Opções: `Alphanumeric` / `Numeric` |
| [!UICONTROL Code Prefix] | Global | Define qualquer prefixo adicionado ao início do código. |
| [!UICONTROL Code Suffix] | Global | Define qualquer sufixo adicionado ao final do código. |
| [!UICONTROL Dash Every X Characters] | Global | Se você quiser incluir traços no código, o determinará o número de caracteres entre cada traço. |
| [!UICONTROL New Pool Size] | Global | Determina o tamanho do novo pool de códigos a ser gerado. |
| [!UICONTROL Low Code Pool Threshold] | Global | Determina o número de registros no pool de códigos que aciona um alerta de que o pool precisa ser reabastecido. |
| [!UICONTROL Generate] | Global | Clique em para gerar a lista de códigos de cartão-presente. |

{style="table-layout:auto"}
