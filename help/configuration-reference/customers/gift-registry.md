---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Gift Registry]'
description: Revise as configurações no [!UICONTROL Customers] &gt; [!UICONTROL Gift Registry] página do Administrador do Commerce.
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

Para obter informações detalhadas sobre como usar essas configurações para habilitar registros de presentes para os clientes da loja, consulte [Configurar registros de presentes](../../merchandising-promotions/gift-registry-configure.md). Para obter informações sobre como incluir a pesquisa de registro de presentes na loja, consulte [Adicionar pesquisa de registro de presente](../../merchandising-promotions/gift-registry-search.md).

## [!UICONTROL General Options]

![Opções gerais](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Gift Registry] | Exibição da loja | Determina se os registros de presentes estão disponíveis. Opções: <br/>**`Yes`**- Habilita registros de presentes para a exibição de loja selecionada. A guia Registro de presentes aparece no painel de conta de clientes registrados.<br/>**`No`** - Os registros de presentes não estão disponíveis para a exibição de loja. |
| [!UICONTROL Maximum Registrants] | Exibição da loja | Define o número de pessoas que um cliente pode adicionar a um registro de presentes. O cliente compartilha o registro de presentes com cada inscrito. Na vitrine, o _Adicionar Inscrito_ O botão está disponível para clientes até que o número máximo seja atingido. |

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![Notificação do proprietário](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Email Template] | Exibição da loja | Determina o modelo usado para o email de Notificação do Proprietário enviado quando um registro de presente é criado. Modelo padrão: Notificação do proprietário do registro de presentes |
| [!UICONTROL Email Sender] | Exibição da loja | Identifica o [armazenar contato](../../getting-started/store-details.md#store-email-addresses) que aparece como o remetente do email de Notificação do Proprietário do Registro de Presentes. Valor padrão: `General Contact` |

{style="table-layout:auto"}

## Compartilhamento do Registro de presentes

![Compartilhamento do Registro de presentes](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Email Template] | Exibição da loja | Determina o modelo usado para o email de Compartilhamento do Registro de presentes enviado quando um registro de presentes é criado. Quando o proprietário clicar em _Compartilhar Registro de presentes_, o email é enviado para cada recipient. Modelo padrão: `Gift Registry Sharing` |
| [!UICONTROL Email Sender] | Exibição da loja | Identifica o [armazenar contato](../../getting-started/store-details.md#store-email-addresses) que aparece como o remetente do email Compartilhamento do Registro de presentes. Valor padrão: `General Contact` |
| [!UICONTROL Maximum Sent Emails Threshold] | Exibição da loja | O número máximo de mensagens de notificação por email do Registro de presentes que podem ser enviadas de uma vez. |

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![Atualização do Registro de presentes](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Email Template] | Exibição da loja | Determina o modelo usado para o email de Atualização do Registro de presentes que é enviado ao proprietário do Registro de presentes quando uma compra é feita no Registro de presentes. A atualização inclui informações sobre o item e a quantidade comprada, mas não inclui o nome da pessoa que fez o pedido. Modelo padrão: `Gift Registry Update` |
| [!UICONTROL Email Sender] | Exibição da loja | Identifica o [armazenar contato](../../getting-started/store-details.md#store-email-addresses) que aparece como o remetente do email Atualização do registro de presentes. Valor padrão: `General Contact` |

{style="table-layout:auto"}
